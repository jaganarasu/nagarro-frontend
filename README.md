# nagarro-frontend


Question1:- 
Stretch the Green block to the Parent, with two solutions, one with CSS flex, one with CSS Grid. 
https://nagarro.netlify.app/question1_with_grid

with grid style
.container {
    display: grid;
    border: 1px solid #000;
    height: 400px;
    width: 400px;
}
.container-box {
    grid-area: 1 / 1 / 2 / 2;
    background:green;
}

https://nagarro.netlify.app/question1_with_flex

with flex style
.container {
    display: flex;
    border: 1px solid #000;
    height: 400px;
    width: 400px;
}

.container-box {
    flex: 1;
    background:green;
}

Question2: -
Correct the HTML classes using BEM Methodology

https://nagarro.netlify.app/question2
<!-- BEM corrected code-->
 
1.Form Block:

The main form container is a block: .form.
The wrapper within the form is an element: .form__wrapper.
The actual form is an element: .form__inner.

2.Form Group Element:
Each input field and its label are grouped in an element: .form__group.

3.Input Element and Label Element:
The input elements: .form__input.
The label elements: .form__label.

4.Button Group Element:
The button group is an element: .form__button-group.

5.Button Element and Modifier:
The button element: .form__button.
The reset button modifier: .form__button--reset.
The submit button modifier: .form__button--submit.  


Question3: -
Stretch the "content" block to the full height of the "page" block, that the header to the top of the block and the footer to the bottom.

https://nagarro.netlify.app/question3_with_flex
with flex style

 .page {
    height: 600px;
    border: 1px solid #000;
    display: flex;
    flex-direction: column;
}

.page__header,
.page__footer {
    height: 50px;
    border: 1px solid #000;
    flex-shrink: 0;
}

.page__content {
    border: 1px solid #000;
    flex-grow: 1;
}

with grid style
https://nagarro.netlify.app/question3_with_grid 
 .page {
    height: 600px;
    border: 1px solid #000;
    display: grid;
    grid-template-rows: auto 1fr auto;
}

.page__header,
.page__footer {
    height: 50px;
    border: 1px solid #000;
}

.page__content {
    border: 1px solid #000;
}

Question4:-
 Make the first block same as “expected result”

 with flex style
 https://nagarro.netlify.app/question4_with_flex

"     body {
            margin: 0;
        }
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        img {
            display: block;
        }
        .wrapper {
            display: flex;
            flex-wrap: nowrap;
            gap: 5px;
            margin: 0 auto; 
        }
        .expected {
            background: gray;
            border:1px solid #000;
            padding: 25px;

            width: 460px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .expected__title {
            color: #fff;
            margin-bottom: 10px;
        }


         /* Flex option */
         .card {
            display: flex;  
            flex-direction: column;  
            
        }

        .card > * {
            flex: 1;  
        }


        
        .card {
            background: gray;
            border: 1px solid #000;
            padding: 25px;
            position: relative;  

            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .card__image {
            width: 100%;
            height: auto;
        }

        .card__content {
            position: absolute;
            display: flex; 
            flex-direction: column; 
            justify-content: space-between;  
            
        }

        .card__like{
            position: absolute;
            top: -150px;
            right: -78px;

        }
        .card__like img{
            width: 20px;
            height: 20px;
            border-radius: 15px;
        }
        .card__play {
            justify-items: center;
            text-decoration: none;
            text-align: center;
            color: #000;
            margin: auto;
            height: 40px;
            padding: 10px;
            background: #fff;
            width: 200px;
            border-radius: 15px;    
            font-weight: 800;
        }

        .card__info {
            margin-top: 10px;
            text-align: center;
            position: absolute;
            bottom: -184px;
             left: 0;
            right: 0;
        }

        .card__provider {
            display: block;
            color: #fff;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .card__description {
            display: block;
            color: #fff;
        }
"

with grid style
https://nagarro.netlify.app/question4_with_grid

"
body {
            margin: 0;
        }
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        img {
            display: block;
        }
        .wrapper {
            display: grid;
            grid-template-columns: repeat(2, 460px);
            grid-gap: 5px;
        }
        .expected {
            background: gray;
            border:1px solid #000;
            padding: 25px;
        }
        .expected__title {
            color: #fff;
            margin-bottom: 10px;
        }


        
        /* grid format */
  
        .card { display: grid}
        .card > * { grid-row: 1; grid-column: 1}

        .card {
            background: gray;
            border: 1px solid #000;
            padding: 25px;
        }

        .card__image {
            width: 100%;
            height: auto;
        }

        .card__content {
            display: grid;
            grid-template-rows: auto auto auto;
          
            margin-top: 10px;
        }

        .card__like{
            justify-self: right;
            margin: 25px;
        }
        .card__like img{
            border-radius: 15px;
        }
        .card__play {
            justify-items: center;
            text-decoration: none;
            text-align: center;
            color: #000;
            margin: auto;
            height: 50px;
            padding: 10px;
            background: #fff;
            width: 200px;
            border-radius: 15px;
            font-weight: 800;
        }

        .card__info {
            margin-top: 10px;
            text-align: center;
        }

        .card__provider {
            display: block;
            color: #fff;
            font-weight: bold;
            margin-bottom: 5px;
        }

        .card__description {
            display: block;
            color: #fff;
        }
"
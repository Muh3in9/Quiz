# Quiz

Let's break down the provided HTML code for a quiz website:

### HTML Structure Explanation

#### 1. `<!DOCTYPE html>`
This line defines the document type and version of HTML being used. It helps the browser to render the page correctly.

#### 2. `<html lang="en">`
This opening tag indicates the start of an HTML document and specifies the language as English (`lang="en"`).

#### 3. `<head>`
The `<head>` section contains meta-information about the document, such as its character encoding, title, and links to stylesheets.

- **`<meta charset="UTF-8">`**: This sets the character encoding for the document to UTF-8, which supports a wide range of characters.
- **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`**: This makes the website responsive by setting the viewport to the device's width and scaling it accordingly.
- **`<title>Quiz Website</title>`**: This sets the title of the web page, which appears in the browser tab.
- **`<link rel="stylesheet" href="style.css">`**: This links an external CSS file (`style.css`) to style the HTML document.

#### 4. `<body>`
The `<body>` section contains the content of the HTML document that will be displayed on the web page.

- **`<div class="application">`**: This is a container div that holds the main content of the quiz application.
  - **`<h1>Quiz Website</h1>`**: This is a header element displaying the title "Quiz Website".
  - **`<div class="quiz">`**: This is a container div for the quiz content.
    - **`<h2 id="question">Question goes here</h2>`**: This is a header element that will display the quiz question. The `id="question"` allows it to be easily accessed and modified by JavaScript.
    - **`<div id="answer-buttons">`**: This is a container div for the answer buttons. The `id="answer-buttons"` allows it to be easily accessed and modified by JavaScript.
      - **`<button class="btn">Answer 1</button>`**: These are buttons for the quiz answers. Each button has the class `btn`.
      - **`<button class="btn">Answer 2</button>`**
      - **`<button class="btn">Answer 3</button>`**
      - **`<button class="btn">Answer 4</button>`**
      - **`<button class="btn">Answer 5</button>`**
    - **`<button id="next-btn">Next</button>`**: This is a button to move to the next question. The `id="next-btn"` allows it to be easily accessed and modified by JavaScript.

#### 5. `<script src="script.js"></script>`
This includes an external JavaScript file (`script.js`) that contains the functionality for the quiz.

### Summary
- The HTML document sets up a basic structure for a quiz website.
- It includes a header, a container for the quiz question and answer buttons, and a button to proceed to the next question.
- External CSS and JavaScript files are linked to style the page and add functionality.

If you need further details or explanations about specific parts of this code or how to implement the JavaScript functionality for the quiz, feel free to ask!

Let's break down the provided CSS code step-by-step:

### Global Styles
```css
* {
    margin: 0;
    padding: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    box-sizing: border-box;
}
```
- **`*`**: Applies styles to all elements.
  - **`margin: 0;`**: Removes default margin from all elements.
  - **`padding: 0;`**: Removes default padding from all elements.
  - **`font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;`**: Sets a default font family for the entire document.
  - **`box-sizing: border-box;`**: Ensures that padding and border are included in the element's total width and height.

### Body Styles
```css
body{
    background: rgb(3, 0, 12);
}
```
- **`body`**: Styles the body element.
  - **`background: rgb(3, 0, 12);`**: Sets the background color to a dark shade of blue.

### Application Container Styles
```css
.application{
    background: lavender;
    width: 90%;
    max-width: 600px;
    margin: 100px auto 0;
    border-radius: 10px;
    padding: 30px;
}
```
- **`.application`**: Styles the main container for the quiz application.
  - **`background: lavender;`**: Sets the background color to lavender.
  - **`width: 90%;`**: Sets the width to 90% of the parent element.
  - **`max-width: 600px;`**: Sets the maximum width to 600 pixels.
  - **`margin: 100px auto 0;`**: Centers the container horizontally and adds 100 pixels of margin at the top.
  - **`border-radius: 10px;`**: Adds rounded corners with a 10-pixel radius.
  - **`padding: 30px;`**: Adds padding inside the container.

### Header Styles
```css
.application h1{
    font-size: 25px;
    color: #001;
    font-weight: 600;
    border-bottom: 1px solid #001;
}
```
- **`.application h1`**: Styles the header within the application container.
  - **`font-size: 25px;`**: Sets the font size to 25 pixels.
  - **`color: #001;`**: Sets the text color to a dark blue.
  - **`font-weight: 600;`**: Sets the font weight to 600 (semi-bold).
  - **`border-bottom: 1px solid #001;`**: Adds a dark blue bottom border.

### Quiz Container Styles
```css
.quiz{
    padding: 20px 0;
}
.quiz h2{
    font-size: 18px;
    color: #001;
    font-weight: 600;
}
```
- **`.quiz`**: Styles the quiz container.
  - **`padding: 20px 0;`**: Adds vertical padding.
- **`.quiz h2`**: Styles the question header within the quiz container.
  - **`font-size: 18px;`**: Sets the font size to 18 pixels.
  - **`color: #001;`**: Sets the text color to a dark blue.
  - **`font-weight: 600;`**: Sets the font weight to 600 (semi-bold).

### Button Styles
```css
.btn{
    background: lavender;
    color: #222;
    font-weight: 400;
    width: 100%;
    border: 1px solid #222;
    padding: 10px;
    margin: 10px 0;
    text-align: left;
    border-radius: 4px;
    cursor: pointer;
}
.btn:hover:not([disabled]){
    background: rgb(3, 0, 12);
    color: lavenderblush;
}
.btn:disabled{
    cursor: no-drop;
}
```
- **`.btn`**: Styles the answer buttons.
  - **`background: lavender;`**: Sets the background color to lavender.
  - **`color: #222;`**: Sets the text color to dark gray.
  - **`font-weight: 400;`**: Sets the font weight to 400 (normal).
  - **`width: 100%;`**: Sets the width to 100% of the parent element.
  - **`border: 1px solid #222;`**: Adds a dark gray border.
  - **`padding: 10px;`**: Adds padding inside the button.
  - **`margin: 10px 0;`**: Adds vertical margin.
  - **`text-align: left;`**: Aligns the text to the left.
  - **`border-radius: 4px;`**: Adds rounded corners with a 4-pixel radius.
  - **`cursor: pointer;`**: Changes the cursor to a pointer on hover.
- **`.btn:hover:not([disabled])`**: Styles the button on hover when it is not disabled.
  - **`background: rgb(3, 0, 12);`**: Changes the background color to dark blue.
  - **`color: lavenderblush;`**: Changes the text color to lavenderblush.
- **`.btn:disabled`**: Styles the button when it is disabled.
  - **`cursor: no-drop;`**: Changes the cursor to indicate the button cannot be clicked.

### Next Button Styles
```css
#next-btn{
    background: #001;
    color: azure;
    font-weight: 500;
    width: 150px;
    border: 0;
    padding: 10px;
    margin: 20px auto 0;
    border-radius: 4px;
    cursor: pointer;
    display: none;
}
```
- **`#next-btn`**: Styles the next button.
  - **`background: #001;`**: Sets the background color to dark blue.
  - **`color: azure;`**: Sets the text color to azure.
  - **`font-weight: 500;`**: Sets the font weight to 500 (medium).
  - **`width: 150px;`**: Sets the width to 150 pixels.
  - **`border: 0;`**: Removes the border.
  - **`padding: 10px;`**: Adds padding inside the button.
  - **`margin: 20px auto 0;`**: Adds vertical and horizontal margin to center the button.
  - **`border-radius: 4px;`**: Adds rounded corners with a 4-pixel radius.
  - **`cursor: pointer;`**: Changes the cursor to a pointer on hover.
  - **`display: none;`**: Hides the button by default.

### Answer Indicator Styles
```css
.correct{
    background: rgba(0, 100, 0, 0.467);
}
.incorrect{
    background: rgba(139, 0, 0, 0.404); 
}
```
- **`.correct`**: Styles the correct answer indicator.
  - **`background: rgba(0, 100, 0, 0.467);`**: Sets a semi-transparent green background.
- **`.incorrect`**: Styles the incorrect answer indicator.
  - **`background: rgba(139, 0, 0, 0.404);`**: Sets a semi-transparent red background.

### Summary
- **Global Styles**: Applied to all elements to reset margins, paddings, set a default font, and use border-box sizing.
- **Body Styling**: Sets a dark background color.
- **Application Container**: Styled with a lavender background, centered with rounded corners and padding.
- **Header Styling**: Header within the application container with specific font size, color, and a bottom border.
- **Quiz Container**: Contains padding and styles for the question header.
- **Button Styling**: Answer buttons with hover effects and disabled styles.
- **Next Button**: Specific styles for the next question button, including centering and hiding by default.
- **Answer Indicators**: Styles for indicating correct and incorrect answers with semi-transparent backgrounds.

If you need further details or have any specific questions about the CSS, feel free to ask!

Let's break down the JavaScript code for the quiz application step-by-step:

### Code Explanation

#### 1. Question Data
```javascript
const questions = [
    {
        question: "Who is the first Worlds Money Richest Man? in 2024",
        answers: [
            { text: "Jeff Bezos", correct: false},
            { text: "Mark ZuckerBerg", correct: false},
            { text: "Leonal Messi", correct: false},
            { text: "Elon Musk", correct: true},
            { text: "Mohammed Salla", correct: false},
        ]
    },
    {
        question: "What is th world's most Brainless,Heartless and ugly thing",
        answers: [
            { text: "Germany", correct: false},
            { text: "Isreal", correct: true},
            { text: "United Kingdom(UK)", correct: false},
            { text: "India", correct: false},
            { text: "Russia", correct: false},
        ]
    },
    {
        question: "What is the largest animal in the world",
        answers: [
            { text: "Blue whale", correct: true},
            { text: "Shark", correct: false},
            { text: "Elephant", correct: false},
            { text: "Hippopotamus", correct: false},
            { text: "Giraffe", correct: false},
        ]
    },
    {
        question: "What is the smallest continent in the world?",
        answers: [
            { text: "Asia", correct: false},
            { text: "Africa", correct: false},
            { text: "Antarctica", correct: false},
            { text: "North America", correct: false},
            { text: "Australia", correct: true},
        ]
    },
    {
        question: "What is the largest desert in the world",
        answers: [
            { text: "Kalahari", correct: false},
            { text: "Antarctica", correct: true},
            { text: "Sahara", correct: false},
            { text: "Gobi", correct: false},
            { text: "Austria", correct: false},
        ]
    }
];
```
- **`questions`**: An array of question objects, each containing a question string and an array of answer objects. Each answer object has text and a boolean indicating if it is correct.

#### 2. Selecting Elements
```javascript
const questionElement = document.getElementById("question");
const answerButtons = document.getElementById("answer-buttons");
const nextButton = document.getElementById("next-btn");
```
- **`questionElement`**: Selects the HTML element with the ID `question`.
- **`answerButtons`**: Selects the HTML element with the ID `answer-buttons`.
- **`nextButton`**: Selects the HTML element with the ID `next-btn`.

#### 3. Initial Variables
```javascript
let currentQuestionIndex = 0;
let score = 0;
```
- **`currentQuestionIndex`**: Tracks the current question index.
- **`score`**: Tracks the user's score.

#### 4. Starting the Quiz
```javascript
function startQuiz() {
    currentQuestionIndex = 0;
    score = 0;
    nextButton.innerHTML = "Next";
    showQuestion();
}
```
- **`startQuiz()`**: Resets the question index and score, updates the next button text, and shows the first question.

#### 5. Showing Questions
```javascript
function showQuestion() {
    resetState();
    let currentQuestion = questions[currentQuestionIndex];
    let questionNo = currentQuestionIndex + 1;
    questionElement.innerHTML = questionNo + ". " + currentQuestion.question;

    currentQuestion.answers.forEach(answer => {
        const button = document.createElement("button");
        button.innerHTML = answer.text;
        button.classList.add("btn");
        answerButtons.appendChild(button);
        if (answer.correct) {
            button.dataset.correct = answer.correct;
        }
        button.addEventListener("click", selectanswer);
    });
}
```
- **`showQuestion()`**: Resets the state, gets the current question, updates the question element, and creates buttons for each answer. Adds an event listener to each button for selecting an answer.

#### 6. Resetting State
```javascript
function resetState() {
    nextButton.style.display = "none";
    while (answerButtons.firstChild) {
        answerButtons.removeChild(answerButtons.firstChild);
    }
}
```
- **`resetState()`**: Hides the next button and removes existing answer buttons.

#### 7. Selecting an Answer
```javascript
function selectanswer(e) {
    const selectedBtn = e.target;
    const isCorrect = selectedBtn.dataset.correct === "true";
    if (isCorrect) {
        selectedBtn.classList.add("correct");
        score++;
    } else {
        selectedBtn.classList.add("incorrect");
    }
    Array.from(answerButtons.children).forEach(button => {
        if (button.dataset.correct === "true") {
            button.classList.add("correct");
        }
        button.disabled = true;
    });
    nextButton.style.display = "block";
}
```
- **`selectanswer(e)`**: Handles answer selection, checks if the selected answer is correct, updates the button styles, and disables all buttons. Shows the next button.

#### 8. Showing the Score
```javascript
function showScore() {
    resetState();
    questionElement.innerHTML = `You scored ${score} out of ${questions.length}!`;
    nextButton.innerHTML = "Play Again";
    nextButton.style.display = "block";
}
```
- **`showScore()`**: Resets the state, displays the user's score, updates the next button text, and shows the next button.

#### 9. Handling the Next Button
```javascript
function handleNextButton() {
    currentQuestionIndex++;
    if (currentQuestionIndex < questions.length) {
        showQuestion();
    } else {
        showScore();
    }
}
```
- **`handleNextButton()`**: Increments the question index and either shows the next question or the score.

#### 10. Adding Event Listeners
```javascript
nextButton.addEventListener("click", () => {
    if (currentQuestionIndex < questions.length) {
        handleNextButton();
    } else {
        startQuiz();
    }
});

startQuiz();
```
- **`nextButton.addEventListener("click", () => {...})`**: Adds a click event listener to the next button to handle moving to the next question or restarting the quiz.
- **`startQuiz();`**: Starts the quiz when the script runs.

### Summary
- **Question Data**: Contains the questions and answers for the quiz.
- **Element Selection**: Selects relevant HTML elements.
- **State Management**: Tracks the current question index and user's score.
- **Quiz Functions**: Functions to start the quiz, show questions, reset state, select answers, show the score, and handle the next button.
- **Event Listeners**: Adds event listeners to handle user interactions.

If you have any specific questions or need further details on any part of the code, feel free to ask!

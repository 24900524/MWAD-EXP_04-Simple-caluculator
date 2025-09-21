# MWAD-EXP_04-Simple-caluculator
## Date: 21.09.2025

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
## HTML
```
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="calc.css">
</head>
<body>
    <h1>CALCULATOR</h1>
    <div class="calculator">
        <input type="text" id="display">
        <div class="buttons">
            <button onclick="cleardisplay()">C</button>
            <button onclick="appendvalue('/')">/</button>
            <button onclick="appendvalue('-')">-</button>
            <button onclick="appendvalue('*')">X</button>

            <button onclick="appendvalue('7')">7</button>
            <button onclick="appendvalue('8')">8</button>
            <button onclick="appendvalue('9')">9</button>
            <button onclick="appendvalue('+')">+</button>

            <button onclick="appendvalue('4')">4</button>
            <button onclick="appendvalue('5')">5</button>
            <button onclick="appendvalue('6')">6</button>
            <button onclick="calculateresult()">=</button>

            <button onclick="appendvalue('1')">1</button>
            <button onclick="appendvalue('2')">2</button>
            <button onclick="appendvalue('3')">3</button>
            <button onclick="appendvalue('.')">.</button>
        </div>
    </div>
</body>
<script src="calc.js"></script>
</html>
```
## CSS
```
body{
    margin: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: rgb(227, 220, 220);
    font-family: Arial, Helvetica, sans-serif;
}

.calculator{
    border: 2px solid black;
    background-color: #333;
    border-radius: 9px;
    padding: 25px;
    width: 280px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.6);
}

.buttons{
    display: grid;
    grid-template-columns: repeat(4,1fr);
    gap: 5px;
}

button{
    height: 50px;
    font-size: 25px;
    border: none;
    border-radius: 5px;
    font-weight: 400;
    cursor: pointer;
    transition: background 0.2s ease ;
}

button:hover{
    background: rgb(185, 179, 179);
}

button:active{
    background: rgb(148, 140, 140);
}

#display{
    width: 100%;
    height: 50px;
    font-size: 25px;
    text-align: right;
    margin-bottom: 10px;
    border: none;
    border-radius: 4px;
}
```
## JAVASCRIPT 
```
const display = document.getElementById('display')

// add function

function appendvalue(value){
    display.value += value
}

function cleardisplay(){
    display.value = ''
}

//try and catch property

function calculateresult(){
    try{
        display.value = eval(display.value)
    }
    catch(error){
        alert("Invalid Expression")
        cleardisplay()
    }
}
```

## OUTPUT
<img width="1919" height="1134" alt="image" src="https://github.com/user-attachments/assets/a0181dc6-8e31-4bc1-bccb-84b2d6b84a4b" />

## RESULT
The program for developing a simple calculator in React.js is executed successfully.

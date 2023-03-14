# JavaScript

## Variables

Variables are containers for storing data (storing data values).

we can declare variable use let , var and for constant Value const.

The `var` keyword is used in all JavaScript code from 1995 to 2015.

The `let` and `const` keywords were added to JavaScript in 2015.

If you want your code to run in older browsers, you must use `var`.

Variables defined with `let` cannot be Redeclared.

Variables defined with `let` must be Declared before use.

Variable defined with Var can be Redeclared and we can declare after using it.

```jsx
let x=5;
var y=15;
const p=4;

```

## Data Types

There are 8 datatypes in JavaScript

1.String

2. Number

3. Big int

4. Boolean

5. Undefined

6. Null

7. Symbol

8. Object

## Control flow statement(if/Else)

1. If/else statement

The if else statement is a conditional statement and the block of code only execute if the if condition is true .

```jsx
if (hour < 18) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```

if  there is another alternative method is there we use if-else-if statment

```jsx
if (time < 10) {
  greeting = "Good morning";
} else if (time < 20) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```

Switch statement is another type of conditional statement use the variable as parameter and the options with their block of code using **case** keyword and **break** keywork to terminate the checking if the **case** condition is satisfied.

```jsx
switch (new Date().getDay()) {case 0:day = "Sunday";break;
case 1:day = "Monday";break;
case 2:day = "Tuesday";break;
case 3:day = "Wednesday";break;
case 4:day = "Thursday";break;
case 5:day = "Friday";break;
case 6:day = "Saturday";
}
```

## Loop

For loop: 

```jsx
for (let i = 0; i < 5; i++) {
  text += "The number is " + i + "<br>";
}
```

## Do while loop

```jsx
do {
  text += "The number is " + i;
  i++;
}
while (i < 10);
```

## Functions

A JavaScript function is defined with the `function` keyword, followed by a **name**, followed by parentheses **()**.

```jsx
let x = myFunction(4, 3);   // Function is called, return value will end up in x

function myFunction(a, b) {
  return a * b;             // Function returns the product of a and b
}
```

## Objects

You define (and create) a JavaScript object with an object literal:

```jsx
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

## Events

An HTML event can be something the browser does, or something a user does.

Here are some examples of HTML events:

- An HTML web page has finished loading
- An HTML input field was changed
- An HTML button was clicked

| onchange | An HTML element has been changed |
| --- | --- |
| onclick | The user clicks an HTML element |
| onmouseover | The user moves the mouse over an HTML element |
| onmouseout | The user moves the mouse away from an HTML element |
| onkeydown | The user pushes a keyboard key |
| onload | The browser has finished loading the page |

**JavaScript Notes From Asabeneh 30-Days-of-JavaScript**

```jsx
console.log(’Hello world’) //To display some text on the console
let string='Java';
let Firstletter=string[0]; //Accessing each values of strings
string.charAt(index)// to change/access specfic string value
string.concat(values to be concatinated)
let string='Love is the best to in the world';
console.log(string.endswith('world');//true endswith returns boolean value
console,log(string.includes('best');
console.log(indexOf('wolrd'); //returns the index 
//of the first element of the substring if the word exists if not it returns -1
```
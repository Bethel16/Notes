# JSON

**Json(JavaScript object notation)**

JSON is a light weight data format for storing and transporting. JSON is mostly used when data is sent from a server to a client. JSON is an easier-to-use alternative to XML.The difference  between java script and JSON is the key of a JSON object should be with double quotes or it should be a string. JavaScript Object and JSON are very similar that we can change JSON to Object and Object to JSON.

JSON is a **text format** for storing and transporting data

JSON is "self-describing" and easy to understand

# Why Use JSON?

The JSON format is syntactically similar to the code for creating JavaScript objects. Because of this, a JavaScript program can easily convert JSON data into JavaScript objects.

Since the format is text only, JSON data can easily be sent between computers, and used by any programming language.

JSON is a wildly successful way of formatting data for several reasons. First, it's native to JavaScript, and it's used inside of JavaScript programs as JSON literals. You can also use JSON with other programming languages, so **it's useful for data exchange between heterogeneous systems**
. Finally, it is human readable.

JavaScript has a built in function for converting JSON strings into JavaScript objects:

`JSON.parse()`

JavaScript also has a built in function for converting an object into a JSON string:

`JSON.stringify()`

JSON format Vs Javascript objects

```json
Javascript Objects
const users = {
  Alex: {
    email: 'alex@alex.com',
    skills: ['HTML', 'CSS', 'JavaScript'],
    age: 20,
    isLoggedIn: false,
    points: 30
  },
  Asab: {
    email: 'asab@asab.com',
    skills: [
      'HTML',
      'CSS',
      'JavaScript',
      'Redux',
      'MongoDB',
      'Express',
      'React',
      'Node'
    ],
    age: 25,
    isLoggedIn: false,
    points: 50
  }}

JSON 
{
    "Alex": {
        "email": "alex@alex.com",
        "skills": [
            "HTML",
            "CSS",
            "JavaScript"
        ],
        "age": 20,
        "isLoggedIn": false,
        "points": 30
    },
    "Asab": {
        "email": "asab@asab.com",
        "skills": [
            "HTML",
            "CSS",
            "JavaScript",
            "Redux",
            "MongoDB",
            "Express",
            "React",
            "Node"
        ],
        "age": 25,
        "isLoggedIn": false,
        "points": 50
    }}
```

```json
const usersObj = JSON.parse(usersText, undefined, 4) // to convert JSON  to Javascript object`

JSON.stringify(obj, replacer, space) // converting Object to JSON`

const txt = JSON.stringify(user,['firstName', 'lastName', 'country', 'city', 'age'],4)// to convert selecetd objects as an array to JSON format`
```

Looping an Array

```json
<script>
const myJSON = '{"name":"John", "age":30, "cars":["Ford", "BMW", "Fiat"]}';
const myObj = JSON.parse(myJSON);

let text = "";
for (let i = 0; i < myObj.cars.length; i++) {
  text += myObj.cars[i] + ", ";
}

document.getElementById("demo").innerHTML = text; // The result will display inside demo in html
</script
```

**Promises in JavaScript**

Promises are objects that represent the eventual completion or failure of an asynchronous operation and its resulting value. They allow us to handle asynchronous operations without blocking the main thread. Promises are used to handle asynchronous operations, such as fetching data from a server.

Promises have three states:

- Pending: The initial state; the promise is neither fulfilled nor rejected.
- Fulfilled: The operation completed successfully, and the promise has a resulting value.
- Rejected: The operation failed, and the promise has a reason for the failure.

Promises have two methods:

- then(): It is used to handle the fulfilled state of a promise.
- catch(): It is used to handle the rejected state of a promise.

Example of a promise:

```
const promise = new Promise((resolve, reject) => {
  const x = 5;
  const y = 2;
  if (x + y === 7) {
    resolve("Promise fulfilled");
  } else {
    reject("Promise rejected");
  }
});

promise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });

```

The above example creates a promise that adds two numbers and resolves if the result is 7. The promise is then handled using the then() method to log the result to the console if fulfilled, and the catch() method to log the error to the console if rejected.

**DOM**

HTML document is structured as a JavaScript Object. Every HTML element has a different properties which can help to manipulate it. It is possible to get, create, append or remove HTML elements using JavaScript.

**Getting elements by tag name**

```jsx
document.getElementsByTagName('tagname')
const allTitles = document.getElementsByTagName('h1')

console.log(allTitles) //HTMLCollections
console.log(allTitles.length) // 4

for (let i = 0; i < allTitles.length; i++) {
console.log(allTitles[i]) // prints each elements in the HTMLCollection

document.getElementsByClassName('classname')
document.getElementsByClassName('id')

const allTitles = document.querySelectorAll('h1') # selects all the available h1 elements in the page

console.log(allTitles.length) // 4
```

**Adding attribute**

```jsx
const titles = document.querySelectorAll('h1')
titles[3].className = 'title'
titles[3].id = 'fourth-title'
```

**Adding attribute using setAttribute**

```jsx
const titles = document.querySelectorAll('h1')
titles[3].setAttribute('class', 'title')
titles[3].setAttribute('id', 'fourth-title')
```

### Adding class using classList

```jsx
//another way to setting an attribute: append the class, doesn't over ride
titles[3].classList.add('title', 'header-title')
//another way to setting an attribute: append the class, doesn't over ride
titles[3].classList.remove('title', 'header-title')
```

**Adding Text content using textContent**

```jsx
const titles = document.querySelectorAll('h1')
titles[3].textContent = 'Fourth Title'
```

**Adding Text Content using innerHTML**

```html
<!DOCTYPE html>
<html lang="en">
<head> <title> JavaScript for everyone </title>
<body> 
<h1>Lists Using JavaScript</h1>
<ul> </ul>
<script>
const lists= `<li>30DaysOfPython Challenge Done</li>
            <li>30DaysOfJavaScript Challenge Ongoing</li>
            <li>30DaysOfReact Challenge Coming</li>
            <li>30DaysOfFullStack Challenge Coming</li>
            <li>30DaysOfDataAnalysis Challenge Coming</li>
            <li>30DaysOfReactNative Challenge Coming</li>
            <li>30DaysOfMachineLearning Challenge Coming</li>`
const ul=document.querySelector('ul)
ul.innerHTML=lists
 </script>
</body>
</html>
```

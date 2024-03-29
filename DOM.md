# DOM

**DOM**

The **Document Object Model** (*DOM*) is the data representation of the objects that comprise the structure and content of a document on the web. This guide will introduce the DOM, look at how the DOM represents an [HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML) document in memory and how to use APIs to create web content and applications.

HTML document is structured as a JavaScript Object. Every HTML element has a different properties which can help to manipulate it. It is possible to get, create, append or remove HTML elements using JavaScript.

The Document Object Model (DOM) is a representation of the structure and content of a web document. It is possible to manipulate HTML elements using JavaScript, and there are several APIs available to do so. This document provides examples of how to get elements by tag name, add attributes, add text content, and add styles using the DOM.

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

### Adding Style Background Color

Let us add some style to our titles. If the element has even index we give it green color else red.

```jsx
const titles = document.querySelectorAll('h1')
titles.forEach((title, i) => {
  title.style.fontSize = '24px' // all titles will have 24px font size
  if (i % 2 === 0) {
    title.style.backgroundColor = 'green'
  } else {
    title.style.backgroundColor = 'red'
  }
})
```

### Adding Style Font Size

Let us add some style to our titles. If the element has even index we give it 20px else 30px

```jsx
const titles = document.querySelectorAll('h1')
titles.forEach((title, i) => {
  title.style.fontSize = '24px' // all titles will have 24px font size
  if (i % 2 === 0) {
    title.style.fontSize = '20px'
  } else {
    title.style.fontSize = '30px'
  }
})
```

### **To create HTML element using JavaScript**

The Document object provides a method **createElement()** to create an element and **appendChild()** method to add it to the HTML DOM. Following are the steps involved in creating HTML DOM −

**Step 1** − To insert an element into HTML DOM, firstly, we need to create an element and append to HTML DOM. The **document.createElement()** is used to create the HTML element. The syntax to create an element is shown below.

```jsx
document.createElement(tagName[, options]);

```

Where,

- **tagName** is the name of the tag to be created. The tag is of <p> type.
- **options** param is an optional element object.

**Step 2** − After creation of a tag, we need to create a text to assign to the tag. The syntax to create a text node is shown below.

```jsx
Document.createTextNode(“String”);

```

**Step 3** − After creating the text, we need to add the text to the element <p> type and thus finally adding to the div tag. The syntax to append the element to a tag is shown below.

```
appendChild(parameter);

```

### **Example 1**

In the following example, initially the div section consists of only 2 texts. But later on, one more text is created and added to the div section as shown in the output.

```html
<html>
<body>
   <div id="new">
      <p id="p1">Tutorix</p>
      <p id="p2">Tutorialspoint</p>
   </div>
   <script>
      var tag = document.createElement("p");
      var text = document.createTextNode("Tutorix is the best e-learning platform");
      tag.appendChild(text);
      var element = document.getElementById("new");
      element.appendChild(tag);
   </script>
</body>
</html>

```

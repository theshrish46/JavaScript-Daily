# What are functions in JavaScript?

### In this section, we'll explore what functions are and the different types of functions in JavaScript.

<p>Functions are one of the key building blocks of programming in JavaScript. They allow developers to encapsulate reusable pieces of code, which can be called upon and executed whenever they're needed. Functions are used to define procedures, execute code blocks, and perform specific tasks in JavaScript.</p>

<br>

## What are functions in JavaScript?

A function in JavaScript is a block of code that can be called upon and executed whenever it's needed. It's a self-contained unit of code that can take inputs, process them, and produce outputs. Functions can be defined using the "function" keyword, and they can be stored in variables, passed as arguments to other functions, or returned as values.

<br>

# Types of Functions in JavaScript

<br>

## Function Declarations

<p>A function declaration is one of the most common ways of defining a function in JavaScript. It starts with the "function" keyword, followed by the name of the function, a list of parameters enclosed in parentheses, and the function's body enclosed in curly braces. Function declarations are hoisted, which means they can be called before they're defined in the code.</p>

Example:

```js
function addNumbers(num1, num2) {
  return num1 + num2;
}
```

<br>

## Function Expressions

<p>A function expression is another way of defining a function in JavaScript. It's similar to function declarations, but the function is assigned to a variable. Function expressions can be named or anonymous, and they're not hoisted, which means they can only be called after they're defined.</p>

Example:

```js
const addNumbers = function (num1, num2) {
  return num1 + num2;
};
```

<br>

## Arrow Functions
<p>Arrow functions are a shorthand way of defining functions in JavaScript. They're anonymous functions that use the "=>" symbol instead of the "function" keyword. Arrow functions are often used as callbacks or to create functions that return values.</p>

Example:
```js
const addNumbers = (num1, num2) => {
return num1 + num2;
}
```
<br>

## Method Functions
<p>Method functions are functions that are defined inside objects. They're called using the object's name followed by a dot and the method name. Method functions have access to the object's properties and can modify them.</p>

Example:
```js
const myObject = {
firstName: "John",
lastName: "Doe",
getFullName: function() {
return `${this.firstName} ${this.lastName}`;
}
};
```
<br>

## Constructor Functions
<p>Constructor functions are used to create new objects. They're defined using the "function" keyword and are used with the "new" keyword to create instances of the object. Constructor functions typically set the initial values of the object's properties.</p>

Example:
```js
function Person(firstName, lastName) {
this.firstName = firstName;
this.lastName = lastName;
}

const johnDoe = new Person("John", "Doe");
```
<br>

## Conclusion
<p>Functions are a fundamental concept in JavaScript that encapsulates reusable code. There are different types of functions in JavaScript, including function declarations, function expressions, arrow functions, method functions, and constructor functions. Each type of function has its unique features and use cases. By understanding the different types of functions in JavaScript, developers can write more efficient, maintainable, and scalable code.</p>
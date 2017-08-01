# Javascript syntax

## Variables

Variables ES5
```javascript
var myVar; // value = undefined
var data = 5; // value = 5
```

Variables ES6
```javascript
let num = 5 // Local Variable
const PI = 3.14 // constant
```

## Data Types

Number
```javascript
let myInt = 5; // number
let myDec = 10.5 // number
```
Boolean
```javascript
let yes = true;
let no = false;
```
String
```javascript
let text = "Say 'Hello'"; // "" === ''
let text = 'Say "Hello"'; // '' === ""
```
Undefined
```javascript
var data; // its value is undefined
var data = undefined;
```
## Template Literals (ES6)

Multiline
```javascript
var text = `This is a template literal`;
var paragraph = `This is a
    new paragraph`; // template literal support multiline
```
Variables inside
```javascript
var name = 'World';
var greeting = `Hello ${name}`; // template literal support variables inside of text
```
## Objects

Object
```javascript
var myObject = { property: "value" }; // JSON Object
var myObject = new Object({ property: "value" }); // new instance of object
```
Arrays
```javascript
var myArray = []; // Array is an Object
var myArray = new Array(); // new instance of Array
var myArray = [1, 2, 3, 4]; // Array init
```

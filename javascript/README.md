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
var note = `${teacher.name},

    Please excuse ${student.name}.
    He is recovering from the flu.

    Thank you,
    ${student.guardian}`;
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
Object Literal Shorthand
```Javascript
let type = 'quartz';
let color = 'rose';
let carat = 21.29;

let gemstone = {
    type = type,
    color = color,
    carat = carat
};
// or 
let gemstone = { type, color, carat };
```

Arrays
```javascript
var myArray = []; // Array is an Object
var myArray = new Array(); // new instance of Array
var myArray = [1, 2, 3, 4]; // Array init
```

## Iterations

```javascript
// ES5
const years = ['1999', '2001', '2013', '2016'];

for (let i = 0; i< years.length; i++) {
    console.log(years[i])
}
// ES6 => for..of loop
const names = ['James', 'Kavita', 'Richard'];

for (const name of names) {
    console.log(name);
}
```

```Javascript
const months = new Set(['January', 'February', 'March', 'April', 'May', 'June', 'July', 'August', 'September', 'October', 'November', 'December']);

const iterator = months.values();

iterator.next(); // { value: 'January', done: false }
iterator.next(); // { value: 'February', done: false }
iterator.next(); // { value: 'March', done: false }

```

## Functions

```Javascript
// function ES5
const upperizedNames = ['Farrin', 'Kagure', 'Asser'];
    .map(function (name) {
        return name.toUpperCase();
    });
// function ES6 arrow functions
const upperizedNames = ['Farrin', 'Kagure', 'Asser'];
    .map(name => name.toUpperCase());
```

## Classes

```javascript
// ES5 Object
function Plane(numEngines) {
    this.numEngines = numEngines;
    this.enginesActive = false;
}

Plane.prototype.startEngines = function () {
    console.log('starting engines...');
    this.enginesActive = true;
};

var richardsPlane = new Plane(1);
richardsPlane.startEngines();

var jamesPlane = new Plane(4);
jamesPlane.startEngines();
// ES6
class Plane {
    constructor() {
        this.numEngines = numEngines;
        this.enginesActive = false;
    }

    startEngines() {
        console.log('starting engines...');
        this.enginesActive = true;
    }
}

var richardsPlane = new Plane(1);
richardsPlane.startEngines();

var jamesPlane = new Plane(4);
jamesPlane.startEngines();
```

## Extending classes

```Javascript
class Tree {
    constructor(size = '10', leaves = { spring: 'green' })

    changeSeason(season) {...}
}

class Maple extends Tree {
    constructor(syrupQty = 15, size, barkColor, leaves) {
        super(size, barkColor, leaves);
        this.syrupQty = syrupQty;
    }

    changeSeason(season) {...}

    gatherSyrup() {...}
}

```
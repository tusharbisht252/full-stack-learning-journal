# JavaScript Functions

JavaScript functions are reusable blocks of code used to perform a specific task. They help make code **modular, reusable, and easier to maintain**.

---

## Function Declaration

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

console.log(greet("Bhanu"));
```

---

## Function Expression

```javascript
const add = function(a, b) {
    return a + b;
};

console.log(add(5, 3));
```

---

## Arrow Function

```javascript
const square = (num) => num * num;

console.log(square(5));
```

---

## Parameters & Arguments

* **Parameters** are variables defined in a function.
* **Arguments** are the actual values passed while calling the function.

```javascript
function multiply(a, b) {
    return a * b;
}

console.log(multiply(4, 6));
```

---

## Return Statement

The `return` statement sends a value back from a function.

```javascript
function cube(num) {
    return num ** 3;
}

console.log(cube(3));
```

---

## Callback Function

A callback is a function passed as an argument to another function.

```javascript
function process(callback) {
    callback();
}

process(() => {
    console.log("Task Completed");
});
```

---

## Scope

Scope determines where a variable can be accessed.

* **Global Scope** → Accessible throughout the program.
* **Local Scope** → Accessible only inside a function.
* **Block Scope** → Accessible only inside a block `{ }`.

```javascript
let language = "JavaScript";

function showLanguage() {
    console.log(language);
}
```

---

# JavaScript Events

An **event** is an action that occurs in the browser, such as clicking a button, typing in an input box, or moving the mouse.

JavaScript can respond to these events using **event listeners**.

## Common Events

| Event       | Description                            |
| ----------- | -------------------------------------- |
| `click`     | Triggered when an element is clicked   |
| `dblclick`  | Triggered on double click              |
| `mouseover` | Mouse enters an element                |
| `mouseout`  | Mouse leaves an element                |
| `keydown`   | A key is pressed                       |
| `keyup`     | A key is released                      |
| `input`     | Input value changes                    |
| `submit`    | Form is submitted                      |
| `change`    | Input value changes after losing focus |
| `load`      | Page finishes loading                  |

---

## Event Listener

The `addEventListener()` method is the preferred way to handle events.

```javascript
const button = document.querySelector("button");

button.addEventListener("click", () => {
    alert("Button Clicked!");
});
```

---

## Event Object

JavaScript automatically passes an **event object** containing information about the event.

```javascript
document.addEventListener("click", function(event) {
    console.log(event.target);
});
```

### Common Event Object Property

* `event.target` → Element on which the event occurred.

---

## Prevent Default Action

`preventDefault()` stops the browser's default behavior for an event.

```javascript
const form = document.querySelector("form");

form.addEventListener("submit", function(event) {
    event.preventDefault();
    console.log("Form submission prevented.");
});
```

---

## Practice Example

```javascript
const btn = document.getElementById("btn");

btn.addEventListener("click", () => {
    btn.textContent = "Clicked!";
});
```

---

## Key Learnings

* Learned different types of JavaScript functions.
* Understood parameters, arguments, and return values.
* Practiced callback functions and variable scope.
* Learned how JavaScript responds to browser events.
* Used `addEventListener()` to handle user interactions.
* Understood the event object and `preventDefault()`.

---

# JavaScript Objects & Arrays

## Objects

Objects store related data as **key-value pairs**.

They are commonly used to represent real-world entities such as users, products, and employees.

```javascript
const student = {
    name: "Rahul",
    age: 18
};
```

---

## Access Object Properties

### Dot Notation

```javascript
student.name;
```

### Bracket Notation

```javascript
student["age"];
```

---

## Add, Update & Delete Properties

### Add Property

```javascript
student.city = "Delhi";
```

### Update Property

```javascript
student.age = 19;
```

### Delete Property

```javascript
delete student.city;
```

---

## Object Methods

A **method** is a function defined inside an object.

The `this` keyword refers to the **current object**.

```javascript
const student = {
    name: "Rahul",

    greet() {
        console.log(`Hello, ${this.name}`);
    }
};

student.greet();
```

---

## Useful Object Methods

| Method             | Purpose                 |
| ------------------ | ----------------------- |
| `Object.keys()`    | Returns all keys        |
| `Object.values()`  | Returns all values      |
| `Object.entries()` | Returns key-value pairs |

Example:

```javascript
const student = {
    name: "Rahul",
    age: 18
};

console.log(Object.keys(student));
console.log(Object.values(student));
console.log(Object.entries(student));
```

---

# Arrays

Arrays store multiple values in an **ordered collection**.

Real-world data often comes as **arrays of objects**.

```javascript
const products = [
    { id: 1, name: "Laptop", price: 65000 },
    { id: 2, name: "Mouse", price: 500 }
];
```

---

## Array Methods

| Method      | Purpose                             |
| ----------- | ----------------------------------- |
| `forEach()` | Runs code for every item            |
| `map()`     | Creates a new array                 |
| `filter()`  | Keeps matching items                |
| `find()`    | Returns the first matching item     |
| `some()`    | Returns `true` if any item matches  |
| `every()`   | Returns `true` if all items match   |
| `sort()`    | Sorts the array                     |
| `reduce()`  | Reduces the array to a single value |

---

## Examples of Array Methods

### `forEach()`

Runs a function for every element.

```javascript
const numbers = [1, 2, 3];

numbers.forEach(num => {
    console.log(num);
});
```

---

### `map()`

Creates a **new array** by transforming every element.

```javascript
const numbers = [1, 2, 3];

const doubled = numbers.map(num => num * 2);

console.log(doubled);
```

Output:

```text
[2, 4, 6]
```

---

### `filter()`

Creates a new array containing only elements that satisfy a condition.

```javascript
const numbers = [10, 15, 20, 25];

const result = numbers.filter(num => num > 15);

console.log(result);
```

Output:

```text
[20, 25]
```

---

### `find()`

Returns the **first element** that satisfies a condition.

```javascript
const numbers = [10, 15, 20, 25];

const result = numbers.find(num => num > 15);

console.log(result);
```

Output:

```text
20
```

---

### `some()`

Returns `true` if **at least one** element satisfies the condition.

```javascript
const numbers = [10, 15, 20];

console.log(numbers.some(num => num > 18));
```

Output:

```text
true
```

---

### `every()`

Returns `true` if **all** elements satisfy the condition.

```javascript
const numbers = [10, 20, 30];

console.log(numbers.every(num => num > 5));
```

Output:

```text
true
```

---

### `reduce()`

Reduces all elements into a **single value**.

```javascript
const numbers = [10, 20, 30];

const total = numbers.reduce((sum, num) => sum + num, 0);

console.log(total);
```

Output:

```text
60
```

---

## Quick Revision

* **Object** → Key-value pairs
* **Array** → Ordered collection
* **`this`** → Refers to the current object
* **`Object.keys()`** → Returns keys
* **`Object.values()`** → Returns values
* **`Object.entries()`** → Returns key-value pairs
* **`forEach()`** → Runs code for each item
* **`map()`** → Creates a new transformed array
* **`filter()`** → Keeps matching items
* **`find()`** → Returns the first matching item
* **`reduce()`** → Reduces array to one value
* **`some()`** → Checks if any item matches
* **`every()`** → Checks if all items match
* **`sort()`** → Sorts items

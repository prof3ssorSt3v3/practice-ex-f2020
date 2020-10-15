# List of Practice Exercises for PA open lab sessions

## Datatypes

1. Create an Object with a series of X properties. Each property has a value that is a different type: String, Boolean, Number, null, undefined, Array, Object, and function. Assign the object to a `const`.

## Functions

1. Take the first datatype exercise and add code inside the function property to `return` the value of one of the other properties. Below the object, call the function property and assign the returned value to a new variable. Then console.log the returned value.
2. Create three functions that console log a message. Make one a function declaration, one a function expression, and the third a function expression with an arrow function.
3. Create a function that accepts a string parameter and a number parameter and then outputs the string the number of times specified by the number parameter.
4. Create a function that calculates tax and tip on a number that is passed to the function. The function accepts three numbers. The first parameter is a subtotal number. The second is a tax percentage to use. The third is a percentage to use to calculate the tip. The function will calculate the amount of the tax based on the first two parameters, then add the subtotal to the tax amount. Next multiply the total of the tax and subtotal by the tip percentage and add that total with the previous. The tip is being calculated on the after tax amount. Output these three values - subtotal, total with tax, and total with tax and tip.
5. Fix the scope / hoisting problems in this code with the fewest changes possible:

```js
init();
let init = function () {
  output();
};
let output = function () {
  console.log(NAME);
};
const NAME = 'Gandalf';
```

6. Take this code and re-write it as an IIFE that will run the init function when `DOMContentLoaded` happens.

```js
const APP = {
  name: 'EnviroApp',
  clicks: 0,
  init: function () {
    document.body.addEventListener('click', APP.addClick);
  },
  addClick: function () {
    APP.clicks++;
    APP.output();
  },
  output: function () {
    console.log(`${APP.clicks} clicks so far`);
  },
};

document.addEventListener('DOMContentLoaded', APP.init);
```

## Arrays

1. Create an Array literal with 4 names. Create a function that accepts one parameter - an Array. The function needs to loop through the values in the Array and return a new Array where all the names have been capitalized. There are many ways to solve this. Call the function and pass in the name of arrays. `console.log()` the return value from the function.
2. Create 2 Array literals, one with a bunch of names, one with a bunch of numbers greater than 100. Write a function that will accept an array as its one parameter and sort the Array. Make sure that the number array is being sorted numerically and the names are being sorted alphabetically.
3. Create an empty Array. Use the `push()` method to add a series of 3 `Date` objects to the Array. Write a function that will sort the date array so that the dates appear in the same order that they appear during the year. Eg: January dates first, then February, then March... and so on.
4. Create an Array with 8 numbers between 1 and 100. Use the filter method to generate a new Array that only contains the numbers from the original Array that are greater than 50.

## Numbers

1. Create a function that accepts a number and then uses an `if else` statement and the `modulus` operator to determine and output whether a number is odd or even.
2. Create a function that accepts a number and then uses the `toString` method to convert the number from a typical base-10 number into its hexidecimal equivalent.

## Strings

1. Create a variable that holds a bunch of Lorem Ipsum text. Write a function that will accept two string parameters. The first will be the string to look through. The second is the thing to look for. The function needs to return the number of times the second string appears in the first string.
2. Create a variable that holds a string. Write a function that accepts the string and returns the same string backwards.
3. Create a function that accepts a string and then builds a new string made from every second letter in the string.
4. Create a function that accepts a single number parameter and then outputs a new version of that number as a string. The number needs to be converted to a string using the `toString` method. Next, the length of the string needs to be 25 characters or more. If the string's length is less than 25 characters then use the string `padStart` method to add extra `0`s in front.

## Loops

1. Start with the code below as an example. Create new versions of this code that give the exact same output with a `for in` loop, a `for of` loop, a `do while` loop, a `while` loop, and the Array `forEach` method.

```js
let places = [
  'Ottawa',
  'Toronto',
  'Vancouver',
  'Winnipeg',
  'Edmonton',
  'Calgary',
  'Halifax',
];
for (let num = 0, len = places.length; num < len; num++) {
  console.log(places[num].toLocaleUpperCase('en-CA'));
}
```

2. Create an object with 4 different properties. Create a `for in` loop that will output both the name and value of each property in the object.

## Control Flow

1. Create a `function` which accepts a number parameter. The function needs to contains an `if statement` that will output three different messages depending on whether the number parameter value is:

- less than 100
- between 100 and 999 inclusive
- greater or equal to 1000

2. Create a new version of the control flow exercise 1 that uses nested ternary operators.

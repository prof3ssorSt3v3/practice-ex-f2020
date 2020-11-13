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
5. Explain what this function does and what the output will be:

```js
function monkeyCount(n) {
  return Array.from({ length: n }, (_, i) => i + 1);
}
```

6. Create an Array with 5 strings and then use the `map` method to generate a new version of the Array where only the last letter of each string is capitalized.
7. Create a String that holds a sentence. Use the `split` method to convert the String into an Array of individual letters and chain on the `forEach` method. The `forEach`'s function will `console.log` each letter BUT alternate between uppercase and lowercase.
8. Create an Array of integers and then use the `map` method to loop through the Array and create a new version of the Array where each integer is the hexadecimal version. eg: 15 becomes F. `Hint: look at Numbers exercise 2`

## Numbers

1. Create a function that accepts a number and then uses an `if else` statement and the `modulus` operator to determine and output whether a number is odd or even.
2. Create a function that accepts a number and then uses the `toString` method to convert the number from a typical base-10 number into its hexadecimal equivalent.
3. Create a function that accepts two numbers, converts the numbers to integers, determines which is the bigger and which is the smaller integer, and then returns a random integer that is between those two numbers inclusively.

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
3. Create nested loops that will loop through the objects in this array and output all the property names and values.

```js
const students = [
  { num: 456, name: 'Anoop', program: 'Advanced Beginning' },
  { num: 654, name: 'Mariana', program: 'Beginning for Intermediates' },
  { num: 564, name: 'Manuel', program: 'Advanced Introductory' },
  {
    num: 645,
    name: 'Aiden',
    program: 'Intermediate Introduction to Beginning Advanced',
  },
];
```

## Control Flow

1. Create a `function` which accepts a number parameter. The function needs to contains an `if statement` that will output three different messages depending on whether the number parameter value is:

- less than 100
- between 100 and 999 inclusive
- greater or equal to 1000

2. Create a new version of the control flow exercise 1 that uses nested ternary operators.
3. Create a `switch..case` statement that checks the value of a positive numeric variable that outputs one of three things:

- "Between 0 and 3"
- "Between 4 and 6"
- "Greater than 6"

## DOM & Events

1. Use this provided array of objects:

```js
let data = [
  { id: 14, name: 'Ricky', email: 'winner@nascar.org' },
  { id: 34, name: 'Doctor', email: 'immortal@tardis.org' },
  { id: 54, name: 'Chandler', email: 'c.bing@friends.org' },
];
```

Write a script that will generate the following `card` for each object in the array and add them to the page.

```html
<div class="card" data-id="id goes here">
  <h2 class="name">The name here</h2>
  <p class="email">sample@email.address</p>
</div>
```

Once they are created create some CSS for the cards and their content to make them look like cards.

2. Start with this HTML on your page:

```html
<section class="cards">
  <div class="card" data-id="34">
    <h2 class="name">Chandler Bing</h2>
    <p class="email">c.bing@friends.org</p>
    <p><a href="#">Read More...</a></p>
  </div>
  <div class="card" data-id="77">
    <h2 class="name">Rachel Green</h2>
    <p class="email">r.green@friends.org</p>
    <p><a href="#">Read More...</a></p>
  </div>
  <div class="card" data-id="15">
    <h2 class="name">Joey Tribianni</h2>
    <p class="email">j.tribianni@friends.org</p>
    <p><a href="#">Read More...</a></p>
  </div>
</section>
<section class="output">
  <p><span>You Selected:</span></p>
</section>
```

Add a single click listener to `section.cards` which calls a function that will:

- determine which card was clicked or IF a card was clicked. Try using the `closest()` method to find the card.
- If a card was clicked `console.log` the id from `data-id` and put the value from `name` inside the `.output` section, in the paragraph.
- Make sure that you don't delete the `span` when adding the name.

3. Create a webpage with four or more paragraphs and a button. Put a different name inside each paragraph and give the paragraphs a default background colour to show where they can be clicked.

In the CSS create a default style for the paragraphs and a class called `highlight` that has a bright background color.

Add a click listener to the `body` AND a second click listener to the button.

In the body's click function check that the user clicked a paragraph. If they did click a paragraph then: add the `highlight` CSS class which will change the background; and add the reference to the paragraph to a global array.

In the button's click function loop through all the elements in the global array with `forEach`. Remove the `highlight` class from each element in the array.

4. Start with your solution for `Hybrid 9 - DOM Manipulation`, which is the one that toggles the text of each paragraph between upper and lower case as the user mouses over and out of each paragraph. Change the solution so that the original words with capital letters get them back when the user mouses out from each paragraph.

# Program structure

## Expressions and statements

A fragment of code that produces a value is called an expression:
```js
22
'psychoanalysis'
```
A statement perfoms an action:
```js
alert('Warning!');
```

Statements can display something on the screen—that counts as changing the world—or it could change the internal state of the machine in a way that will affect the statements that come after it. These changes are called *side effects*. 

## Variables

```js
var caught = 5 * 5;
```

```js
// good variable names
a
a1 // can contain numbers
_a // can contain the underscore
$a // and the dollar sign

// bad variable names
1a // shouldn't start with numbers
if // shouldn't be a reserved word
```

Reassign values
```js
var mood = "light";
console.log(mood);
// → light
mood = "dark";
console.log(mood);
// → dark
```

```js
var b;
console.log(b); // → undefined;
```

```js
var one = 1, two = 2; // define multiple variables
console.log(one + two); // → 3
```

## Keywords and reserved words

```
break case catch class const continue debugger
default delete do else enum export extends false
finally for function if implements import in
instanceof interface let new null package private
protected public return static super switch this
throw true try typeof var void while with yield
```

## The environment

The collection of variables and their values that exist at a given time is called *the environment*.

## Functions

```js
alert("Good morning!");
```
```js
var x = 30;
console.log("the value of x is", x); // → the value of x is 30
```

### Return values

```js
console.log(Math.max(2, 4)); // → 4
Math.max(2, 4); // doesn't produce side effects, it retuns a computed value
console.log(); // produces a side effect
```

### Prompt and confirm

```js
confirm("Shall we, then?");
prompt("Tell me everything you know.", "...");
```

## Control flow

```js
// The statements are executed, predictably, from top to bottom
var theNumber = Number(prompt("Pick a number", ""));
alert("Your number is the square root of " +
      theNumber * theNumber);
```

### Conditional execution

`if` statement:
```js
var theNumber = Number(prompt("Pick a number", ""));
if (!isNaN(theNumber))
  alert("Your number is the square root of " +
        theNumber * theNumber);
```

`if else` statement:
```js
var theNumber = Number(prompt("Pick a number", ""));
if (!isNaN(theNumber))
  alert("Your number is the square root of " +
        theNumber * theNumber);
else
  alert("Hey. Why didn't you give me a number?");
```

Chain `if` statements:
```js
var num = Number(prompt("Pick a number", "0"));

if (num < 10)
  alert("Small");
else if (num < 100)
  alert("Medium");
else
  alert("Large");
```

### while and do loops

`while`:
```js
var number = 0;
while (number <= 12) {
  console.log(number);
  number = number + 2;
}
// → 0
// → 2
//   … etcetera
```

`do`:
```js
// A do loop always executes its body at least once
do {
  var yourName = prompt("Who are you?");
} while (!yourName);
console.log(yourName);
```

### Indenting Code

The role of the indentation inside blocks is to make the structure of the code stand out.

### For loops

```js
for (var number = 0; number <= 12; number = number + 2)
  console.log(number);
// → 0
// → 2
//   … etcetera
```

### Breaking Out of a Loop

```js
for (var current = 20; ; current++) {
  if (current % 7 == 0)
    break;
}
console.log(current);
// → 21
```

```js
for (var i = 0; i < 10; i++) {
  if (i % 2 == 0) continue;
  alert(i);
}
```

## Updating variables succinctly

```js
counter = counter + 1;
counter += 1; // shortcut for the previous example
```

```js
result *= 2;
counter -= 1;
counter++; // even shorter equvivalents
counter--;
```

### i++ vs ++i

```js
var i = 1;
console.log(i++); // → 1
console.log(i); // → 2
i = 1;
console.log(++i); // → 2
console.log(i); // → 2
```

## Dispatching on a value with switch

```js
switch (prompt("What is the weather like?")) {
  case "rainy":
    console.log("Remember to bring an umbrella.");
    break;
  case "sunny":
    console.log("Dress lightly.");
  case "cloudy":
    console.log("Go outside.");
    break;
  default:
    console.log("Unknown weather type!");
    break;
}
```

## Capitalization

```js
fuzzylittleturtle
fuzzy_little_turtle
FuzzyLittleTurtle
fuzzyLittleTurtle
```

## Comments

```js
var accountBalance = calculateBalance(account);
// It's a green hollow where a river sings
accountBalance.adjust();
// Madly catching white tatters in the grass.
var report = new Report();
// Where the sun on the proud mountain rings:
addToReport(accountBalance, report);
// It's a little valley, foaming like light in a glass.

/*
 I first found this number scrawled on the back of one of
 my notebooks a few years ago. Since then, it has often
 dropped by, showing up in phone numbers and the serial
 numbers of products that I've bought. It obviously likes
 me, so I've decided to keep it.
*/
var myNumber = 11213;
```

## Summary

You now know that a program is built out of statements, which themselves sometimes contain more statements. Statements tend to contain expressions, which themselves can be built out of smaller expressions.

Putting statements after one another gives you a program that is executed from top to bottom. You can introduce disturbances in the flow of control by using conditional (if, else, and switch) and looping (while, do, and for) statements.

Variables can be used to file pieces of data under a name, and they are useful for tracking state in your program. The environment is the set of variables that are defined. JavaScript systems always put a number of useful standard variables into your environment.

Functions are special values that encapsulate a piece of program. You can invoke them by writing functionName(argument1, argument2). Such a function call is an expression, and may produce a value.

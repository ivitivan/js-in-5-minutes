# Values, Types, and Operators

## Bits

## Values

Bits are diffucult to read for humans. Programming languages use human readable values. In JavaScript, they are numbers, strings, Booleans, objects, functions, and undefined values.

### Numbers

```js
13
9.81
```

#### Fractional numbers are not precise

For example,

```js
var x = 0.3 - 0.2;
var y = 0.2 - 0.1;
x == y // → false;
```

#### Arithmetic

```js
100 + 4 * 11
(100 + 4) * 11 // use parentheses to change the order of operations
100 - 4 // substraction
100/4 // division
99 % 4 // → 3, remainder
```

#### Special numbers

```js
Infinity
-Infinity
NaN
```

## Strings

```js
"Patch my boat with chewing gum" // double quotes
'Monkeys wave goodbye' // single quotes
'String "5"' // double quotes inside single quotes
"String '5'" // single quotes inside double quotes
"This is the first line\nAnd this is the second" // escaping characters
```
```js
"con" + "cat" + "e" + "nate" // string concatenation
```

## Unary operators

```js
typeof 4.5 // →  'number'
typeof 'x' // → 'string'
-10 // minus can be used as uniry and binary operator
```

## Boolean values

```js
console.log(3 > 2) // → true
console.log(3 < 2) // → false
```

```js
console.log("Aardvark" < "Zoroaster") // → true
```

```js
>= // → greater than or equal to
<= // → less than or equal to
== // equal to
!= // not equal to
```

```js
console.log("Itchy" != "Scratchy") // → true
```

```js
console.log(NaN == NaN) // → false
```

## Logical operators

```js
console.log(true && false) // → false
console.log(true && true) // → true
```

```js
console.log(false || true) // → true
console.log(false || false) // → false
```

```js
console.log(!true) // → false
```

```js
console.log(true ? 1 : 2); // → 1
console.log(false ? 1 : 2); // → 2
```

## Undefined values

`null`, `undefined`

## Automatic type conversion

```js
console.log(8 * null) // → 0
console.log("5" - 1) // → 4
console.log("5" + 1) // → 51
console.log("five" * 2) // → NaN
console.log(false == 0) // → true
console.log(null == undefined); // → true
console.log(null == 0); // → false
```

### Short-circuiting of logical operators

```js
console.log(null || "user") // → user
console.log("Karl" || "user") // → Karl
```

```js
console.log(false && 2) // → false
console.log(true && 2) // → 2
```

# Summary

Types: `numbers`, `strings`, `Booleans`, and `undefined` values.

Operators: 
- arithmetic: `+`, `-`, `*`, `/`, and `%`
- string concatenation: `+`
- comparison: `==`, `!=`, `===`, `!==`, `<`, `>`, `<=`, `>=`
- logic: `&&`, `||`
- unary: `-`, `!`, `typeof`
- ternary: `?:`

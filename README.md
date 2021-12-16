# What is JavaScript Standard Style

The JavaScript Standard Style is a series of rules for how code should be structured in JavaScript.

## Why should I follow the standard JavaScript style?

Considering the corporate collective work in programming, a code you create will be used by other members of your team, so that the code is cleaner the JavaScript Standard Style standardizes the way it is written, facilitating maintenance and interpretation by other people.

## Rules

### 1. Use 2 spaces

For information contained within a scope, it is necessary to indent two spaces as in the example below:

```js
const getFirstUser = (array) => {
  if (array[0]) {
		return array[0]
	} else {
		return 'this array has no first element'
	}
}
```

As you can see I used two spaces both to define the if inside the function and the function returns inside the if and else.

### 2. Strings with single quotes

Strings with single or double quotes are identified equally by JavaScript, but for better organization Standard indicates that you use single quotes for a string by standardizing the API code as a whole.

```js
const string = 'i am a string'

const index = require('./index.js')

switch (expression) {

	case '1':

	break

	case '2':

	break
}
```

As you can see, everywhere I used a string I enclosed it in single quotes.

The only situation you should opt for double quotes is when you need to escape.

```js
const string = "this is a string 'string'"
```

This is necessary for the quotes to be visible.

### 3. Don't leave unused algorithms in the code.

When creating your codes, do not leave variables and algorithms declared that will not be used, because when running the server will reserve a space in memory for this that will never be used.

```js
const apple = 'apple'
const orange = 'orange'
const melon = 'melon' //Never Used
const fruits = []

fruits.push(apple)
fruits.push(orange)
```

As you can see inside the fruits array the string apple and orange is pulled, but the melon is never used in this code.

### 4. Space between method statements

When declaring any method, if/else, while, for and after braces, use a space. This allows the code to have greater readability and standardization.

```js
if (condition) {
	// ...	
 }

for (let i = 0; i === j; i++) {
	// ...
}

function functionJs () {
	// ...
}
```

### 5. Equality Operators

When using a comparison of equality or inequality, don't use it with two characters but with three, for example, don't use == in a comparison, use ===, don't use != use !==

**Why does this happen?**

When you use a double term in an equality like comparing 1 == '1' it will convert your 1 number to a string, increasing the weight of the comparison, but as most of the times we want to compare if the value is absolutely equal we should use the === this is instructed by the standard to avoid unnecessary calculations.

It depends on the situation obviously, if you want to compare an object to see if it is null or if it is undefined you use it with two characters, because the comparison to get something null or undefined must be based on relative and not absolute.

```js
const number = 1

if (1 === number) {
	// ...
}

if (number !== 2) {
	// ...
}

number === 1 ? 1 : null
```

### 6. Infix operators

The infix operators are those characters or algorithms that are between something, that is, when declaring a variable, constant and the like, use a space between the equality statement and what it contains.

This rule also validates for spacing between strings and concatenations.

```js
const x = 1
// Note the space between const, x and 1

const string = 'String'

const concatenatedString = 'I am a' + string + 'concatenated'
// Always a space between the join
```

### 7. Spaces after commas

Whenever you use commas, whether in argument, in a string or elsewhere, include a space after the comma for better readability and understanding.

```js
const array = [1, 2, 3, 4, 5]

const arrowFunction = (arg1, arg2) => {
	//...
}
```

### 8. Use of else

When using if/else, when opening the else's scope, declare it on the same line as the if closing but with a space between the closing and the else and a space after the else to open its scope.

```js
if (condition) {
	// ...
} else {
	// ...
}
```

### 9. Use of if

When using the if, if what is contained in it has more than one line, open curly braces to wrap, however it fits in the same line, you can use it sequentially.

```js
if (condition) //small code

if (condition) {
	// large code
}
```

### 10. Error handling

When your function has an error take an approach to handling the error, this is important not only for formatting but also to prevent your server from malfunctioning as an unhandled error can crash your code.

```js
try {
	function () {
		//...
	}

} catch (err) {
	console.log(err)
}
```

The try/catch is just one of the ways to deal with an error, there are others that can be manual like throw new error, or the catch of a then, the important thing is that the error is already handled.

### 10. Not have multiple null lines

Essa regra vem das normas do livro "Clean Code" e ela refere-se a um código que possui mais do que uma linha em branco e isso torna o codigo mal otimizado.

```js
const number = 1

const string = 'string'

//one space only, between the codes
```

### 11. Ternary operator

Quando for utilizar o ternary, se possivel utilize-o em apenas uma linha, porém se o código for maior, separe a condição do "?" e também ":" em suas proprias linhas.

```js
object === objectTwo ? 'yes' : 'no' //Small code

object === objectTwo // Large code 
? 'yes'
: 'no'
```

### 12. Variable declarations

When declaring more than one variable, declare them separately, as JavaScript allows the declaration of two variables as.

```js
var element = 1, object = {}
```

But the Standard recommends declaring them individually.

```js
var element = 1

var object = {}
```

### 13. Parentheses in definitions

When changing the definition of something within a scope, use parentheses to enclose it, so it's clearer that it's an "=" declaration expression and not an equity "===".

```js
let element

while (element = 1) {
  // ...
}
```

### 14. Semicolon at the end of the line

When you finish the line of your code there is no need to insert a semicolon, because in JavaScript this interpretation is done automatically by where the code is being read, whether by browser or by the server itself.

```js
var object = {}
//correct

var object = {};
//wrong
```

### 15. Start of line

When to start a line of code never start with (, [or `, in case you need to use something because of the escape use ";".

```js
;(function () {
}())

;[1, 2, 3].forEach(bar)

;`String`.indexOf(0)
``` 
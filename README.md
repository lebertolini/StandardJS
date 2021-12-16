# What is JavaScript Standard Style

The JavaScript Standard Style is a series of rules for how code should be structured in JavaScript.

## Why should I follow the standard JavaScript style?

Considering the corporate collective work in programming, a code you create will be used by other members of your team, so that the code is cleaner the JavaScript Standard Style standardizes the way it is written, facilitating maintenance and interpretation by other people.

## Regras

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

### 2. # StandardJS

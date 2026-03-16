# ![Chiang Rai International School](../images/logo.png?raw=true) Introduction to JavaScript

## Arrays and Loops

### Arrays

An array is a list of values.

Example:

```js
let studentHeights = [155, 162, 158, 176, 176, 186, 175, 168, 164, 163];
```

This array stores student heights in centimeters.

### Indexes

Each value has an index.

Indexes start at `0`.

```text
index:   0    1    2    3    4    5    6    7    8    9
value: 155  162  158  176  176  186  175  168  164  163
```

### Get One Value

Use square brackets `[]`.

```js
let studentHeights = [155, 162, 158, 176, 176, 186, 175, 168, 164, 163];

let pollysHeight = studentHeights[0];
let tommysHeight = studentHeights[4];

console.log("Polly's height", pollysHeight);
console.log("Tommy's height", tommysHeight);
```

Output:

```text
Polly's height 155
Tommy's height 176
```

### Bad Index

What if the index is too big?

```js
let joesHeight = studentHeights[10];
console.log("Joe's height", joesHeight);
```

Output:

```text
Joe's height undefined
```

Why?

- The last index is `9`
- There is no value at index `10`
- JavaScript gives `undefined`

### Length

Use `.length` to get the number of values.

```js
console.log("number students:", studentHeights.length);
```

Output:

```text
number students: 10
```

Important:

- `length` is the number of values
- The last index is `length - 1`

### Loops

A loop repeats code.

Use a `for` loop to visit every value in the array.

```js
for (let i = 0; i <= studentHeights.length - 1; i++) {
  let value = studentHeights[i];
  console.log("student: " + i, value);
}
```

This loop does three things:

- Start with `i = 0`
- Keep going while `i <= studentHeights.length - 1`
- Add `1` each time

### Full Example

```js
// student height (cm)

// indexes:             0    1    2    3    4    5    6    7    8    9
let studentHeights = [155, 162, 158, 176, 176, 186, 175, 168, 164, 163];

let pollysHeight = studentHeights[0];
let tommysHeight = studentHeights[4];

console.log("Polly's height", pollysHeight);
console.log("Tommy's height", tommysHeight);
console.log("number students:", studentHeights.length);

for (let i = 0; i <= studentHeights.length - 1; i++) {
  let value = studentHeights[i];
  console.log("student: " + i, value);
}
```

### Rules to Remember

- An array is a list
- Indexes start at `0`
- Use `array[index]` to get one value
- Use `.length` to get the number of values
- Use a loop to visit every value

### References

- [Indexed collections](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Indexed_collections)
- [Array length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length)
- [for statement](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)

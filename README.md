babel-plugin-transform-console-log-variable-names
-------------------------------------------------

__WARNING: Very very alpha code quality__

Everytime I try to `console.log` a variable's value, I forget to label
the variable and so the logged statements become unuseful and confusing,
especially when used inside a loop—case in point: React's `render`
function, or `componentWillReceiveProps`.


This plugin transforms `console.log` statements that have just variable
labels as arguments and prepends a string that specifies what those
labels are. For example, for the following statements:

```javascript

const a = 12;
const b = 13;
const c = 59;

console.log(a);
console.log(a, b);
console.log(a, b, c);
```

The output would look something like:


```
a: 12
a, b: 12 13
a, b, c: 12, 13, 59
```
# Named Export vs Default Export in ES

In ECMAScript 6 (ES6) and later versions, modules are used to organize and share code between different JavaScript files. Two common ways to export functionality from a module are named exports and default exports. They serve different purposes and have slightly different syntaxes. Let's explore them in detail.

1. Named Export:
   Named exports allow us to export multiple functions, variables, or objects from a module by explicitly specifying their names. This means that we can selectively choose which elements to export and import individually in other files.

Here's an example of exporting multiple functions using named exports:

```javascript
// math.js
export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}
```

To import the named exports in another file, we need to use their exact names:

```javascript
// app.js
import { add, subtract } from "./math.js";

console.log(add(5, 3)); // Output: 8
console.log(subtract(5, 3)); // Output: 2
```

We can also use the `as` keyword to rename named exports during import:

```javascript
// app.js
import { add as sum, subtract as sub } from "./math.js";

console.log(sum(5, 3)); // Output: 8
console.log(sub(5, 3)); // Output: 2
```

Named exports provide explicit control over the imported elements and allow for better organization of exported functionality.

2. Default Export:
   Default exports allow us to export a single function, class, or object as the default export from a module. Unlike named exports, default exports are typically used when a module wants to expose a primary functionality or a single entity.

Here's an example of exporting a default function:

```javascript
// math.js
export default function multiply(a, b) {
  return a * b;
}
```

When importing a default export, we can choose any name we prefer:

```javascript
// app.js
import multiply from "./math.js";

console.log(multiply(5, 3)); // Output: 15
```

Note that there can only be one default export per module. If a module has a default export, it can be imported without using braces `{}`.

```javascript
// app.js
import myFunction from "./myModule.js";
```

In summary, named exports are used when we want to export multiple functions or variables from a module, while default exports are used when we want to export a single function, class, or object as the primary export. Both approaches provide flexibility in organizing and sharing code across JavaScript files based on the specific needs of the module.

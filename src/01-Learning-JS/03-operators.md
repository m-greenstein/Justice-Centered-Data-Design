# 1.3 Operators

## Start Your GH Workflow

Remember, before you start anything else, always follow this GH methodological workflow:

1. Create meaningful **branch** that uses the agreed upon naming scheme: `CHP/X.x--lastname`.
2. Practice the iterative process to **commit** and **push** regularly with meaningful **commit messages**.

## Overview

Operators. What are they? You already know the basics–just think back to your math classes.

- `+` -- Add
- `-` -- Subtract
- `*` -- Multiply
- `/` -- Divide
- `>` -- Greater than
- ...

In JS, and many other languages, these symbols operate similarly. Yet, they also differ and change sometimes depending on the data types and functional context of your code.

Overall, operators help you perform lots of desired actions, so let's dig into them and start learning more interesting coding techniques!

## 1.3.1 Assignment Operators

Assignment operators denote the assignment of a value in a **right(*value*)-to-left(*variable*) direction**: `let variableName = 42`.

There are lots of assignment operators, but below is an abridged table of some. For now, the equals sign operator `=` is what you should know and understand.

<table>
  <thead>
    <tr>
      <th>Assignment Operator</th>
      <th>Description</th>
      <th>Example</th>
      <th>Result</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><code>=</code></td><td>Equality </td>
      <td><code>let a = 5, b = 10;</code><br><code>b = a;</code></td>
      <td>b = 5</td>
    </tr>
    <tr><td><code>+=</code></td><td>Shorthand Addition </td>
      <td><code>let a = 5, b = 10;</code><br><code>b += a;</code></td>
      <td>b = 15</td>
    </tr>
    <tr><td><code>-=</code></td><td>Shorthand Subtraction </td>
      <td><code>let a = 5, b = 10;</code><br><code>b -= a;</code></td>
      <td>b = 5</td>
    </tr>
  <tr><td><code>*=</code></td><td>Shorthand Multiplication </td>
      <td><code>let a = 5, b = 10;</code><br><code>b *= a;</code></td>
      <td>b = 50</td>
    </tr>
    <tr><td><code>/=</code></td><td>Shorthand Division </td>
      <td><code>let a = 5, b = 10;</code><br><code>b /= a;</code></td>
      <td>b = 2</td>
    </tr>
  </tbody>
</table>

## 1.3.2 Basic Arithmetic Operators

Arithmetic operators return a single numerical value from other numerical literals or variables.

<table>
  <thead>
    <tr>
      <th>Operator</th>
      <th>Description</th>
      <th>Example</th>
      <th>Result</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>+</code></td><td>Addition</td>
      <td><code>let a = 10 + 5;</code><br><code>let a = 10 + '5';</code></td>
      <td><code>a = 15</code><br><code>a = 105</code> (string concatenation)</td>
    </tr>
    <tr>
      <td><code>-</code></td><td>Subtraction</td>
      <td><code>let a = 10 - '5';</code></td>
      <td><code>a = 5</code></td>
    </tr>
    <tr>
      <td><code>*</code></td><td> Mutiplication</td>
      <td><code>let a = 10 * '5';</code></td>
      <td><code>a = 50</code></td>
    </tr>
    <tr>
      <td><code>/</code></td><td>Division</td>
      <td><code>let a = 10 / '5';</code></td>
      <td><code>a = 2</code></td>
    </tr>
    <tr>
      <td><code>%</code></td><td>Modulus</td>
      <td><code>let a = 10 % '5';</code><br><code>let a = 12 % '5';</code></td>
      <td><code>a = 0</code> (integer remainder)<br><code>a = 2</code> (integer remainder)</td>
    </tr>
  </tbody>
</table>

### WATCH OUT! Numbers and the `+` operator

In expressions involving numeric and string values with the `+` operator, JavaScript converts numeric values to strings.
  - **Example**:
    ```javascript
    let x = "The answer is " + 42; // "The answer is 42"
    let y = 42 + " is the answer"; // "42 is the answer"
    let z = "37" + 7; // "377"
    ```

JS does ***not*** convert numeric values to strings, when using any other operator.
  - **Example**:
    ```javascript
    "37" - 7; // 30
    "37" * 7; // 259
    ```

## 1.3.3 Comparison Operators

Sometimes we need to compare values in our project. Comparison operators allow us to compare variables, whether numbers or strings, so we can yield `true` or `false` Boolean values.

<p class="tip">Open your console and try them out by using some of the examples below.</p>

<video controls style="width: 620px; height:620px">
  <source src="../assets/vids/01-js/01.3-operators-console.mp4" type="video/mp4" />
</video>

- **`==` Is Equal To**
    ```javascript
    // Yields Boolean true
    12 == 12

    // Yields Boolean false
    12 == 10
    ```
- **`!=` Is Not Equal To**
    ```javascript
    // Yields Boolean false
    12 != 12

    // Yields Boolean true
    12 != 10
    ```
- **`<` Is Less Than**
    ```javascript
    // Yields Boolean false
    12 < 12

    // Yields Boolean false
    12 < 10
    ```
- **`<=` Is Less Than or Equal To**
    ```javascript
    // Yields Boolean true
    12 <= 12

    // Yields Boolean false
    12 <= 10
    ```
- **`>` Is Greater Than**
    ```javascript
    // Yields Boolean false
    12 > 12

    // Yields Boolean true
    12 > 10
    ```
- **`>=` Is Greater Than or Equal to**
    ```javascript
    // Yields Boolean true
    12 <= 12

    // Yields Boolean true
    12 <= 10
    ```

## 1.3.4 AND`&&` and OR `||` Operators

Finally, for now, it will be good to learn about conjunction operators like AND`&&` and OR `||`.

These two help you build expressions by combining multiple comparisons, which we will practice more in the next chapter on **Conditionals**.

- **`&&` AND**
    ```javascript
    // Yields Boolean false
    12 == 12 && 10 == 12

    // Yields Boolean true
    12 == 12 && 10 == 10
    ```
- **`||` OR**
    ```javascript
    // Yields Boolean true
    12 == 12 || 10 == 12

    // Yields Boolean true
    12 == 12 || 10 == 10
    ```

## E1. Create a Suite of Variables Evaluated by Operators

Create your own suite of operators that evaluate a suite of variables.

First, go back to the last chapter and grab the suite of primitives that you created as a starting point. Feel free to add more variables, as needed to practice writing operators with any combination of those variables.

1. Convert the `javascript` codeblock to an executable block with the `js`.
2. Declare and initialize your own suite of variables. As mentioned above, feel free to grab the variables used in the prior chapter.
3. Declare and initialize your own suite of operators.
   <p class="note">Have fun with it! Choose a theme like your favorite movie, story, hobby, etc.</p>
4. Print them all to the console with `console.log()`.
5. Check your work, as you go, by opening the browser console with the **Inspect Element** tool.

```js
// Write your code in here

let band = "All Time Low"

const year = 2003

let booleanHappy = true
let booleanSad = false

let null = "Boo!"

let undefined
console.log(undefined)

let goodSongs = {
  neverland: "Somewhere in Neverland",
  maria: "Dear Maria, Count Me In",
}

let bandYear = band + " was founded in " + year + "."
// All Time Low was founded in 2003.
```

## Submission

1. Create a **PR** (**pull request**) and use the provided content in the template to start it.
2. No peer responses are due for this chapter.
3. Submit the PR link in Moodle, when you're ready.

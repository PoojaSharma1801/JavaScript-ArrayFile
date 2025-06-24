# 📊 JavaScript Array Utility – `first()` Function

This project demonstrates a JavaScript utility function named `first()` that returns the first element(s) of an array.

---

## 📄 Description

The `first()` function behaves as follows:
- Returns the first element if no `n` is passed.
- Returns the first `n` elements if `n` is provided and positive.
- Returns an empty array if the input array is empty or `n` is negative.

---

## 📂 Files

- `JavaScript.js` – JavaScript function and test cases.
- `OutputArray.png` – Screenshot showing the output in the terminal.

---

## 💻 Code

```javascript
function first(array, n) {
  if (!Array.isArray(array) || array.length === 0) {
    return [];
  }

  if (n === undefined) {
    return array[0];
  }

  if (n < 0) {
    return [];
  }

  return array.slice(0, n);
}

// Test Data
console.log(first([7, 9, 0, -2]));
console.log(first([], 3));
console.log(first([7, 9, 0, -2], 3));
console.log(first([7, 9, 0, -2], 6));
console.log(first([7, 9, 0, -2], -3));

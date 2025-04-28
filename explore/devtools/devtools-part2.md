# DevTools Part 2

## 1. What was the bug?

The bug is that the `calculateSum` function just adds `num1` and `num2` directly.  
Since `num1` and `num2` are **string** types from the input fields, JavaScript does **string concatenation** instead of doing a math addition.

Example:
- If I enter `1` and `3`, the output is `13`, not `4`.

---

## 2. How did you fix it?

I fixed it by converting `num1` and `num2` into numbers inside the `calculateSum` function.

I used `Number()` to convert them before adding:

```javascript
function calculateSum(num1, num2) {
  let result = Number(num1) + Number(num2);
  return result;
}

# Part 2

## Question 1

**What will happen at line 12 and why?**

Line 12 prints `3`.

Since `i` was declared with `var`, it has function scope. That means we can still access it outside the `for` loop.  
After the loop finishes, `i` becomes `3` because it stops when it reaches the length of the `prices` array.  
No error happens here.

---

## Question 2

**What will happen at line 13 and why?**

Line 13 prints `150`.

`discountedPrice` was also declared with `var`, so it’s available anywhere inside the function.  
After the loop ends, `discountedPrice` holds the last calculated value, which is `150`.  
No error shows up.

---

## Question 3

**What will happen at line 14 and why?**

Line 14 prints `150`.

`finalPrice` is declared with `var` at the top of the function. That’s why it’s accessible after the loop.  
It keeps the last value we calculated, which is `150`.  
No error occurs.

---

## Question 4

**What will this function return?**

It returns `[50, 100, 150]`.

The function applies the discount to each price, rounds the result, and stores it in an array.  
Since the input is `[100, 200, 300]` and the discount is `0.5`, we get 50, 100, and 150.  
No errors here.

---

## Question 5

**What will happen at line 12 and why?**

Line 12 throws `ReferenceError: i is not defined`.

Because `i` was declared with `let`, it’s block-scoped.  
When the loop ends, `i` no longer exists outside the loop, so trying to print it causes an error.

---

## Question 6

**What will happen at line 13 and why?**

Line 13 throws `ReferenceError: discountedPrice is not defined`.

Since `discountedPrice` was declared with `let` inside the loop, it disappears once each iteration ends.  
Trying to access it outside causes an error.

---

## Question 7

**What will happen at line 14 and why?**

Line 14 prints `150`.

`finalPrice` is declared with `let` at the start of the function.  
It’s still accessible after the loop, holding the last calculated value `150`.  
No error here.

---

## Question 8

**What will this function return?**

It returns `[50, 100, 150]`.

Each price is multiplied by `(1 - discount)`, rounded, and stored in the array.  
Because the input is `[100, 200, 300]` and the discount is `0.5`, the final result is [50, 100, 150].  
No issues here.

---

## Question 9

**What will happen at line 11 and why?**

Line 11 throws `ReferenceError: i is not defined`.

Since `i` is block-scoped with `let`, it’s not available outside the loop.  
When we try to log it after the loop, it throws an error.

---

## Question 10

**What will happen at line 12 and why?**

Line 12 prints `3`.

`length` was declared with `const` at the start of the function, so it’s accessible anywhere inside.  
Since the input array has 3 items, it prints 3.

---

## Question 11

**What will this function return?**

It returns `[50, 100, 150]`.

The function applies the discount to each price and stores it in the array.  
Since the input array is `[100, 200, 300]` with a discount of `0.5`, we get [50, 100, 150].

---

## Question 12

**A. Accessing the value of the name property in the student object**

```javascript
student.name
```

---

**B. Accessing the value of the Grad Year property in the student object**

```javascript
student['Grad Year']
```

---

**C. Calling the function for the greeting property in the student object**

```javascript
student.greeting()
```

---

**D. Accessing the name property of the object in the Favorite Teacher property in student**

```javascript
student['Favorite Teacher'].name
```

---

**E. Access index zero in the array of the courseLoad property of the student object**

```javascript
student.courseLoad[0]
```
---

## Question 13: Arithmetic

**A. '3' + 2**

Result: `'32'`

Explanation: `'3'` is a string. When we use `+`, JavaScript turns `2` into `'2'` and joins them.

---

**B. '3' - 2**

Result: `1`

Explanation: Using `-` makes JavaScript convert `'3'` into number `3`. Then `3 - 2 = 1`.

---

**C. 3 + null**

Result: `3`

Explanation: `null` becomes `0` in math operations. So `3 + 0 = 3`.

---

**D. '3' + null**

Result: `'3null'`

Explanation: Here, `null` becomes the string `'null'` and gets joined with `'3'`.

---

**E. true + 3**

Result: `4`

Explanation: `true` becomes `1`, so `1 + 3 = 4`.

---

**F. false + null**

Result: `0`

Explanation: Both `false` and `null` are treated like `0`, so `0 + 0 = 0`.

---

**G. '3' + undefined**

Result: `'3undefined'`

Explanation: `undefined` becomes the string `'undefined'` and gets joined with `'3'`.

---

**H. '3' - undefined**

Result: `NaN`

Explanation: When using `-`, `'3'` becomes `3`, but `undefined` becomes `NaN`.  
`3 - NaN` is still `NaN`.

---

## Question 14: Comparison

**A. '2' > 1**

Result: `true`

Explanation: `'2'` becomes number `2`, and `2 > 1` is true.

---

**B. '2' < '12'**

Result: `false`

Explanation: When comparing two strings, JavaScript uses dictionary (lexicographic) order.  
Since `'2'` comes after `'1'`, it’s false.

---

**C. 2 == '2'**

Result: `true`

Explanation: `==` lets JavaScript convert `'2'` to `2`, so they’re equal.

---

**D. 2 === '2'**

Result: `false`

Explanation: `===` checks both type and value. A number and a string are not the same type.

---

**E. true == 2**

Result: `false`

Explanation: `true` becomes `1`. Since `1 != 2`, it’s false.

---

**F. true === Boolean(2)**

Result: `true`

Explanation: `Boolean(2)` is `true`, and `true === true` is true.

---

## Question 15: Difference between == and ===

`==` checks if two values are the same after type conversion. It lets JavaScript change types to compare.

`===` checks if two values are the same **without** any type conversion. Types must match exactly too.

---
## Question 16

[Click here to see part2-question16.js](./part2-question16.js)

---

## Question 17

If we call `modifyArray([1,2,3], doSomething)`, the result will be `[2, 4, 6]`.

Here’s why:

- `modifyArray` takes in an array and a function (`callback`) as inputs.
- It creates a new empty array `newArr`.
- Then it loops through the original array `[1,2,3]`.
- For each item, it calls `doSomething(num)` where `doSomething` just multiplies the number by 2.
- So:
  - `1 * 2 = 2`
  - `2 * 2 = 4`
  - `3 * 2 = 6`
- After pushing all results, `newArr` becomes `[2, 4, 6]`.

That’s the final result returned by the function.

---

## Question 18

[Click here to see part2-question18.js](./part2-question18.js)

---

## Question 19

The output of the code will be: `1 4 3 2`.

Here’s why:

- First, `console.log(1)` runs right away.
- Then `setTimeout(..., 1000)` schedules `console.log(2)` to run after 1 second.
- Next, `setTimeout(..., 0)` schedules `console.log(3)`, but even with 0 delay, it still gets pushed to the event queue and only runs after the main code finishes.
- `console.log(4)` runs immediately after the two `setTimeout` calls.
- After all the synchronous code is done, the event queue processes:
  - First, the `console.log(3)` runs (because it had 0ms delay).
  - Then, after 1 second, `console.log(2)` finally runs.

That’s why we see `1`, `4`, `3`, `2` in that order.

---

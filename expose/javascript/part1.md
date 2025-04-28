# Part 1


**Q1: What is printed by line 9?**

Line 9 prints: `values added: 20`.

Since line 9 is inside the `if (add)` block, `result` is set to `num1 + num2`, which is 10 + 10 = 20, and it gets printed.

---

**Q2: What is printed by line 13?**

Line 13 prints: `final result: 20`.

Because `result` was declared with `var`, it has function scope, so even though it was created inside the `if` block, it's still accessible outside. That's why it prints 20.

---

**Q3: Why should you not use var?**

We should avoid using `var` because it only has function scope, not block scope.  
This can cause unexpected behaviors and bugs, like variables leaking outside of blocks where we don't expect them.  
In this case, even if we didn’t add the numbers, `result` could still exist and cause confusion. It's better to use `let` or `const` to avoid these kinds of problems.

---

## Question 4

**Q4: What is printed by line 9?**

Line 9 prints: `values added: 20`.

Because `result` is declared with `let` inside the `if` block, and line 9 is still within that block, `result` is accessible and prints 20.

---

**Q5: What is printed by line 13?**

Line 13 throws a `ReferenceError: result is not defined`.

Since `let` is block-scoped, `result` only exists inside the `if` block.  
Line 13 tries to use it outside of that block, which causes an error.

---

## Question 6

**Q6: What is printed by line 9?**

Line 9 throws a `TypeError: Assignment to constant variable.`

Because `result` was declared with `const`, it can’t be reassigned after it's set.  
When the code tries to update `result = num1 + num2`, it breaks the rule and throws an error immediately.

---

## Question 7

**Q7: What is printed by line 13?**

Line 13 is never reached because the program already crashes earlier when trying to reassign `result` at line 7.  
So nothing gets printed from line 13.

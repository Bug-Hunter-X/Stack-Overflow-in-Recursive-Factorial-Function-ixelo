# Hack Bug Report: Stack Overflow in Recursive Factorial

This repository demonstrates a common error in recursive functions written in Hack: stack overflow.  The `foo` function calculates the factorial of a number using recursion. While functionally correct for smaller inputs, it's vulnerable to stack overflow for large inputs. The `bugSolution.hack` file provides a solution using iteration to avoid the stack overflow problem.

**Steps to Reproduce:**
1. Compile `bug.hack`.
2. Run the compiled program.  With small inputs (e.g., 5), the program will run successfully. Try a larger input, for example 10000, to trigger the stack overflow error.

**Expected Behavior:**
The program should calculate the factorial and output the result.

**Actual Behavior:**
For large inputs, the program crashes due to a stack overflow.

**Solution:**
The solution utilizes iteration to calculate the factorial, eliminating the recursive calls and thus preventing the stack overflow.
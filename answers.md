# CMPS 2200 Recitation 06
## Answers

**Name:** Sophie Strobl

Place all written answers from `recitation-07.md` here for easier grading.



- **2)**

W(n) = W(n-1) + W(n-2) + O(1)

This recurrence follows the Fibonacci sequence and results in exponential growth.

Each level of the recursion tree doubles the number of calls, and there are O(n) levels. The majority of the work happens at the leaves (leaf-dominated).

=> W(n) = O(2^n)


- **3)**


For fib_recursive(n), the two recursive calls are made sequentially, so only one path contributes to the span.

S(n) = S(n-1) + O(1)

Base case: S(0) = S(1) = O(1)

This solves to:

=> S(n) = O(n)

- **4)**

Values near the bottom (like F(0), F(1), F(2)) are computed many times, while higher values (closer to F(n)) are computed fewer times.

This highlights the inefficiency of naive recursion: the same subproblems are solved repeatedly — especially for smaller indices — leading to exponential redundancy.


- **6)**

Max number of calls per i: 1

Total number of calls: O(n)

Work: each Fibonacci number from 0 to n is computed once, and each computation does constant work.

=> Work = O(n)

Span: The longest sequence of dependent recursive calls goes from `fib_top_down(n)` down to `fib_top_down(0)`.

=> Span = O(n)

- **8)**

Max reads per F_i: 2

Total number of operations: O(n)

Each value from `F_2` to `F_n` is computed using constant-time operations.

=> Work = O(n)

The algorithm is purely sequential, and each value depends directly on the previous two.

=> Span = O(n)

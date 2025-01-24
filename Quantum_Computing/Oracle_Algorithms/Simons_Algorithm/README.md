# Simon's Problem

Simon’s problem is a computational challenge introduced by Daniel Simon in 1994. 

## Problem Statement

The black-box function $`f : \{0, 1\}^n \to \{0, 1\}^n`$ has the the following properties:

1. **Two-to-One Property:**
   - $`f(x1) = f(x2)`$ if and only if $`x1 \oplus x2 = s`$, where $`\oplus`$ denotes the bitwise XOR operation.
   - The string $`s \in \{0, 1\}^n`$ is called the **secret string**.

2. **Goal:**
   - Determine the secret string $`s`$ with the fewest possible evaluations of $`f`$.

- If $`s = 0`$, then $`f`$ is a one-to-one function.
- If $`s \neq 0`$, then $`f`$ is a two-to-one function, meaning each output of $`f`$ is produced by exactly two different inputs.
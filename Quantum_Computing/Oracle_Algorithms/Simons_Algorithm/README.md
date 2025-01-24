# Simon's Problem

Simon’s problem is a computational challenge introduced by Daniel Simon in 1994. 

## Problem Statement

The black-box function $`f : \{0, 1\}^n \to \{0, 1\}^n`$ has the the following properties:

1. **Two-to-One Property:**
   - $`f(x) = f(y)`$ if and only if $`x \oplus y = s`$, where $`\oplus`$ denotes the bitwise XOR operation.
   - The string $`s \in \{0, 1\}^n`$ is called the **secret string**.

2. **Goal:**
   - Determine the secret string $`s`$ with the fewest possible evaluations of $`f`$.
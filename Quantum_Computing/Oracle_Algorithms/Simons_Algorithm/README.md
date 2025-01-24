# Simon's Problem

Simon’s problem is a computational challenge introduced by Daniel Simon in 1994. 

## Problem Statement

The black-box function $`f : \{0, 1\}^n \to \{0, 1\}^n`$ has the the following properties:

1. **Two-to-One Property:**
   - $`f(x1) = f(x2)`$ if and only if $`x1 \oplus x2 = s`$, where $`\oplus`$ denotes the bitwise XOR operation.
   - The string $`s \in \{0, 1\}^n`$ is called the **secret string**.

2. **Goal:**
   - Determining the secret string $`s`$ with the fewest possible evaluations of $`f`$.

# Simon's Problem and the 2-to-1 Function

The core of Simon's problem is based on finding the secret string $`s`$, where for two distinct inputs $`x_1`$ and $`x_2`$, the following conditions hold:

1. $`f(x_1) = f(x_2)`$  
   (i.e., the function maps both $`x_1`$ and $`x_2`$ to the same output),
2. $`x_1 \oplus x_2 = s`$  
   (i.e., the XOR of $`x_1`$ and $`x_2`$ equals the secret string $`s`$).

For this to be possible, the function must be **2-to-1**. This means that there must be pairs of distinct inputs that produce the same output. These pairs are related by the secret string $`s`$, and you can find the secret string by identifying which inputs produce the same output.

---

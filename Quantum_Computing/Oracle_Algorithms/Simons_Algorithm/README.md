# Simon's Problem

Simon’s problem is a computational challenge introduced by Daniel Simon in 1994. 

## Problem Statement

The black-box function $`f : \{0, 1\}^n \to \{0, 1\}^n`$ has the the following properties:

1. **Two-to-One Property:**
   - $`f(x_1) = f(x_2)`$ if and only if $`x_1 \oplus x_2 = s`$, where $`\oplus`$ denotes the bitwise XOR operation.
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
## Why the Function Cannot Be 1-to-1 in Simon's Problem

If the function were **1-to-1** (injective), there would be no pairs of distinct inputs $`x_1`$ and $`x_2`$ that produce the same output. This would violate the condition $`f(x_1) = f(x_2)`$ for distinct $`x_1`$ and $`x_2`$.

Since Simon's problem relies on finding pairs of inputs that map to the same output (and whose XOR equals the secret string $`s`$), a **2-to-1 function** is essential for solving the problem. The algorithm exploits this 2-to-1 nature to deduce the secret string efficiently.

# Example of Simon's Problem with a 3-Bit Secret String

Let's assume the secret string $`s = 110`$ (a 3-bit string), and define the function $`f`$ such that:

- $`f(000) = 011`$
- $`f(001) = 011`$
- $`f(010) = 100`$
- $`f(011) = 100`$
- $`f(100) = 111`$
- $`f(101) = 111`$
- $`f(110) = 000`$
- $`f(111) = 000`$

---

## Inputs $`x_1`$ and $`x_2`$:

### First Pair: $`x_1 = 000`$ and $`x_2 = 001`$

1. Compute $`x_1 \oplus x_2`$:
   \[
   x_1 \oplus x_2 = 000 \oplus 001 = 001
   \]
   This does not match the secret string $`s = 110`$. Let's try another pair.

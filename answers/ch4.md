# Exercises for Chapter 4

### Exercise 4.1
Prove that the sum of the first $n$ odd natural numbers equals $n^2$ by induction or strong induction

<details>
  <summary>Answer</summary>
<br>

_**Proof.**_ We proceed by induction

<ins>Base case.</ins> $n=1$

$1=1^2$ which is true

<ins>Inductive Hypothesis.</ins>

Assume the statement holds for some $k \in \mathbb{N}$, that is
$1+3+5+...+ (2k-1)=k^2$

<ins>Induction Step.</ins>

We aim to prove that the result holds for $k+1$, that is
$1+3+5+...+ (2k-1) + (2(k+1) - 1)=(k+1)^2$

Substitute our inductive hypothesis, so

$k^2 + (2(k+1) - 1) =(k+1)^2$\
$k^2 + (2k + 2 - 1) =(k+1)^2$\
$k^2 + 2k + 1 =(k+1)^2$

which is true.

<ins>Conclusion.</ins> Therefore, by induction, the sum of the first $n$ odd natural numbers equals $n^2$ for all $n \in \mathbb{N}$. <p align="right">▉</p>
</details>

### Exercise 4.2
Provide three proofs that if $n \in \mathbb{N}$, then $n^2 - n$ is even.

(a) Prove it by cases, by considering the $n$ is even and $n$ is odd cases

<details>
  <summary>Answer</summary>
<br>

_**Proof.**_ We proceed by direct proof by cases

<ins>Case 1.</ins> $n$ is **even**

If $n$ is **even**, then $n = 2k$ for some $k \in \mathbb{N}$. Then,
$$n^2 - n = (2k)^2 - 2k = 4k^2 - 2k = 2(2k^2 - k)$$

Since it's divisible by 2, it's **even**.

<ins>Case 2.</ins> $n$ is **odd**

If $n$ is **odd**, then $n = 2k + 1$ for some $k \in \mathbb{N}$. Then,
$$n^2 - n = (2k + 1)^2 - (2k + 1) = (2k)^2 + 4k + 1 - 2k - 1 = 4k^2 + 2k = 2(2k^2 + k)$$

Since it's divisible by 2, it's **even**.

Thus, $n^2 - n$ is even for all $n \in \mathbb{N}$. <p align="right">▉</p>
</details>


(b) Prove it by applying Proposition 4.2 to the sum $1+2+3+...+(n-1)$

<details>
  <summary>Answer</summary>
<br>

_**Proof.**_ Using Proposition 4.2

By Proposition 4.2, $$1+2+3+...+n= \frac{n(n+1)}{2}$$
but a hint in example is to use 
$$1+2+3+...+(n-1)$$ which means
$$1+2+3+...+(n-1) = \frac{n(n-1)}{2}$$

Multiplying both sides by $2$, we have 

$$2(1+2+3+...+(n-1)) = n(n-1)$$

And since $n^2-n = n(n-1)$, $n^2 - n$ is even. <p align="right">▉</p>
</details>

(c) Prove it by induction


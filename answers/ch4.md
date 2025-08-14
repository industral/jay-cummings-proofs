# Exercises for Chapter 4

### Exercise 4.1
Prove that the sum of the first $n$ odd natural numbers equals $n^2$ by induction or strong induction

_**Proof.**_ We proceed by induction

<ins>Base case</ins> $n=1$

$1=1^2$ which is true

<ins>Inductive Hypothesis</ins>

Assume the statement holds for some $k \in \mathbb{N}$, that is
$1+3+5+...+ (2k-1)=k^2$

<ins>Induction Step</ins>

We aim to prove that the result holds for $k+1$, that is
$1+3+5+...+ (2k-1) + (2(k+1) - 1)=(k+1)^2$

Substitute our inductive hypothesis, so
$k^2 + (2(k+1) - 1) =(k+1)^2$
$k^2 + (2k + 2 - 1) =(k+1)^2$
$k^2 + 2k + 1 =(k+1)^2$

which is true.

<ins>Conclusion</ins> By induction, the sum of the first $n$ odd natural numbers equals $n^2$ for all $n \in \mathbb{N}$.





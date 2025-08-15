# Exercises for Chapter 4

### Exercise 4.1
Prove that the sum of the first $n$ odd natural numbers equals $n^2$ by induction or strong induction

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

<ins>Conclusion.</ins> Therefore, by induction, the sum of the first $n$ odd natural numbers equals $n^2$ for all $n \in \mathbb{N}$. ▉

### Exercise 4.2
Provide three proofs that if $n \in \mathbb{N}$, then $n^2 - n$ is even.

(a) Prove it by cases, by considering the $n$ is even and $n$ is odd cases

_**Proof.**_ We proceed by direct proof by cases

<ins>Case 1.</ins> $n$ is **even**

If $n$ is **even**, then $n = 2k$ for some $k \in \mathbb{N}$. Then,

$$
\begin{aligned}
n^2 - n &= (2k)^2 - 2k\\
& = 4k^2 - 2k \\
& = 2(2k^2 - k)
\end{aligned}
$$

Since it's divisible by 2, it's **even**.

<ins>Case 2.</ins> $n$ is **odd**

If $n$ is **odd**, then $n = 2k + 1$ for some $k \in \mathbb{N}$. Then,

$$
\begin{aligned}
n^2 - n &= (2k + 1)^2 - (2k + 1) \\
&= (2k)^2 + 4k + 1 - 2k - 1\\
&= 4k^2 + 2k\\
&= 2(2k^2 + k)
\end{aligned}
$$

Since it's divisible by 2, it's **even**.

Thus, $n^2 - n$ is even for all $n \in \mathbb{N}$. ▉

(b) Prove it by applying Proposition 4.2 to the sum $1+2+3+...+(n-1)$

_**Proof.**_ Using Proposition 4.2

By Proposition 4.2

$$1+2+3+...+n= \frac{n(n+1)}{2}$$

but a hint in the example is to use 
$$1+2+3+...+(n-1)$$ which means
$$1+2+3+...+(n-1) = \frac{n(n-1)}{2}$$

Multiplying both sides by $2$, we have 

$$2(1+2+3+...+(n-1)) = n(n-1)$$

And since $n^2-n = n(n-1)$, $n^2 - n$ is even. ▉

(c) Prove it by induction

_**Proof.**_ We proceed by induction

<ins>Base case.</ins> $n=1$

$1^2-1=0$ which is even

<ins>Inductive Hypothesis.</ins>

Assume $k^2-k$ is even for some $k \in \mathbb{N}$, that is

$k^2 - k = 2m$ for some $m \in \mathbb{Z}$

<ins>Induction Step.</ins>

We aim to prove that the result holds for $k + 1$, that is
$(k+1)^2 - (k+1)$ is also even.

$$
\begin{aligned}
(k+1)^2 - (k+1) &= k^2 + 2k + 1 - k - 1 \\
&= k^2 +k\\
&= (k^2 + k) - 2k
\end{aligned}
$$

Use inductive hypothesis $k^2 - k = 2m$, so

$$
\begin{aligned}
(k+1)^2 - (k+1) &= 2m + 2k\\
&= 2(m + k)
\end{aligned}
$$

which is even.

<ins>Conclusion.</ins> By induction, $n^2 - n$ is even for all $n \in \mathbb{N}$. ▉

### Exercise 4.3
Use induction or strong induction to prove that the following hold for every $n \in \mathbb{N}$.

(a) $3 | (4^n - 1)$

_**Proof.**_ We proceed by induction

<ins>Base case.</ins> $n=1$

$$4^1 - 1 = 4 - 1 = 3$$
and $3|3$. So statement holds for $n=1$.

<ins>Inductive Hypothesis.</ins>

Let $k \in \mathbb{N}$ and assume that $3 | (4^k - 1)$

<ins>Induction Step.</ins>

We have to prove that the result holds for $k+1$, that is

$$3 | (4^{k+1} - 1)$$

$4^k - 1 = 3m$ for some integer m.\
$4^k = 3m + 1$

$$
\begin{aligned}
4^{k+1} - 1 & = 4^k \cdot 4 - 1 \\
& =4(3m+1) - 1 \\
& =12m+4-1 \\
& =12m+3 \\
& =3(4m+1)
\end{aligned}
$$

hence, $3 | (4^{k+1} - 1)$.

<ins>Conclusion.</ins> Therefore, by induction, $3 | (4^n - 1)$ for all $n \in \mathbb{N}$. ▉

(b) $6 | (n^3 - n)$

_**Proof.**_ We proceed by induction

<ins>Base case.</ins> $n=1$

$1^3 - 1 = 0$, and $6|0$. Thus, the statement holds for $n=1$.

<ins>Inductive Hypothesis.</ins>

Let $k \in \mathbb{N}$ and assume that $6 | (k^3 - k)$.

<ins>Induction Step.</ins>

We need to prove that the result holds for $k+1$, that is

$$6 | ((k+1)^3 - (k+1))$$

$$
\begin{aligned}
(k+1)^3 - (k+1) &= k^3+3k^2+3k+1-(k+1) \\
&= k^3+3k^2+3k+1-k-1 \\
&= k^3 +3k^2 +2k \\
&= (k^3-k) + 3k^2+3k \\
&= (k^3-k) + 3(k^2+k) \\
&= (k^3-k) + 3 \cdot k(k+1)  && (1)
\end{aligned}
$$

By inductive hypothesis:
- $k^3-k$ is divisible by $6$
- $3$ divides $3$
- $k(k+1)$ is a product of two consecutive numbers, hence it's even. Thus, $2$ divides $k(k+1)$

Therefore, $3 \cdot k(k+1))$ is divisible by both $2$ and $3$, so it's divisible by $6$.

Since both terms on the right-hand side of (1) are multiples of $6$, their sum is also a multiple of $6$. Hence,

$$6|((k+1)^3 - (k+1))$$

<ins>Conclusion.</ins> By induction, $6 | (n^3 - n)$ for all $n \in \mathbb{N}$. ▉

(c) $9 | (3^{4n} + 9)$

_**Proof.**_ We proceed by induction

<ins>Base case.</ins> $n=1$

$3^{4\cdot1}+9=3^4+9=81+9=90$

Since $9|90$, so the base case holds.

<ins>Inductive Hypothesis.</ins>

Let $k \in \mathbb{N}$ and assume that $9|(3^{4k} +9)$.

<ins>Induction Step.</ins>

We must show that $9|(3^{4(k+1)} + 9)$

$$
\begin{aligned}
3^{4(k+1)} + 9 &= 3^4 \cdot 3^{4k} + 9 \\
&= 81 \cdot 3^{4k} + 9 \\
&= 9(9 \cdot 3^{4k} + 1)
\end{aligned}
$$

Since $9 \cdot 3^{4k} + 1 \in \mathbb{Z}$, it follows that $9|3^{4(k+1)} + 9$

<ins>Conclusion.</ins> By induction, $9|3^{4n} + 9$ for all $n \in \mathbb{N}$. ▉  

(d) $5 | (n^5 - n)$

_**Proof.**_ We proceed by induction

<ins>Base case.</ins> $n=1$

$$n^5 - n = 1^5 - 1 = 0$$

Since $5|0$, the base case holds.

<ins>Inductive Hypothesis.</ins>

Let $k \in \mathbb{N}$ and assume $5|(k^5 - k)$, that is, there exists $m \in \mathbb{Z}$ such that $k^5 - k = 5m$

<ins>Induction Step.</ins>

We must show that $5|((k+1)^5 - (k+1))$

Expand $(k+1)^5$ via Binomial Theorem:

$$(k+1)^5 = k^5 + 5k^4 + 10k^3 + 10k^2 + 5k + 1$$

Now

$$
\begin{aligned}
(k+1)^5 - (k+1) &= k^5 + 5k^4 + 10k^3 + 10k^2 + 5k + 1 - (k+1) \\
&= k^5 + 5k^4 + 10k^3 + 10k^2 + 5k + 1 - k - 1 \\
&= (k^5 - k) + 5k^4 + 10k^3 + 10k^2 + 5k && \text{(factor $(k^5 - k)$ so we can use inductive hypothesis)}   \\ 
&= (k^5 - k) + 5(k^4 + 2k^3 + 2k^2 + k) \\ 
&= 5m + 5(k^4 + 2k^3 + 2k^2 + k) && \text{(use inductive hypothesis)} \\ 
&= 5(m + k^4 + 2k^3 + 2k^2 + k) \\ 
\end{aligned}
$$

hence, $5|(k+1)^5 - (k+1)$.

<ins>Conclusion.</ins> By induction, $5|(n^5 - n)$ for all $n \in \mathbb{N}$. ▉

(e) $6 | (5^{2n} - 1)$

_**Proof.**_ We proceed by induction.

<ins>Base case.</ins> $n=1$

$5^{2n} - 1 = 5^{2 \cdot 1} - 1 = 5^2 - 1 = 24$. Since $6|24$, the statement holds for $n=1$.

<ins>Inductive Hypothesis.</ins>

Let $k \in \mathbb{N}$ and assume $6|5^{2k} - 1$, that is, there exists $m \in \mathbb{Z}$ such that $5^{2k} - 1 = 6m$.

<ins>Induction Step.</ins>

We must prove that $6|5^{2(k+1)} - 1$.

$$
\begin{aligned}
5^{2(k+1)} - 1 &= 5^{2k+2} - 1\\
&=5^{2k} \cdot 5^2 - 1 \\
&=5^{2k} \cdot 25 - 1 \\
&=25 \cdot 5^{2k} - 25 +  24 \\
&=25(5^{2k} - 1) +  24 \\
\end{aligned}
$$

By the inductive hypothesis, $5^{2k} - 1$ is divisible by $6$, so $25(5^{2k} - 1)$ is also divisible by $6$.\
Also, $24$ is divisible by $6$.\
The sum of two numbers divisible by $6$ is also divisible by $6$, hence $5^{2(k+1)} - 1$ is divisible by $6$.

<ins>Conclusion.</ins> By induction, $6 | (5^{2n} - 1)$ for all $n \in \mathbb{N}$. ▉

(f) $5 | (6^n - 1)$

_**Proof.**_ We proceed by induction.

<ins>Base case.</ins> $n=1$

$6^n - 1 = 6^1 - 1 = 6 - 1 = 5$. Since $5 | 5$, the statement holds for $n=1$.

<ins>Inductive Hypothesis.</ins>

Let $k \in \mathbb{N}$ and assume $5|(6^k - 1)$, that is, there exists $m \in \mathbb{Z}$ such that $6^k - 1 = 5m$.

<ins>Induction Step.</ins>

We must prove that $5|(6^{k+1} - 1)$.

$$
\begin{aligned}
6^{k+1} - 1 &= 6^k \cdot 6 - 1\\
&= 6(6^k) - 1 \\
&= 6(6^k) - 6 + 5 \\
&= 6(6^k - 1) + 5 && \text{(express in terms of $(6^k - 1)$ so we can use inductive hypothesis)} \\
&= 6 \cdot 5m + 5 && \text{(by the inductive hypothesis)} \\
&= 30m + 5 \\
\end{aligned}
$$

Since both $30m$ and $5$ are divisible by $5$, $6^{k+1} - 1$ is divisible by $5$.

<ins>Conclusion.</ins> By induction, $5 | (6^n - 1)$ for all $n \in \mathbb{N}$. ▉

## Quiz 01

1. 什么是信息科学
2. 学习信息科学理论有什么用，怎么学习对科研更有帮助
3. 对课程教学的建议

## Quiz 02: Prove the following propositions

### Proposition 2.5

For random variables $X$, $Y$, and $Z$, $X\perp Z\mid Y$ if and only if

$$
p(x,y,z)=a(x,y)b(y,z)
$$

for all $x$, $y$, and $z$ such that $p(y)>0$.

### Proposition 2.27 (Chain Rule for Conditional Mutual Information)

For random variables $X_1,X_2,\ldots,X_n,Y$, and $Z$,

$$
I(X_1,X_2,\ldots,X_n;Y\mid Z)
=\sum_{i=1}^{n} I(X_i;Y\mid X_1,\ldots,X_{i-1},Z).
$$

## Quiz 03: Prove the following

$$
D(p\Vert q)=\sum_x p(x)\log\frac{p(x)}{q(x)}
=E_p\log\frac{p(X)}{q(X)}.
$$

**(1)** Theorem 2.31 (Divergence Inequality)

For any two probability distributions $p$ and $q$ on a common alphabet $\mathcal{X}$,

$$
D(p\Vert q)\ge0, \qquad (2.107)
$$

with equality if and only if $p=q$.

**(2)** Lemma 2.41

If $X\to Y\to Z$ forms a Markov chain, then

$$
I(X;Z)\le I(X;Y)
$$

and

$$
I(X;Z)\le I(Y;Z).
$$

## Quiz 4: Compute the channel capacity

**Binary Symmetric Channel (BSC)**

```text
    Z
    ↓
X → ⊕ → Y
```

Alternative representation of a BSC:

$$
Y=X+Z\pmod2
$$

with

$$
\Pr\lbrace Z=0\rbrace=1-\epsilon
\qquad\text{and}\qquad
\Pr\lbrace Z=1\rbrace=\epsilon,
$$

and $Z$ is independent of $X$.

## Quiz 05: Prove that $H(W)=I(X;Y)$.

- **Message Set:** $\mathcal{W}=\lbrace 1,2,\ldots,M\rbrace$.
- **Codewords:** $f(1),f(2),\ldots,f(M)$.
- **Codebook:** The set of all codewords.

```text
W → [Encoder] → X → [Channel p(y|x)] → Y → [Decoder] → Ŵ
```

Message $W$ · Estimate of message $\hat W$

$$
f:\lbrace 1,2,\ldots,M\rbrace\to\mathcal{X}^n,
\qquad
g:\mathcal{Y}^n\to\lbrace 1,2,\ldots,M\rbrace.
$$

The communication system consists of the r.v.’s

$$
W,X_1,Y_1,X_2,Y_2,\ldots,X_n,Y_n,\hat W
$$

generated in this order.

The memorylessness of the DMC imposes the following Markov constraint for each $i$:

$$
(W,X_1,Y_1,\ldots,X_{i-1},Y_{i-1})\to X_i\to Y_i.
$$

## Quiz 06: Prove Kraft inequality and solve optimal code

### (1) Prove Kraft Inequality

**Theorem 5.2.1 (Kraft inequality).** For any instantaneous code (prefix code) over an alphabet of size $D$, the codeword lengths $l_1,l_2,\ldots,l_m$ must satisfy the inequality

$$
\sum_i D^{-l_i}\le1. \qquad (5.6)
$$

Conversely, given a set of codeword lengths that satisfy this inequality, there exists an instantaneous code with these word lengths.

**(2)** Solve the problem of finding the prefix code with the minimum expected length.

## Quiz 07

1. 请简述 Minimum Description Length（MDL，最小描述长度）原理的核心思想；并说明粗两部分 MDL（crude two-part MDL）的目标优化表达式，解释每一项的物理含义。

2. 请比较信源编码、信道编码、率失真、最小描述长（MDL）这几个理论。

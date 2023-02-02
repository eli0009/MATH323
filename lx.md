Enlai Li - Jan 30, 2023

$y \sim Bin(n, p)$
"~" = distributed according to

$$X_{i} = {}
\begin{Bmatrix}
1 & p \\
0 & 1-p 
\end{Bmatrix}
$$

$$
Y = \sum_{i=1}^{n} X_i
$$
$$
P(X_i = 1) = p \\
P(X_i = 0) = 1 - p \\
P(Y = K) = 
\binom{n}{K}
p^K(1-p)^{n-k}
\\
k = 0, 1, 2, ..., n
$$

$$
Var (Y) = \mathbb{E}(Y^2) - [\mathbb{E} (Y)]^2 \\{}
[\mathbb{E}(Y)]^2 = \mathbb{E}[Y(Y-1)] + \mathbb{E}(Y) \\
\mathbb{E}[Y(Y-1)]
$$

$$
Var(Y) = Var(\sum_{i=1}^n X_i) \\
\stackrel{?}{=} \sum_{i=1}^n Var(X_i)
Var(X_i) = \mathbb{E}(X_i^2) - [\mathbb{E}(X_i)]^2 \\
\mathbb{E}(X_i^2) = 1^2 \cdot p \ + \ 0^2 \cdot (1-p) \\ = p
\\ Var(X_i) = p \ - \ [p]^2 \\ = p \ - \ p^2 \\ = p(1 \ - \ p)
$$

## The Geometric p.m.f

- Q1: $\frac{6}{49}$ 1st trial
- Q2 2nd trial
- Q3: How long on the average should one wait to win the jackpot of $\frac{6}{49}$

1. An infinite sequence of identical and independant trial
2. Each trial can only result in one of two possible outcomes
$$
1(S) \ or \ 0 (F)
$$
3. probability of S remains the same, say p
$$
X_i = \begin{Bmatrix}
1 & p \\
0 & 1-p
\end{Bmatrix}
$$
4. The geometric r.v. Y is the # of trial required for success
$$
S = \lbrace s_1, s_2, ... \rbrace
\\ s_1: 1
\\ s_2: 0 \ 1
\\ s_3: 0 \ 0 \ 1
\\ \dots
\\ s_k: \underbrace{0 \ 0 \ ... \ 0}_{k-1} \ 1
$$
$$
Y: S \rightarrow \mathbb{R}
\\ Y(s_k) = k
\\ P(Y = k) = P(s_k)
\\ P(Y=1) = p
\\ P(Y=2) = (1-p)p
\\ P(Y=3) = (1-p)^2 \ p
\\ ... 
\\ P(Y=3) = (1-p)^{k -1} \ p > 0
\\ k = 1, 2, ... \\
\sum_{k=1}^\infty P(Y=k) \stackrel{?}{=} 1 \\
\sum_{k=1}^\infty (1-p)^{k-1}p \\
= p \sum_{k=1}^\infty (1-p)^{k-1}
$$

$$
\sum_{k=0}^\infty x^k \\
\phi_n(x) = \sum_{k=0}^\infty x^k \\
x\phi_n(x) = \sum_{k=0}^\infty x^{k+1} \\
\underbrace{\phi_n(x) - x\phi_n(x)}_{{(1-x)}\phi_n(x)} = \sum_{k=0}^\infty x^k - \sum_{k=0}^\infty x^{k+1}
\\ = (1+\sout{x+x^2+...+x^n}) - (\sout{x+x^2+...}+x^{n+1})
\\ = 1 - x^{n+1}
$$
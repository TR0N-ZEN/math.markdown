Anstieg einer Potenzfunktion $f(x) = x^n$ am/im Punkt $(x_0,f(x_0))$,
abgekürzt als $f'(x_0)$ oder $\frac{d f(x)}{d x}$ oder $\frac{d f}{d x}$.

$$
\begin{aligned}
f'(x_0) &=  \lim_{\Delta x → 0}
\frac
  {f(x_0+ \Delta x)-f(x_0)}
  {(x_0 + \Delta x) - x_0} \\
\\
&= \lim_{\Delta x → 0}
\frac
  {(x_0+ \Delta x)^n - (x_0)^n}
  {(x_0 + \Delta x) - x_0} \\
\end{aligned}
$$



Ersetze $(x_0 + \Delta x)$ durch $a$ und
ersetze $(x_0)$ durch $b$.

$$
\begin{aligned}
f'(b)=&\lim_{\Delta a → b}
\frac
  {a^n - b^n}
  {a- b}
\\
=&\lim_{\Delta a → b}
\frac
  { (a - b) (a^{n-1} + a^{n-2} b^1 + ... + a^1 b^{n-2} + b^{n-1})}
  {a- b}
\\
=&\lim_{\Delta a → b}
  a^{n-1} + a^{n-2} b^1 + ... + a^1 b^{n-2} + b^{n-1}
\\
=&b^{n-1} + b^{n-2} b^1 + ... + b^1 b^{n-2} + b^{n-1}
\\
=&\underbrace{ b^{n-1} + b^{n-1} + ... + b^{n-1} + b^{n-1} }_{n}
\\
=&n \cdot b^{n-1}
\end{aligned}
$$

Ersetze $b$ zurück durch $(x_0)$

$$
f'(x_0) = n \cdot (x_0)^{n-1}
$$

Das Taylorpolynom

$$
p_n(x) = \sum_{k=0}^n \frac{f^{(k)}(x_0)}{k!} \cdot (x-x_0)^k
$$

für die Sinusfunktion $\sin(x)$

$$
p_{\sin}(x) = \sum_{k=0}^n \frac{\sin^{(k)}(x_0)}{k!} \cdot (x-x_0)^k
$$

in der Umgebung von $x_0$ für $x_0 = 0$

$$
\begin{aligned}
p_{\sin}(x) &= \sum_{k=0}^n \frac{\sin^{(k)}(0)}{k!} \cdot (x-0)^k \\
p_{\sin}(x) &= \sum_{k=0}^n \frac{\sin^{(k)}(0)}{k!} \cdot x^k \\
p_{\sin}(x) &=   \frac{\sin^{(0)}(0)}{0!} \cdot x^0
               + \frac{\sin^{(1)}(0)}{1!} \cdot x^1
               + \frac{\sin^{(2)}(0)}{2!} \cdot x^2
               + \frac{\sin^{(3)}(0)}{3!} \cdot x^3
               + \frac{\sin^{(4)}(0)}{4!} \cdot x^4
               + ... \\
p_{\sin}(x) &=   \sin^{(0)}(0) \frac{x^0}{0!}
               + \sin^{(1)}(0) \frac{x^1}{1!}
               + \sin^{(2)}(0) \frac{x^2}{2!}
               + \sin^{(3)}(0) \frac{x^3}{3!}
               + \sin^{(4)}(0) \frac{x^4}{4!}
               + ... \\
p_{\sin}(x) &=   \sin(0) \frac{x^0}{0!}
               + \cos(0) \frac{x^1}{1!}
               - \sin(0) \frac{x^2}{2!}
               - \cos(0) \frac{x^3}{3!}
               + \sin(0) \frac{x^4}{4!}
               + ... \\
p_{\sin}(x) &=   \frac{x^1}{1!}
               - \frac{x^3}{3!}
               + \frac{x^5}{5!}
               - \frac{x^7}{7!}
               + ... \\
p_{\sin}(x) &= \sum_{k=0}^{n} (-1)^k \cdot \frac{x^{2k+1}}{(2k+1)!}
\end{aligned}
$$

Entwickle Taylorpolynom für $f=\cos$
in der Umgebung von $x_0$ für $x_0 = 0$

$$
\begin{aligned}
p_{\cos}(x) &= \sum_{k=0}^n \frac{\cos^{(k)}(0)}{k!} \cdot (x-0)^k \\
p_{\cos}(x) &= \sum_{k=0}^n \frac{\cos^{(k)}(0)}{k!} \cdot x^k \\
p_{\cos}(x) &=   \frac{\cos^{(0)}(0)}{0!} \cdot x^0
               + \frac{\cos^{(1)}(0)}{1!} \cdot x^1
               + \frac{\cos^{(2)}(0)}{2!} \cdot x^2
               + \frac{\cos^{(3)}(0)}{3!} \cdot x^3
               + \frac{\cos^{(4)}(0)}{4!} \cdot x^4
               + ... \\
p_{\cos}(x) &=   \cos^{(0)}(0) \frac{x^0}{0!}
               + \cos^{(1)}(0) \frac{x^1}{1!}
               + \cos^{(2)}(0) \frac{x^2}{2!}
               + \cos^{(3)}(0) \frac{x^3}{3!}
               + \cos^{(4)}(0) \frac{x^4}{4!}
               + ... \\
p_{\cos}(x) &=   \cos(0) \frac{x^0}{0!}
               - \sin(0) \frac{x^1}{1!}
               - \cos(0) \frac{x^2}{2!}
               + \sin(0) \frac{x^3}{3!}
               + \cos(0) \frac{x^4}{4!}
               + ... \\
p_{\cos}(x) &=   \frac{x^0}{0!}
               - \frac{x^2}{2!}
               + \frac{x^4}{4!}
               - \frac{x^6}{6!}
               + \frac{x^8}{8!}
               + ... \\
p_{\cos}(x) &= \sum_{k=0}^{n} (-1)^k \cdot \frac{x^{2k}}{(2k)!}
\end{aligned}
$$

Entwickle Taylorpolynom für $f(x)=e^x=\exp(x)$
in der Umgebung von $x_0$ für $x_0 = 0$

$$
\begin{aligned}
p_{\exp}(x) &= \sum_{k=0}^n \frac{(\exp^k(0))}{k!} \cdot (x-0)^k \\
p_{\exp}(x) &= \sum_{k=0}^n \frac{(\exp^k(0))}{k!} \cdot x^k \\
p_{\exp}(x) &=   \frac{(\exp^0(0))}{0!} \cdot x^0
               + \frac{(\exp^1(0))}{1!} \cdot x^1
               + \frac{(\exp^2(0))}{2!} \cdot x^2
               + \frac{(\exp^3(0))}{3!} \cdot x^3
               + ... \\
p_{\exp}(x) &=   \frac{\exp(0)}{0!} \cdot x^0
               + \frac{\exp(0)}{1!} \cdot x^1
               + \frac{\exp(0)}{2!} \cdot x^2
               + \frac{\exp(0)}{3!} \cdot x^3
               + ... \\
p_{\exp}(x) &=   \frac{x^0}{0!}
               + \frac{x^1}{1!}
               + \frac{x^2}{2!}
               + \frac{x^3}{3!}
               + ... \\
p_{\exp}(x) &= \sum_{k=0}^{n} \frac{x^k}{k!}
\end{aligned}
$$

Bei *genauer Betrachtung* auch bekannt als *scharfes Hinsehen*,
fällt auf, dass ...

$$
\begin{aligned}
e^{ix} =& \cos(x) + i \cdot \sin(x)
\\
p_{\exp}(ix) =& p_{\cos}(x) + i \cdot p_{\sin}(x)
\\
\sum_{k=0}^{n} \frac{(ix)^k}{k!}
=&
          \sum_{k=0}^{n} (-1)^k \cdot \frac{x^{2k}}{(2k)!}
+ i \cdot \sum_{k=0}^{n} (-1)^k \cdot \frac{x^{2k+1}}{(2k+1)!}
\\
  \frac{(ix)^0}{0!}
+ \frac{(ix)^1}{1!}
+ \frac{(ix)^2}{2!}
+ \frac{(ix)^3}{3!}
+ \frac{(ix)^4}{4!}
+ \frac{(ix)^5}{5!}
+ \frac{(ix)^6}{6!}
+ \frac{(ix)^7}{7!}
+ \frac{(ix)^8}{8!}
+ ...
=&    \frac{x^0}{0!}
    - \frac{x^2}{2!}
    + \frac{x^4}{4!}
    - \frac{x^6}{6!}
    + \frac{x^8}{8!}
    + ...
  +  i \cdot (
      \frac{x^1}{1!}
    - \frac{x^3}{3!}
    + \frac{x^5}{5!}
    - \frac{x^7}{7!}
    + ...
  )
\\
  \frac{i^0 x^0}{0!}
+ \frac{i^1 x^1}{1!}
+ \frac{i^2 x^2}{2!}
+ \frac{i^3 x^3}{3!}
+ \frac{i^4 x^4}{4!}
+ \frac{i^5 x^5}{5!}
+ \frac{i^6 x^6}{6!}
+ \frac{i^7 x^7}{7!}
+ \frac{i^8 x^8}{8!}
+ ...
=&    \frac{x^0}{0!}
    - \frac{x^2}{2!}
    + \frac{x^4}{4!}
    - \frac{x^6}{6!}
    + \frac{x^8}{8!}
    + ...
  +
      i \cdot \frac{x^1}{1!}
    - i \cdot \frac{x^3}{3!}
    + i \cdot \frac{x^5}{5!}
    - i \cdot \frac{x^7}{7!}
    + ...
\\
  \frac{    x^0}{0!}
+ \frac{i^1 x^1}{1!}
- \frac{    x^2}{2!}
- \frac{i^1 x^3}{3!}
+ \frac{    x^4}{4!}
+ \frac{i^1 x^5}{5!}
- \frac{    x^6}{6!}
- \frac{i^1 x^7}{7!}
+ \frac{    x^8}{8!}
+ ...
=&    \frac{  x^0}{0!}
    - \frac{  x^2}{2!}
    + \frac{  x^4}{4!}
    - \frac{  x^6}{6!}
    + \frac{  x^8}{8!}
    + ...
  +
      \frac{i x^1}{1!}
    - \frac{i x^3}{3!}
    + \frac{i x^5}{5!}
    - \frac{i x^7}{7!}
    + ...
\\
  \frac{  x^0}{0!}
+ \frac{i x^1}{1!}
- \frac{  x^2}{2!}
- \frac{i x^3}{3!}
+ \frac{  x^4}{4!}
+ \frac{i x^5}{5!}
- \frac{  x^6}{6!}
- \frac{i x^7}{7!}
+ \frac{  x^8}{8!}
+ ...
=&    \frac{  x^0}{0!}
    + \frac{i x^1}{1!}
    - \frac{  x^2}{2!}
    - \frac{i x^3}{3!}
    + \frac{  x^4}{4!}
    + \frac{i x^5}{5!}
    - \frac{  x^6}{6!}
    - \frac{i x^7}{7!}
    + \frac{  x^8}{8!}
    + ...
\\
\end{aligned}
$$

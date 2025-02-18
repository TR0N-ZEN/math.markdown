# Funktionsapproximation


Sei $f(x)$ die zu schätzende Funkion.  
Sei $x_0$ eine Stelle die *nahe* (was das genau heißt später) der
  Stelle $x$ für die $f(x)$ geschätzt werden soll.


## linear

Falls $f'(x)$ existiert,
sucht man sich eine Stelle $x_0$, für die man den Wert von $f$, also $f(x_0)$ kennt.
Dann berechnet man die Steigung von $f$ an der Stelle $x_0$, also $f'(x_0)$ und
multipliziert diesen mit dem Abstand von $x_0$ zu $x$ , also mit $(x - x_0)$:

$f(x) \approx f(x_0) + f'(x_0) \cdot (x-x_0) = p_1(x)$

Also wird $f(x)$ in der Nähe der Stelle $x_0$ durch/von/mit $p_1(x)$ geschätzt/approximiert.



## quadratisch

Wäre die Änderung von $f'$ an der Stelle $x_0$ null, also $f''(x_0) = 0$,
so wäre die Schätzung durch 

$f(x) \approx f(x_0) + f'(x_0) \cdot (x-x_0) = p_1(x)$

das Ergebnis des gegenwärtigen Schätzungsansatzes.

Falls $f''(x)$ existiert und verschieden null ist,  
lässt sich $f''$, also die Änderung von $f'$, nutzen um die Schätzung zu optimieren.

Angenommen der Wert der Veränderung von $f'$, also $f''$, liegt in der Umgebung von $x_0$ nah an der tatsächlichen Änderung
von $f'$, so ist $f''(x_0) \cdot (x - x_0)$ die Veränderung von $f'$ auf dem Abschnitt zwischen $x_0$ und $x$.
$f''(x_0) \cdot (x-x_0) \cdot (x-x_0)$ bzw. $f''(x_0) \cdot (x-x_0)^2$ wäre somit, der Beitrag an $f$,
den die Veränderung $f'$ auf dem Abschitt zwischen $x_0$ und $x$ leistet.

$f(x) \approx f(x_0) + f'(x_0) \cdot (x-x_0) + f''(x_0) \cdot (x-x_0)^2$

Doch auch die Ableitungen der Schätzung sollten an der Stelle $x_0$ von der die Schätzung für die Umgebung erfolgt,
den gleichen Wert wie die Ableitung der zu schätzende Funktion $f$, also $f'$ haben.

Also $f$ erstmal nach $x$ ableiten:

$$
\begin{aligned}
f'(x) &= (f(x_0)   + f'(x_0) \cdot (x-x_0)     + f''(x_0) \cdot (x-x_0)^2)' \\
f'(x) &= (f(x_0)   + (f'(x_0) \cdot (x-x_0))'  + (f''(x_0) \cdot (x-x_0)^2)' \\
f'(x) &= (f(x_0))' + f'(x_0) \cdot ((x-x_0))'  + f''(x_0) \cdot ((x-x_0)^2)' \\
f'(x) &= 0         + f'(x_0)                   + f''(x_0) \cdot 2 \cdot (x-x_0)^1 \\
f'(x) &= f'(x_0) + f''(x_0) \cdot 2 \cdot (x-x_0)^1 \\
\end{aligned}
$$

Und $x_0$ für $x$ einsetzen: $f'(x_0) = f'(x_0) + f''(x_0) \cdot 2 \cdot (x_0-x_0)^1 = f'(x_0)$

Nun $f'$ nach $x$ ableiten:

$$
\begin{aligned}
f''(x) &= (f'(x_0)   + f''(x_0) \cdot 2 \cdot (x-x_0)^1)' \\
f''(x) &= (f'(x_0))' + (f''(x_0) \cdot 2 \cdot (x-x_0)^1)' \\
f''(x) &= 0          + f''(x_0) \cdot 2 \cdot ((x-x_0)^1)' \\
f''(x) &=              f''(x_0) \cdot 2 \\
\end{aligned}
$$

Das sieht jetzt schon problematisch aus, wird beim Einsetzen von $x_0$ für $x$, dann aber offensichtlich,

denn $f''(x_0) = f''(x_0) \cdot 2$ ist offensichtlich ein Widerspruch.

Dies ließe sich jedoch durch die Korrektur von

$f(x) \approx f(x_0) + f'(x_0) \cdot (x-x_0) + f''(x_0) \cdot (x-x_0)^2$  
zu  
$f(x) \approx f(x_0) + f'(x_0) \cdot (x-x_0) + \frac{f''(x_0) \cdot (x-x_0)^2}{2} = p_2(x)$

Also wird $f(x)$ in der Nähe der Stelle $x_0$ durch/von/mit $p_2(x)$ geschätzt/approximiert.


## kubisch

Falls $f'''(x)$ existiert und verschieden null ist,  
lässt sich $f'''$, also die Änderung von $f''$, nutzen um die Schätzung weiter zu optimieren.

...

$f(x) \approx f(x_0) + f'(x_0) \cdot (x-x_0) + \frac{f''(x_0) \cdot (x-x_0)^2}{2} + \frac{f'''(x_0) \cdot (x-x_0)^3}{3 \cdot 2}$

## Generalisierung zur Approximation durch Taylorpolynome

Da für $m \leq k$ beim $m$-fachen Ableiten von $(x-x_0)^k$ nach $x$,
sich der Term $k \cdot (k-1) \cdot (k-2) \cdot ... \cdot (k-(m-1)) \cdot (x - x_0)^{k-m}$
bzw. kürzer geschrieben $\frac{k!}{(k-m)!} \cdot (x-x_0)^{k-m}$ ergibt,
würde insbesondere für $m=k$:

$$
\begin{aligned}
f^{(k)}(x) &= (f^{(k-1)}(x_0)   + f^{(k)}(x_0) \cdot k \cdot (k-1) \cdot (k-2) \cdot ... \cdot 2 \cdot (x-x_0)^1)' \\
f^{(k)}(x) &= (f^{(k-1)}(x_0))' + (f^{(k)}(x_0) \cdot k \cdot (k-1) \cdot (k-2) \cdot ... \cdot 2 \cdot (x-x_0)^1)' \\
f^{(k)}(x) &= 0                 + f^{(k)}(x_0) \cdot k \cdot (k-1) \cdot (k-2) \cdot ... \cdot 2 \cdot ((x-x_0)^1)' \\
f^{(k)}(x) &= f^{(k)}(x_0) \cdot k \cdot (k-1) \cdot (k-2) \cdot ... \cdot 2 \cdot 1 \\
f^{(k)}(x) &= f^{(k)}(x_0) \cdot k!\\
\end{aligned}
$$

und beim Einsetzen von $x_0$ für $x$

$f^{(k)}(x) = f^{(k)}(x_0) \cdot k!$

ein offensichtlicher Widerspruch,

bzw. für $m \lt k$

$$
\begin{aligned}
f^{(m)}(x) =&  (f^{(m-1)}(x_0) \\
              &+ f^{(m)}(x_0) \cdot m! \cdot (x-x_0)^{1} \\
              &+ f^{(m+1)}(x_0) \cdot \frac{(m+1)!}{2!} \cdot (x-x_0)^{2} \\
              &+ ... \\
              &+ f^{(k)}(x_0) \cdot \frac{k!}{(k-(m-1))!} \cdot (x-x_0)^{k-(m-1)})' \\
              \\
f^{(m)}(x) =&  (f^{(m-1)}(x_0))' \\
              &+ (f^{(m)}(x_0) \cdot m! \cdot (x-x_0)^{1})' \\
              &+ (f^{(m+1)}(x_0) \cdot \frac{(m+1)!}{2!} \cdot (x-x_0)^{2})' \\
              &+ ... \\
              &+ (f^{(k)}(x_0) \cdot \frac{k!}{(k-(m-1))!} \cdot (x-x_0)^{k-(m-1)})' \\
              \\
f^{(m)}(x) =&  0 \\
              &+ f^{(m)}(x_0) \cdot m! \\
              &+ f^{(m+1)}(x_0) \cdot \frac{(m+1)!}{2!} \cdot 2 \cdot (x-x_0)^{1} \\
              &+ ... \\
              &+ f^{(k)}(x_0) \cdot \frac{k!}{(k-(m-1))!} \cdot (k - (m-1)) \cdot (x-x_0)^{k-m} \\
              \\
f^{(m)}(x) =&  0 \\
              &+ f^{(m)}(x_0) \cdot m! \\
              &+ f^{(m+1)}(x_0) \cdot \frac{(m+1)!}{2!} \cdot 2 \cdot (x-x_0)^{1} \\
              &+ ... \\
              &+ f^{(k)}(x_0) \cdot \frac{k!}{(k-m)!} \cdot (x-x_0)^{k-m} \\
              \\
\end{aligned}
$$

und beim Einsetzen von $x_0$ für $x$

$$
\begin{aligned}
f^{(m)}(x_0) =& f^{(m)}(x_0) \cdot m! \\
              &+ f^{(m+1)}(x_0) \cdot \frac{(m+1)!}{2!} \cdot 2 \cdot (x_0-x_0)^{1} \\
              &+ ... \\
              &+ f^{(k)}(x_0) \cdot \frac{k!}{(k-m)!} \cdot (x_0-x_0)^{k-m} \\
              \\
f^{(m)}(x_0) =& f^{(m)}(x_0) \cdot m! \\
              &+ f^{(m+1)}(x_0) \cdot \frac{(m+1)!}{2!} \cdot 2 \cdot 0^{1} \\
              &+ ... \\
              &+ f^{(k)}(x_0) \cdot \frac{k!}{(k-m)!} \cdot 0^{k-m} \\
              \\
f^{(m)}(x_0) =& f^{(m)}(x_0) \cdot m! \\
\end{aligned}
$$

, auch ein offensichtlicher Widerspruch,
ergeben würde.

Fast genau so offensichtlich wie der Widerspruch ist ein Lösungsansatz,
der jedes ${f^{(m)}(x_0)}$ im schätzenden/approximierende Polynom durch
$\frac{f^{(m)}(x_0)}{m!}$ ersetzt.

<!-- ... -->

Falls also die $n$-te Ableitung von $f$ existiert,
lassen sich die Ableitungen ${\forall k \leq n: f^{(k)}}$
für die Schätzung nutzen, sodass das Polynom

$$f(x) \approx \sum_{k=0}^n \frac{f^{(k)}(x_0)}{k!} \cdot (x-x_0)^k = p_n(x)$$

zur Schätzung/Approximation von $f(x)$ genutzt werden würde.

Eine beliebige Funktion $f(x)$ soll in *naher Umgebung* der Stelle $x_0$
durch ein Polynom $p_n(x)$ approximiert werden,  
das Kriterium das dieses Polynom erfüllen muss ist:

An der Stelle $x_0$ muss für jede existente Ableitung $f^{(k)}$ der $n$-fach differenzierbaren Funktion $f$ und entsprechende Ableitung $p_n^{(k)}$ von $p_n$,
auf den gleichen Wert abgebildet werden, also unmissverständlich ausgedrückt:

$$\forall k \in \mathbb{N}, k \leq n : p_n^{(k)}(x_0) = f^{(k)}(x_0)$$  

Also schauen wir mal, ob $p_n$ abgeleitet, also $p_n'$, an der Stelle $x_0$, den gleichen Wert wie $f(x_0)$ hat.

$$
\begin{aligned}
  p_n(x)         &= \sum_{k=0}^n \frac{f^{(k)}(x_0)}{k!} \cdot (x-x_0)^k
    \quad\text{leite nach } x \text{ ab}\\
  (p_n(x))'      &= \bigg( \sum_{k=0}^n \Big( \frac{f^{(k)}(x_0)}{k!} \cdot (x-x_0)^k    \Big) \bigg)'
    \quad\text{wende } (a_0x + b_0x)' = (a_0x)' + (b_0x)' \text{ an}\\
  (p_n(x))'      &=        \sum_{k=0}^n \Big( \frac{f^{(k)}(x_0)}{k!} \cdot (x-x_0)^k    \Big)'
    \quad\text{wende } (a_0 \cdot x)' = a_0 \cdot x' \text{ an}\\
  (p_n(x))'      &=        \sum_{k=0}^n \Big( \frac{f^{(k)}(x_0)}{k!} \cdot ((x-x_0)^k)' \Big)
    \quad\text{wende } (x^n)' = n \cdot x^{n-1} \text{ an}\\
  (p_n(x))'      &=        \sum_{k=0}^n \Big( \frac{f^{(k)}(x_0)}{k!} \cdot 1 \cdot k \cdot (x-x_0)^{k-1} \Big)
    \quad\text{}\\
  (p_n(x))'      &=        \sum_{k=0}^n \Big( \frac{f^{(k)}(x_0)}{k!} \cdot k \cdot (x-x_0)^{k-1} \Big)
    \quad\text{}\\
  (p_n(x))'      &=        \underbrace{\frac{f^{(0)}(x_0)}{0!} \cdot 0 \cdot (x-x_0)^{0-1}}_{0} + \sum_{k=1}^n \Big( \frac{f^{(k)}(x_0)}{k!} \cdot k \cdot (x-x_0)^{k-1} \Big)
    \quad\text{}\\
  (p_n(x))'      &=        \sum_{k=1}^n \Big( \frac{f^{(k)}(x_0)}{k!} \cdot k \cdot (x-x_0)^{k-1} \Big)
    \quad\text{}\\
  (p_n(x))'      &=        \sum_{k=1}^n \Big( \frac{f^{(k)}(x_0)}{(k-1)!} \cdot (x-x_0)^{k-1} \Big)
    \quad\text{}\\
  (p_n(x))'      &=        \sum_{k=0}^n \Big( \frac{f^{(k+1)}(x_0)}{k!} \cdot (x-x_0)^{k} \Big)
\end{aligned}
$$

Setze $x_0$ für $x$ ein:

$$
\begin{aligned}
  (p_n(x_0))'    &=        \sum_{k=0}^n \Big( \frac{f^{(k+1)}(x_0)}{k!} \cdot (x_0-x_0)^k \Big)
    \quad\text{}\\
  (p_n(x_0))'    &=        \sum_{k=0}^n \Big( \frac{f^{(k+1)}(x_0)}{k!} \cdot 0^k         \Big)
    \quad\text{}\\
  (p_n(x_0))'    &=        \frac{f^{(n+1)}(x_0)}{0!} \cdot 0^0 + \underbrace{\sum_{k=1}^n \Big( \frac{f^{(k+1)}(x_0)}{k!} \cdot 0^k \Big)}_{0}
    \quad\text{}\\
  (p_n(x_0))'    &=        \frac{f^{(n+1)}(x_0)}{1} \cdot 1
    \quad\text{}\\
  (p_n(x_0))'    &=        f^{(n+1)}(x_0)
\end{aligned}
$$

Da diese Annahme alle Bedingungen erfüllt, kann jede $n$-fach differnzierbare Funktion durch ein Polynom $p_n(x)$ approximiert werden.  


$${p_n(x) = \sum_{k=0}^n \frac{f^{(k)}(x_0)}{k!} \cdot (x-x_0)^k}$$  
heißt  **Taylorpolynom $n$-ten Grades**


<!--
#### Taylorformel

$$f(x) = p_n(x) + R_n(x,x_0)$$  
Dabei ist $R_n(x,x_0)$ die Abweichung des Taylorpolynoms $n$-ter Ordnung $p_n$ an der Stelle $x$ mit Mittelpunkt $x_0$ von $f$ im Punkt $x$.  
Wobei gilt: $\exists z: (x_0 - r) < z < (x_0 + r) : R_n(x,x_0) = \frac{f^{(n+1)}(z)}{(n+1)!} \cdot (x - x_0)^{(n+1)}$.  

#### Taylorreihe

$f(x) = \sum_{k=0}^\infin \frac{f^{(k)}(x_0)}{k!} \cdot (x-x_0)^k$  
-->

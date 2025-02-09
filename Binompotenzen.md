Gibt es eine Strucktur nach der sich $(x+y)^n$
in eine Summe umformen lässt?

Mal ein bisschen für $n=2$ probieren und beobachten:

$$
\begin{aligned}
&(x+y)^2 \\
\text{als Produkt geschrieben}\quad
  &(x+y) \cdot (x+y) \\
\text{am Ausmultiplizieren}\quad
  &x \cdot (x+y) + y \cdot (x+y)\\
\text{ausmultipliziert}\quad
  &xx + xy + yx + yy\\&\text{} \\
\text{Fakoren in Summanden geordnet}\quad
  &xx + xy + xy + yy \\
\text{gleiche Summanden ausklammern}\quad
  &xx + (xy + xy) + yy\\
  &xx + 2xy + yy\\
\text{Produkte als Potenzen schreiben}\quad
  &x^2 + 2xy + y^2
\end{aligned}
$$


Mal mal noch für $n=3$ probieren:

$$
\begin{aligned}
&(x+y)^3 \\
\text{als Produkt geschrieben}\quad
  &(x+y) \cdot (x+y)^2 \\
\text{Ergebnis von }(x+y)^2 \text{ nutzen}\quad
  &(x+y) \cdot (x^2 + 2xy + y^2)\\
\text{am Ausmultiplizieren}\quad
  &x \cdot (x^2 + 2xy + y^2) + y \cdot (x^2 + 2xy + y^2) \\
\text{ausmultipliziert}\quad
  &x^3 + 2x^2y + xy^2 + x^2y + 2xy^2 + y^3 \\
\text{Summanden nach Variablen} \\
\text{und Potenz sortiert}\quad
  &x^3 + 2x^2y + x^2y + xy^2 + 2xy^2 + y^3 \\
\text{gleiche Summanden ausklammern}\quad
  &x^3 + 3x^2y + 3xy^2 + y^3
\end{aligned}
$$


Mal mal noch für $n=4$ probieren:

$$
\begin{aligned}
&(x+y)^4 \\
\text{als Produkt geschrieben}\quad
  &(x+y) \cdot (x+y)^3 \\
\text{Ergebnis von }(x+y)^3 \text{ nutzen}\quad
  &(x+y) \cdot (x^3 + 3x^2y + 3xy^2 + y^3) \\
\text{am Ausmultiplizieren}\quad \\
  &x \cdot (x^3 + 3x^2y + 3xy^2 + y^3) + y \cdot (x^3 + 3x^2y + 3xy^2 + y^3) \\
\text{ausmultipliziert}\quad \\
  &x^4  + 3x^3y   + 3x^2y^2 + xy^3 + x^3y + 3x^2y^2 + 3xy^3   + y^4 \\
\text{Summanden nach Variablen} \\
\text{und Potenz sortiert}\quad \\
  &x^4 + 3x^3y + x^3y + 3x^2y^2 + 3x^2y^2 + 3xy^3 + xy^3 + y^4 \\
\text{gleiche Summanden ausklammern}\quad \\
\text{Produkte als Potenzen schreiben}\quad
  &x^4 + 4x^3y + 6x^2y^2 + 4xy^3 + y^4 \\
\end{aligned}
$$


Die Summe der Exponenten $b$ und $c$ eines jeweiligen eines Summanden $ax^by^c$
ist immer gleich der Potenz $n$ aus $(x+y)^n$, also $b+c=n$.

Beim Ausmultiplizieren werden im Prinzip alle Produkte als Pärchen
zwischen den Summanden der Faktoren gebildet.

Das Nichtnutzen der Potenzschreibweise und beibehalten der Ordnung der Faktoren
beim Ausmultiplizieren erleichtern die Erkenntnis:

$$
\begin{aligned}
(x+y)(x+y) &= x (x+y) + y (x+y) \\
           &= xx + xy + yx + yy \\
(x+y)(x+y)^2 &= (x+y) (xx + xy + yx + yy) \\
             &= xxx + xxy + xyx + xyy + yxx + yxy + yyx + yyy \\
\end{aligned}
$$


Es ist Klar, das jeder Summand der beim Ausmultiplizieren von $(x+y)^n$
$n$ Faktoren haben wird.
Beim Beibehalten der Reihenfolge der Faktoren, wird auch offensichtlich,
dass kein Summand einem anderen optisch gleich sein wird.
Sie werden selbst bei gleicher Anzahl von $x$ und somit auch $y$,
eine einzigartige Reihenfolge von $x$-en und $y$-s haben, was an der Ausmultiplikation
$(x+y)^{n+1} = (x+y) (x+y)^n = x(x+y)^n + y(x+y)^n$ liegt,
bei dem alle der Ausmultiplikation des linken Produkts entstehenden Summanden $x$ als Präfix
und alle der Ausmultiplikation des rechten Produkts entstehenden Summanden $y$ als Präfix haben werden.

Es folgt die Frage, wie viele Möglichkeiten der Reihenfolge es für $x$-e und $y$-s
für $x^by^c$ für ein festes $n$ mit $b+c=n$ gibt.

Die Frage nach wie viele Kombinationsmöglichkeiten von $x^by^c$ es für
ein festes $n$ und $b+c=n$ gibt,
kann mit dem [Binomialkoeffizienten](./Binomialkoeffizient.md) $\binom{n}{b}$ bzw. $\binom{n}{c}$ beantwortet werden,
was uns den gesuchten Koeffizienten $a$ aus $ax^by^c$ liefert.

Somit folgt

$$
(x+y)^n = \sum_{k=0}^{n} \binom{n}{k}x^ky^{n-k}
$$

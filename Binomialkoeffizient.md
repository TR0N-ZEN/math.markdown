Was ist die Anzahl an Möglichkeiten vier verschieden Dinge
in einem Regal mit vier Fächern anzuordnen?

Für das erste Ding gibt es vier verschiedenen wählbare Fächer.
Für das zweite Ding gibt es ein Fach weniger und
  somit eine Möglichkeit der Positionierung weniger, also drei.
Für das dritte Ding gibt es ein Fach weniger und
  somit eine Möglichkeit der Positionierung weniger, also zwei.
Für das vierte Ding gibt es ein Fach weniger und
  somit eine Möglichkeit der Positionierung weniger, also eine.

Das sind $4 \cdot 3 \cdot 2 \cdot 1$ Möglichkeiten.  
Für ein Produkt, deren Faktoren jeweils um eins fallen und dessen
größter Faktor $a$ ist schreiben wir verkürzend $a!$,
gelesen "*a Fakultät*",
bzw. ist $a!$ die Kurzschreibsweise von

$$
a \cdot (a-1) \cdot (a-2) \cdot ... \cdot 2 \cdot 1
$$


Also sind es kurz geschrieben $4!$ Möglichkeiten.

Für ein Regal mit $n$ Fächern und $n$ verschiedene Dinge,
gibt es $n!$ Möglichkeiten die Dinge in das Regal zu stellen.

Wenn ich nun die Anzahl der Möglichkeiten,
zwei verschiedene Dinge in ein Regal mit vier Fächern zu platzieren,
berechnen will, so fange ich an einzuräumen wie vorhin.

Für das erste Ding gibt es vier verschiedenen wählbare Fächer.
Für das zweite Ding gibt es ein Fach weniger und
  somit eine Möglichkeit der Positionierung weniger, also drei.
Jetzt bin ich fertig mit Einräumen und hab $4 \cdot 3$ Möglichkeiten.

Im Bezug auf $4! = 4 \cdot 3 \cdot 2 \cdot 1$ bezogen,
will ich nur die ersten zwei Faktoren haben.

$$
\underbrace{4 \cdot 3}_{2} \cdot ... \cdot 1
$$

Um die hinteren Faktoren zu entfernen steht einem die Division durch
diese Faktoren zur Verfügung.

$$
\frac{4 \cdot 3 \cdot 2 \cdot 1}{2 \cdot 1} = 4 \cdot 3
$$

Verallgemeinert gesagt ist die Anzahl der zu behaltenden größten Faktoren des Produkts,
die Anzahl der einzuräumenden Dinge.

Für $n$ Fächer und $k$ verschiedene einzuräumende Dinge

$$
\begin{aligned}
&\underbrace{n \cdot ... \cdot ?}_{k} \cdot ... \cdot 1 \\
=&\underbrace{(n-0) \cdot ... \cdot (n-(k-1))}_{k} \\
=&\frac
  { n \cdot ... \cdot (n-(k-1)) \cdot (n-k) \cdot ... \cdot 1 }
  { (n-k) \cdot ... \cdot 1 } \\
=&\frac
  { n! }
  { (n-k)! }
\end{aligned}
$$


Also in unserem Beispiel

$$
\begin{aligned}
&\frac
  { 4! }
  { (4-2)! } \\
=&\frac
  { 4 \cdot ... \cdot (4-(2-1)) \cdot (4-2) \cdot ... \cdot 1 }
  { (4-2) \cdot ... \cdot 1 } \\
=&4 \cdot ... \cdot (4-(2-1)) \\
=&4 \cdot ... \cdot (4-1) \\
=&4 \cdot ... \cdot 3 \\
=&4 \cdot 3 \\
\end{aligned}
$$


Man packe nun die verschiedenen Dinge in gleich aussehende, undurchsichtige Schachteln.
Ich könnte die nun irgendwie ins Regal gestellten Schachteln vertauschen ohne, dass es von außen ersichtlich wäre, ob ich sie vertauscht hab.

Für die Anzahl an Schachteln $k$, ergeben sich nun $k!$ gleich aussehende Anordnungen von Schachteln,
die sich aber nach entferenen der Schachteln um die verschieden Dinge,
als unterschiedliche Anordnungen entpuppen würden.

Die Anzahl der optisch ununterscheidbaren Anordnungen
von verschieden Objekten in Schachteln
ist somit

$$
\frac{n!}{(n-k)! \cdot k!}
$$

Dieser Ausdruck wird als *Binomialkoeffizient* bezeichnet und mit

$$
\binom{n}{k}
$$

,gesprochen "*$n$ über $k$*" oder "*$k$ aus $n$*",
abgekürzt.

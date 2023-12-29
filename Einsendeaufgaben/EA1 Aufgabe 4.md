## Aufgabe 4

Die Nachfrage $z$ nach Apfelsaft hängt vom Preis $x$ für Äpfel und vom Preis $y$ für Apfelsaft ab. Für $1\leq x,y \leq 5$ lautet die Nachfragefunktion $z$:

$z=f(x,y)= -\frac{1}{4}x + \ln y  -\frac{1}{2}(y-x)^2 + 15$

Bestimmen Sie wahre Aussagen:

| Teil | Lösung | Aussage                                                                                                                                              |
| ---- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| A    | X      | Die partielle Ableitung 1. Ordnung nach $x$ lautet: $f_x(x,y) = -x +y -\frac{1}{4}$                                                                  |
| B    | -      | Die Hesse-Matrix **H** der Nachfragefunktion $$f(x,y)$ lautet: $\textbf{H} (x,y) = \begin{pmatrix} -1 & -1 \\ -1 & ~~-1-\frac{1}{y^2}\end{pmatrix}$$ |
| C    | -      | Die partielle Ableitung 1. Ordnung nach $x$ lautet: $f_x(x,y) = x-y -\frac{1}{4}$                                                                    |
| D    | X      | Die Hesse-Matrix **H** der Nachfragefunktion $$f(x,y)$ lautet: $\textbf{H} (x,y) = \begin{pmatrix} -1 & 1 \\ 1 & ~~-1-\frac{1}{y^2}\end{pmatrix}$$   |
| E    | -      | Die Nachfragefunktion $f(x,y)$ hat bei einem Apfelpreis von $x=\frac{15}{4}$ und einem Apfelsaftpreis von $y=4$ einen stationären Punkt.             |

---

### Unteraufgabe A

#### Aufgabe:

Die partielle Ableitung 1. Ordnung nach $x$ lautet: $f_x(x,y) = -x +y -\frac{1}{4}$

#### Berechnung

**Ableitung**

$z=f(x,y)= -\frac{1}{4}x + \ln y -\frac{1}{2}(y-x)^2 + 15$\
$\Rightarrow -\frac{1}{4}x + \ln y -\frac{1}{2}(y^2 - 2xy + x^2) + 15$\
$\Rightarrow -\frac{1}{4}x + \ln y -\frac{1}{2}y^2 + xy - \frac{1}{2}x^2 + 15$\
$f_x(x,y) = -\frac{1}{4} + y - x$

Die Aussage ist wahr

---

### Unteraufgabe B

#### Aufgabe:

Die Hesse-Matrix **H** der Nachfragefunktion $f(x,y)$ lautet: 

$\textbf{H} (x,y) = \begin{pmatrix} -1 & -1 \\ -1 & ~~-1-\frac{1}{y^2}\end{pmatrix}$

#### Überlegungen:

Die Hesse-Matrix beinhaltet die partiellen Ableitungen der Funktion nach dem Schema:

$$\textbf{H} (x,y) = \begin{pmatrix} f_{xx} & f_{xy} \\ f_{yx} & f_{yy}\end{pmatrix}$$

Wir müssen also nur diese Ableitungen bilden.

#### Berechnung:

$f(x,y) = -\frac{1}{4}x + \ln y -\frac{1}{2}y^2 + xy - \frac{1}{2}x^2 + 15$

**1. Ableitungen**

$f_x(x,y) = -\frac{1}{4} + y - x$\
$f_y(x,y) = \frac{1}{y} - y + x = y^{-1} - y + x$

**2. Ableitungen**

$f_{xx}(x,y) = -1$\
$f_{xy}(x,y) = f_{yx}(x,y) = 1$\
$f_{yy}(x,y) = -1 * y^{-2} -1 = -1 -\frac{1}{y^2}$

$\textbf{H} (x,y) = \begin{pmatrix} -1 & 1 \\ 1 & -1 -\frac{1}{y^2}\end{pmatrix}$

Die Aussage ist also falsch.

---

### Unteraufgabe C


#### Aufgabe:

Die partielle Ableitung 1. Ordnung nach $x$ lautet: $f_x(x,y) = x - y -\frac{1}{4}$

Die Aussage ist falsch, siehe A

---

### Unteraufgabe D

#### Aufgabe:

Die Hesse-Matrix **H** der Nachfragefunktion $f(x,y)$ lautet: 

$$\textbf{H} (x,y) = \begin{pmatrix} -1 & 1 \\ 1 & ~~-1-\frac{1}{y^2}\end{pmatrix}$$

Die Aussage ist wahr, siehe B

---

### Unteraufgabe E

#### Aufgabe:

Die Nachfragefunktion $f(x,y)$ hat bei einem Apfelpreis von $x=\frac{15}{4}$ und einem Apfelsaftpreis von $y=4$ einen stationären Punkt.

#### Überlegungen:

Stationäre Punkte liegen da, wo die partiellen Ableitungen 1. Ordnung für die jeweiligen Faktoren gleich 0 sind.

Die Ableitungen haben wir bereits in B berechnet:

$f_x(x,y) = -\frac{1}{4} + y - x$\
$f_y(x,y) = \frac{1}{y} - y + x = y^{-1} - y + x$

Einsetzen:

$f_x(\frac{15}{4},4) = \frac{1}{4} + 4 - \frac{15}{4} = 0.5$\
$f_y(\frac{15}{4},4) = \frac{1}{4} - 4 + \frac{15}{4} = 0$

Für die 1. Ableitung nach x wird beim Einsetzen von x und y das Ergebnis $\neq 0$, der Punkt ist also kein stationärer Punkt und die Aussage ist falsch.
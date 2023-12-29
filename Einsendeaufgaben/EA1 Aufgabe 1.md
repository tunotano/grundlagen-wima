## Aufgabe 1

Bestimmen Sie wahre Aussagen:

| Teil | Lösung | Aussage                                                                                                                                                                       |
| ---- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| A    | -      | Gegeben sei die Gewinnfunktion $G(x)= - 0.02x^2 + 6x - 200$, wobei $x$ die herzustellende Menge angibt $(x\geq 0)$. Dann liegt an der Stelle $x_0=125$ ein Gewinnmaximum vor. |
| B    | -      | Für alle $a,b \in \mathbb{R}$ mit $a,b \geq 0$ gilt: $`\| \left( 2a, 2b\right) ^T\| = 4\cdot \|\left(a, b \right)^T\|`$                                                       |
| C    | X      | Gegeben sei die Gewinnfunktion $G(x)= - 0.02x^2 + 6x - 200$, wobei x die herzustellende Menge angibt ($x\geq 0$). Dann liegt an der Stelle $x_0=150$ ein Gewinnmaximum vor.   |
| D    | X      | Im Gewinnmaximum $\left(x_0, G(x_0)\right)$ stimmt der Grenzerlös $E'(x_0)$ mit den Grenzkosten $K'(x_0)$ überein.                                                            |
| E    | X      | $\| \left( 3, -5, -1, 1\right) ^T\| = \|\left(-4, 2, 4 \right)^T\|$                                                                                                           |

---

### Unteraufgabe A

#### Aufgabe:

Gegeben sei die Gewinnfunktion $G(x)= - 0.02x^2 + 6x - 200$, wobei $x$ die herzustellende Menge angibt $(x\geq 0)$. Dann liegt an der Stelle $x_0=125$ ein Gewinnmaximum vor.

#### Überlegungen:

Ein Gewinnmaximum liegt dann vor, wenn die 1. Ableitung an einem gegebenen Punkt gleich 0 ist und die 2. Ableitung kleiner als 0.

#### Berechnung

**Ableitungen berechnen**

$G(x)= - 0.02x^2 + 6x - 200$\
$\Rightarrow G'(x) = -0.04x + 6$\
$\Rightarrow G''(x) = -0.04$

Ableitung 2 kleiner als 0 ist gegeben.

**1. Ableitung gleich 0 setzen**

$-0.04x + 6 = 0$\
$\Rightarrow 0.04x = 6$\
$\Rightarrow x = 150$

Ein Gewinnmaximum liegt also im Punkt $x_0 = 150$ vor, die Aussage ist daher falsch.

Zur Kontrolle: Einsetzen von 125 in G':\
$G'(125) = -0.04*125 + 6 = 1$

---

### Unteraufgabe B

#### Aufgabe:

Für alle $a,b \in \mathbb{R}$ mit $a,b \geq 0$ gilt: $\| \left( 2a, 2b\right) ^T\| = 4\cdot \|\left(a, b \right)^T\|$

#### Überlegungen:

Einfach mal Werte einsetzen?

Z.B. a = 1, b = 1

$\| \left( 2, 2\right) ^T\| = 4\cdot \|\left(1, 1 \right)^T\|$

Linke Seite:

$\| \left( 2, 2\right) ^T\| = \sqrt{(2)^2 + (2)^2} = \sqrt{8} = 2.83$

Rechte Seite:

$4\cdot \|\left(1, 1 \right)^T\| = 4 * \sqrt{(1)^2 + (1)^2} = 4 * \sqrt{2} = 5.66$

Die Aussage scheint also falsch zu sein.

Die richtige Aussage wäre wahrscheinlich eher: Für alle $a,b \in \mathbb{R}$ mit $a,b \geq 0$ gilt: $\| \left( 2a, 2b\right) ^T\| = 2\cdot \|\left(a, b \right)^T\|$

---

### Unteraufgabe C

#### Aufgabe

Gegeben sei die Gewinnfunktion $G(x)= - 0.02x^2 + 6x - 200$, wobei x die herzustellende Menge angibt (x\geq 0). Dann liegt an der Stelle $x_0=150$ ein Gewinnmaximum vor.

#### Lösung

Die Aussage ist wahr, siehe A

--- 

### Unteraufgabe D

#### Aufgabe:

Im Gewinnmaximum $\left(x_0, G(x_0)\right)$ stimmt der Grenzerlös $E'(x_0)$ mit den Grenzkosten $K'(x_0)$ überein.

#### Überlegungen:

Das sollte so stimmen?

---

### Unteraufgabe E

#### Aufgabe:

$\| \left( 3, -5, -1, 1\right) ^T\| = \|\left(-4, 2, 4 \right)^T\|$

#### Überlegungen:

Die Aufgabe fragt, ob die Länge des Vektors links mit der Länge des Vektors rechts übereinstimmt.

#### Berechnung:

$\| \left( 3, -5, -1, 1\right) ^T\| = \sqrt{(3)^2 + (-5)^2 + (-1)^2 + (1)^2} = 6$\
$\|\left(-4, 2, 4 \right)^T\| = \sqrt{(-4)^2 + (2)^2 + (4)^2} = 6$

Die Aussage ist also wahr

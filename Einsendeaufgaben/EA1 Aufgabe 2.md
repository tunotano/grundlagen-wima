## Aufgabe 2

Gegeben sei die Funktion $f(x)= (x^2+5) \cdot (x+3)^2$

Bestimmen Sie wahre Aussagen:

| Teil | Lösung | Aussage                                                          |
| ---- | ------ | ---------------------------------------------------------------- |
| A    | -      | Die Funktion $f$ hat ein lokales Maximum an der Stelle $x_0=-3$. |
| B    | -      | Die Funktion $f$ hat ein lokales Maximum an der Stelle $x_0=3$.  |
| C    | -      | Die 1. Ableitung der Funktion $f$ lautet: $f'(x)=4x^3+18x+10$.   |
| D    | X      | Die Funktion $f$ hat ein lokales Minimum an der Stelle $x_0=-3$. |
| E    | X      | Es gilt: $f(-3)=0$.                                              |

---

### Unteraufgabe A

#### Aufgabe:

Die Funktion $f$ hat ein lokales Maximum an der Stelle $x_0=-3$.

#### Überlegungen:

Wenn die Funktion ein lokales Maximum an einer Stelle haben soll, dann muss gelten: 
- die 1. Ableitung in dem Punkt 0 sein
- die 2. Ableitung muss kleiner als 0 sein

#### Berechnung:

**Funktion ausschreiben**

$f(x) = (x^2 + 5) * (x + 3)^2$\
$\Rightarrow f(x) = (x^2 + 5) * (x^2 + 6x + 9)$\
$\Rightarrow f(x) = x^4 + 6x^3 + 9x^2 + 5x^2 + 30x + 45$\
$\Rightarrow f(x) = x^4 + 6x^3 + 14x^2 + 30x + 45$

**1. Ableitung bilden**

$f(x) = x^4 + 6x^3 + 14x^2 + 30x + 45$\
$\Rightarrow f'(x) = 4x^3 + 18x^2 + 28x + 30$

**Einsetzen**\
$f'(-3) = 4*(-3)^3 + 18*(-3)^2 + 28*(-3) + 30 = 0$

Die 1. Ableitung ist 0, es liegt also ein Extrempunkt vor. Wir müssen jetzt noch die 2. Ableitung bilden, um zu prüfen, welche Art von Extrempunkt.

**2. Ableitung bilden**

$f'(x) = 4x^3 + 18x^2 + 28x + 30$
$\Rightarrow f''(x) = 12x^2 + 36x + 28$

**Einsetzen**

$f''(-3) = 12(-3)^2 + 36*(-3) + 28 = 28$

Die 2. Ableitung ist größer als 0, der Extremwert ist also ein Minimum. Die Aussage ist daher falsch.

---

### Unteraufgabe B

#### Aufgabe:

Die Funktion $f$ hat ein lokales Maximum an der Stelle $x_0=3$.

#### Überlegungen:

Wie A

#### Berechnung:

**Einsetzen in 1. Ableitung**

$f'(3) = 4*3^3 + 18*3^2 + 28*3 + 30 = 0$

Die 1. Ableitung ist nicht 0, der Wert ist also keine Extremstelle und die Aussage falsch.

---

### Unteraufgabe C

#### Aufgabe

Die 1. Ableitung der Funktion $f$ lautet: $f'(x)=4x^3+18x+10$.

#### Lösung

Die Aussage ist falsch, siehe A bzw. [Wolfram Alpha](https://www.wolframalpha.com/input?i=derivate+f%28x%29+%3D+%28x%5E2%2B5%29%28x%2B3%29%5E2)

---

### Unteraufgabe D

#### Aufgabe:

Die Funktion $f$ hat ein lokales Minimum an der Stelle $x_0=3$.

#### Überlegungen:

Siehe A, die Aussage ist wahr.

---

### Unteraufgabe E

#### Aufgabe:

Es gilt: $f(-3)=0$.

#### Berechnung:

$f(x)= (x^2+5) * (x+3)^2$\
$\Rightarrow f(-3) = (-3^2+5) * (-3+3)^2 = 0$

Die Aussage ist wahr
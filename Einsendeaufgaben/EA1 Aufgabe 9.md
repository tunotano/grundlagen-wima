## Aufgabe 9

Zur Bestimmung des maximalen Gewinns für die Herstellung der beiden Produkte $P_1$ und $P_2$, wobei $x_1$ die herzustellende Menge von $P_1$ und $x_2$ die herzustellende Menge von $P_2$ bezeichnet, sei folgendes lineares Programm gegeben:

|        |     |     |                  |     |              |        |      |         |
| ------ | --- | --- | ---------------- | --- | ------------ | ------ | ---- | ------- |
| max    |     |     | $\frac{4}{5}x_1$ | $+$ | $2x_2$       |        |      |         |
| u.d.N. |     |     | $x_1$            | $+$ | $2x_2$       | $\leq$ | $40$ | $(1)$   |
|        |     |     | $2x_1$           | $+$ | $x_2$        | $\leq$ | $24$ | $(2)$   |
|        |     |     | $x_1$            |     |              | $\leq$ | $10$ | $(3)$   |
|        |     |     |                  |     | $x_1$, $x_2$ | $\geq$ | $0$  | $(NNB)$ |

Lösen Sie das obenstehende lineare Programm und geben Sie als Ergebnis den maximalen Gewinn in Dezimalschreibweise an.

---

**Überlegungen**

Genereller Ablauf:
1. Zielfunktion in Nullform bringen
2. Nebenbedingungen zu Gleichungen überführen durch Einführen von Schlupfvariablen
3. Simplex-Tabelle erstellen

**Berechnung**

Zielfunktion in Nullform bringen

$Z = \frac{4}{5}x_1 + 2x_2$\
$\Rightarrow Z - \frac{4}{5}x_1 - 2x_2 = 0$

Nebenbedingungen zu Gleichungen überführen

Nebenbedingung 1:

$x_1 + 2x_2 + x_3 = 40$

Nebenbedingung 2:

$2x_1 + x_2 + x_4 = 24$

Nebenbedingung 3:

$x_1 + x_5 = 10$

Bedingungen $x_1, x_2, x_3, x_4, x_5 \geq 0$

Simplex-Tabelle:

| Z   | $x_1$          | $x_2$ | $x_3$ | $x_4$ | $x_5$ | RHS |
| --- | -------------- | ----- | ----- | ----- | ----- | --- |
| 1   | $-\frac{4}{5}$ | -2    | 0     | 0     | 0     | 0   |
|     | 1              | 2     | 1     | 0     | 0     | 40  |
|     | 2              | 1     | 0     | 1     | 0     | 24  |
|     | 1              | 0     | 0     | 0     | 1     | 10  |

Basisvariablen: $x_3$, $x_4$, $x_5$\
Nichtbasisvariablen: $x_1$, $x_2$

Merke: Nichtbasisvariablen (in der Simplextabelle) sind stets 0 $\Rightarrow x_1 = 0, x_2 = 0$

**Pivot-Element bestimmen**

Pivotspalte: Spalte mit kleinster Zahl in Zielfunktionszeile

Pivotzeile: Zeile mit kleinstem Quotienten aus RHS und Wert der Pivotspalte

Pivotspalte: $x_2$ (weil $-2 < -\frac{4}{5}$)

Pivotzeilenwerte

Zeile 1: $40 / 2 = 20$\
Zeile 2: $24 / 1 = 24$\
Zeile 3: $10 / 0 = 0$

Zeile 3 fällt weg, Pivot muss positiv sein

Pivotzeile: Zeile 1

![](images/9Pivot1.png)

**Umrechnung der Tabelle mit Gaußschem Eliminationsverfahren**

| Z   | $x_1$          | $x_2$ | $x_3$ | $x_4$ | $x_5$ | RHS |
| --- | -------------- | ----- | ----- | ----- | ----- | --- |
| 1   | $-\frac{4}{5}$ | -2    | 0     | 0     | 0     | 0   |
|     | 1              | 2     | 1     | 0     | 0     | 40  |
|     | 2              | 1     | 0     | 1     | 0     | 24  |
|     | 1              | 0     | 0     | 0     | 1     | 10  |

Pivotzeile durch Pivot-Element 2 teilen und Pivot-Spalte zur Einheitsspalte machen:

| Z   | $x_1$         | $x_2$ | $x_3$         | $x_4$ | $x_5$ | RHS |
| --- | ------------- | ----- | ------------- | ----- | ----- | --- |
| 1   |               | 0     |               |       |       |     |
|     | $\frac{1}{2}$ | 1     | $\frac{1}{2}$ | 0     | 0     | 20  |
|     |               | 0     |               |       |       |     |
|     |               | 0     |               |       |       |     |

Spalten und Zeilen mit 0en ausgehend vom Pivot-Element abschreiben:

| Z   | $x_1$         | $x_2$ | $x_3$         | $x_4$ | $x_5$ | RHS |
| --- | ------------- | ----- | ------------- | ----- | ----- | --- |
| 1   |               | 0     |               | 0     | 0     |     |
|     | $\frac{1}{2}$ | 1     | $\frac{1}{2}$ | 0     | 0     | 20  |
|     |               | 0     |               | 1     | 0     |     |
|     | 1             | 0     | 0             | 0     | 1     | 10  |

Restliche Zellen ausrechnen:

| Z   | $x_1$         | $x_2$ | $x_3$         | $x_4$ | $x_5$ | RHS   |
| --- | ------------- | ----- | ------------- | ----- | ----- | ----- |
| 1   | **A**         | 0     | **B**         | 0     | 0     | **C** |
|     | $\frac{1}{2}$ | 1     | $\frac{1}{2}$ | 0     | 0     | 20    |
|     | **D**         | 0     | **E**         | 1     | 0     | **F** |
|     | 1             | 0     | 0             | 0     | 1     | 10    |

Vorgehen: Alter Wert aus Zelle - (Wert aus Pivotspalte \* Wert aus Pivotzeile) / Pivotelement

$A: -\frac{4}{5} - \frac{(-2) * 1}{2} = \frac{1}{5}$\
$B: 0 - \frac{(-2) * 1}{2} = 1$\
$C: 0 - \frac{(-2) * 40}{2} = 40$\
$D: 2 - \frac{1 * 1}{2} = \frac{3}{2}$\
$E: 0 - \frac{2 * 1}{2} = -1$\
$F: 24 - \frac{40 * 1}{2} = 4$

| Z   | $x_1$         | $x_2$ | $x_3$         | $x_4$ | $x_5$ | RHS |
| --- | ------------- | ----- | ------------- | ----- | ----- | --- |
| 1   | $\frac{1}{5}$ | 0     | 1             | 0     | 0     | 40  |
|     | $\frac{1}{2}$ | 1     | $\frac{1}{2}$ | 0     | 0     | 20  |
|     | $\frac{3}{2}$ | 0     | -1            | 1     | 0     | 4   |
|     | 1             | 0     | 0             | 0     | 1     | 10  |

Basisvariablen: $x_2 = 20$, $x_4 = 4$, $x_5 = 10$\
Nichtbasisvariablen: $x_1 = 0$, $x_3 = 0$

Da die Zielfunktionswerte alle positiv sind, haben wir eine optimale Lösung gefunden.

$x_1 = 0$, $x_2 = 20$

Maximaler Wert = 40

Um zu überprüfen, dass es sich hier um eine Lösung handelt, können wir die Werte in die Restriktionen einsetzen:

R1: $0 + 2 * 20 \leq 40$\
R2: $0 + 20 \leq 24$\
R3: $0 \leq 10$

Die Restriktionen sind erfüllt und wie wir sehen ist R1 am Limit, weswegen hier nicht weiter optimiert werden kann.

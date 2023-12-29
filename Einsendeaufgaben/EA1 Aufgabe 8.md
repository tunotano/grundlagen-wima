## Aufgabe 8

Berechnen Sie $x \in \mathbb{R}$ und geben Sie die Lösung an:

```math
\begin{pmatrix} 8 & ~4 & ~1 & -1 \\ -2& ~5 & ~0 & ~2 \\ 3 & -6 & ~4 & ~4 \\ 0 & -2 & ~6 & ~0 \\ 7 & ~3 & ~2 & ~8 \end{pmatrix} \cdot \begin{pmatrix} 2 & -4 & ~6 & ~4 \\ 10 & ~5 & ~x & -2 \\ -2 & ~0 & -1 & ~0\\ 4 & ~2 & ~5 & ~8 \\ \end{pmatrix} = \begin{pmatrix} 50 & -14 & ~46 & ~16 \\ 54 & ~37 & ~3 & -2 \\ -46 & -34 & ~28 & ~56 \\ -32 & -10 & -8 & ~4 \\ 72 & 3 & 83 & 86 \end{pmatrix}
```

---

### Überlegungen

Der Wert (i, j) in der Ergebnis-Matrix ergibt sich durch die Summen der Produkte aller Werte der i-ten Zeile in Matrix 1 und j-ten Spalte in Matrix 2.

Z.B. Ergebnis-Matrix Zeile 4, Spalte 2, Wert = -10\
Berechnung durch Matrix 1 Zeile 4 und Matrix 2 Spalte 2:\
$(0 * -4) + (-2 * 5) + (6 * 0) + (0 * 2) = -10$

Gesucht wird x in Spalte 3 von Matrix 2, also könnte man Zeilen 1-5 der Matrix 1 mit Spalte 3 der Matrix 2 multiplizieren und mit dem Ergebnis in Matrix 3 vergleichen.

### Berechnung

Zeile 1 Matrix 1 \* Spalte 3 Matrix 2 = 46\
$(8 * 6) + (4 * x) + (1 * -1) + (-1 * 5) = 46$\
42 + 4*x = 46\
$\Rightarrow$ x = 1

oder 

Zeile 3 Matrix 1 \* Spalte 3 Matrix 2 = 28\
$(3 * 6) + (-6 * x) + (4 * -1) + (4 * 5) = 28$\
34 - 6x = 28\
$\Rightarrow$ x = 1

### Prüfen des Ergebnisses mit Code

```csharp

#r "nuget: MathNet.Numerics, 5.0.0"
using MathNet.Numerics.LinearAlgebra;

var matrix1 = new double[,]{{8,4,1,-1},{-2,5,0,2},{3,-6,4,4},{0,-2,6,0},{7,3,2,8}};
var matrix2 = new double[,]{{2,-4,6,4},{10,5,1,-2},{-2,0,-1,0},{4,2,5,8}};

var M = Matrix<double>.Build;
var m1 = M.DenseOfArray(matrix1);
var m2 = M.DenseOfArray(matrix2);

var result = m1.Multiply(m2);

Console.WriteLine("Matrix 1:");
Console.WriteLine(m1.ToMatrixString());
Console.WriteLine("Matrix 2:");
Console.WriteLine(m2.ToMatrixString());
Console.WriteLine("Matrix 1 * Matrix 2:");
Console.WriteLine(result.ToMatrixString());

```


Output:

```
Matrix 1:
 8   4  1  -1
-2   5  0   2
 3  -6  4   4
 0  -2  6   0
 7   3  2   8

Matrix 2:
 2  -4   6   4
10   5   1  -2
-2   0  -1   0
 4   2   5   8

Matrix 1 * Matrix 2:
 50  -14  46  16
 54   37   3  -2
-46  -34  28  56
-32  -10  -8   4
 72    3  83  86
```

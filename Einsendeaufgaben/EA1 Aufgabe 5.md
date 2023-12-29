## Aufgabe 5

Bestimmen Sie wahre Aussagen:

| Teil | Lösung | Aussage                                                                                                                                                                                    |
| ---- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| A    | -      | Bei einem monatlichen nominellen Zins von $1.8\%$ beträgt der nominelle Jahreszins kaufmännisch gerundet $7.2\%$.                                                                          |
| B    | X      | Bei einer nachschüssigen Zahlung von jeweils $1000$ Euro am Ende einer Zinsperiode und einem Aufzinsungsfaktor von $q = 1.01$ beträgt das Endkapital nach $3$ Jahren: $K_3 = 3030.1$ Euro. |
| C    | -      | Eine Maschine mit einem Anschaffungspreis von 60000 Euro wird über 5 Jahre arithmetisch degressiv abgeschrieben. Dann beträgt die Abschreibung im 4. Jahr: 4000 Euro.                      |
| D    | X      | Bei einem monatlichen nominellen Zins von 1.8% beträgt der nominelle Jahreszins kaufmännisch gerundet 21.6\%.                                                                              |
| E    | X      | Ein Kapital von 1000 Euro wird monatlich zu einem nominellen Zins von 1.5\% verzinst. Dann beträgt der effektive Jahreszins kaufmännisch gerundet 19.56\%.                                 |

---

### Unteraufgabe A

#### Aufgabe:

Bei einem monatlichen nominellen Zins von $1.8\%$ beträgt der nominelle Jahreszins kaufmännisch gerundet $7.2\%$.

#### Überlegungen:

Der nominelle Jahreszins wäre der monatliche nominelle Zins mal 12 Monate, also $1.8\% * 12 = 21.6\%$.

---

### Unteraufgabe B

#### Aufgabe:

Bei einer nachschüssigen Zahlung von jeweils $1000$ Euro am Ende einer Zinsperiode und einem Aufzinsungsfaktor von $q = 1.01$ beträgt das Endkapital nach $3$ Jahren: $K_3 = 3030.1$ Euro.

#### Überlegungen:

Formel ist: $\large{K_n = a * \frac{q^n-1}{i}}$

$a = 1000$\
$q = 1.01$\
$n = 3$\
$i = 0.01$

Das Ergebnis ist 3030.1, die Antwort ist also wahr.

**Lösung mit Code**

```csharp

double EndkapitalNachschüssigeKonstanteZahlung(double annuität, double zins, double jahre) 
{
    var q = 1 + zins; 
    var faktor = (Math.Pow(q, jahre) - 1)/zins;
    return annuität * faktor;
} 

var ergebnis = EndkapitalNachschüssigeKonstanteZahlung(1000, 0.01, 3);
ergebnis

```

Output:

```
3030.1000000000136
```

---

### Unteraufgabe C

#### Aufgabe:

Eine Maschine mit einem Anschaffungspreis von 60000 Euro wird über 5 Jahre arithmetisch degressiv abgeschrieben. Dann beträgt die Abschreibung im 4. Jahr: 4000 Euro.

#### Überlegungen:

Zur Wiederholung:
- lineare Abschreibung: Anschaffungspreis/Jahre der Abschreibung gibt den Abschreibewert
- geometrisch degressive Abschreibung: Prozentuelle Abschreibung (% muss gegeben sein)
- arithmetisch degressive Abschreibung: Bei n Jahren: Abschreibung 1. Jahr n Teile, 2. Jahr n-1 Teile etc. (digitale Abschreibung)

Nachdem keine Aussage über einen Restwert am Ende der Abschreibung gemacht wurde, gehe ich mal von 0 aus.

#### Lösung

- Abschreibung über 5 Jahre, also 5 + 4 + 3 + 2 + 1 = 15 "Teile"
- Gesamtsumme 60000, also 1 Teil: 60000/15 = 4000

| Jahr | Teile | Abschreibung | Rest  |
| ---- | ----- | ------------ | ----- |
| 1    | 5     | 20000        | 40000 |
| 2    | 4     | 16000        | 24000 |
| 3    | 3     | 12000        | 12000 |
| 4    | 2     | 8000         | 4000  |
| 5    | 1     | 4000         | 0     |

Die Antwort ist falsch. Der Restwert beträgt 4000 Euro, nicht die Abschreibung.

---

### Unteraufgabe D

#### Aufgabe:

Bei einem monatlichen nominellen Zins von $1.8\%$ beträgt der nominelle Jahreszins kaufmännisch gerundet $21.6\%$.

#### Überlegung

Sollte wahr sein, Begründung siehe A

---

### Unteraufgabe E

#### Aufgabe:

Ein Kapital von 1000 Euro wird monatlich zu einem nominellen Zins von 1.5\% verzinst. Dann beträgt der effektive Jahreszins kaufmännisch gerundet 19.56\%.

#### Überlegungen:

Wir können hier nicht so einfach die klassische Formel zum Berechnen vom effektiven Zins anwenden, weil wir den monatlichen nominellen Zins gegeben haben und nicht den nominellen Jahreszins.\
Wir können allerdings recht einfach den nominellen Jahreszins berechnen: $1.5\% * 12 = 18\%$

Formel: $\large{i_{eff} = (1 + \frac{i}{m})^m - 1}$

$m = 12$\
$i = 0.18$

#### Lösung:

Beim Einsetzen in die Formel ergibt der effektive Jahreszins $19.56\%$.

Man kann auch die Verzinsung berechnen:

Formel: $\large{K_n = (1 + \frac{i}{12})^{m * n} - 1}$

$m = 12$\
$n = 1$\
$i = 0.18$

Ergebnis: 1195.62, was bei 1000 Euro Startkapital einer Verzinsung von 19.56\% entspricht (1195.62 - 1000 = 195.62)

```csharp

var zins = 0.015;
var zinsperioden = 12;
var nominellerJahreszins = 12 * zins;
var betrag = 1000.0;
Console.WriteLine($"Nomineller Jahreszins: {nominellerJahreszins}");

double EffektiverJahreszins(double zins, double zinsperioden) 
{  
    var ergebnis = Math.Pow((1 + (zins/zinsperioden)),zinsperioden) - 1;
    var gerundet = Math.Round(ergebnis*100,2);
    return gerundet;
}

var effektiverJahreszins = EffektiverJahreszins(nominellerJahreszins, zinsperioden);
Console.WriteLine($"Effektiver Jahreszins: {effektiverJahreszins}");

double MonatlicheVerzinsung(double betrag, double zins, double zinsperioden)
{
    var wertInKlammer = 1 + (zins/12);
    var potenzZuKlammer = Math.Pow(wertInKlammer, zinsperioden);
    return betrag * potenzZuKlammer;
}
var monatlicheVerzinsung = MonatlicheVerzinsung(betrag, nominellerJahreszins, zinsperioden);
Console.WriteLine(monatlicheVerzinsung);

``` 

Output:

```
Nomineller Jahreszins: 0.18\
Effektiver Jahreszins: 19.56\
1195.6181714615338
```

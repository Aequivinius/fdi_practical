# FDI Practical US 1

|    ⏰ | what                                  |
| ---: | ------------------------------------- |
|   5' | Motivation SQM (it takes a long time) |
|  15' | Just SQM + Demo                       |
|  10' | SQM with modulo                       |
|   5' | Stellen                               |
|   5' | Aufgaben                              |

# Motivation

* Für's erste nichts mit Binär-System und $x \mod n$, sondern lediglich schnelles Potenzieren.
* Demonstration: It takes a long time

# Just SQM

* Wir berechnen $2^8 = 2 \times 2 \times 2 \times 2 \times 2 \times 2 \times 2 \times 2 $
* Wir wollen $252^9$ berechnen.

* Wir zerlegen den Exponenten in Potenzen der Basis $2$: $9 = 1 \cdot 2^0 + 0 \cdot 2^1 + 0 \cdot 2^2 + 1 \cdot 2^3$, und wissen, dass $252^9 = 252^{1 \cdot 2^0 + 0 \cdot 2^1 + 0 \cdot 2^2 + 1 \cdot 2^3} = 252^{2^0} \cdot 252^{2^3}$

| Koeffizient |   $2^x$   |                         $252^{2^x}$                          |                            result                            |
| :---------: | :-------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|      1      | $2^0 = 1$ |                        $252^1 = 252$                         |                            $252$                             |
|      0      | $2^1 = 2$ |               $252^2 = 252 \times 252 = 63504$               |                            $252$                             |
|      0      | $2^2 = 4$ |          $252^4 = 252^2 \times 252^2 = 4032758016$           |                            $252$                             |
|      1      | $2^3 = 8$ | $252^8 = 252^4 \times 252^4 = 16263137215612256256$ ($16 \times 10^{18}$) | $16263137215612256256 \times 252 = 4098310578334288576512$ ($4 \times 10^{21}$) |

* Was ist $9$ in Binärform?
* Aber die Zahlen sind immer noch verdammt groß

# SQM with modulo

* Erinnerung: `stupid_ex` und `better_ex`.
* Warum geht das? Das geht, weil $(a \times b) \mod m = \left( (a \mod m) \times (b \mod m)\right) \mod m $.
* Wir wollen $252^{473} \mod 1000$ berechnen. Das sind:
  * $473 = 1 \times 2^8 + 1 \times 2^7 + 1 \times 2^6 + 0 \times 2^5 + 1 \times 2^4 + 1 \times 2^3 + 0 \times 2^2 + 0 \times 2^1 + 1 \times 2^0 $
  * $473_{10} = 111011001_2$
  * etc. gem. Blatt

# Stellen

* Wie schnell wächst es?
* Wieviele Stellen hat eine binäre Repräsentation einer Zahl?
* Wie groß ist der größte Exponent in der Darstellung mit Koeffizienten?

# Notes

* did they have Lern-Checks before?
* they didn't have Quantoren
  * So my analysis wasn't sufficient

* actually they took much longer to do it?
* we didn't have a plan what to do when somebody is finished before
  * so they helped each other after that
* Question not clear

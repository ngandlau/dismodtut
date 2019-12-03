---
layout: post
title:  "Blatt 06 - Vollständige Induktion"
date:   2019-11-30 16:38:36 +0100
---

<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        inlineMath: [['$','$'], ['\\(','\\)']],
        processEscapes: true
      }
    });
    </script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.0/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>


## Tipp 1 

Siehe Post "Vollständige Induktion: Survival Guide".

## Tipp 2

In der _Induktionsvoraussetzung_ ist es manchmal nützlich und/oder sogar *notwendig*, dass wir wenn wir $k \rightarrow k+1$ zeigen wollen, wir in der Induktionsvoraussetzung annehmen, dass die gegebene Gleichung für alle $m\leq k$ gilt.

Was passiert hier? Sagen wir der Induktionsanfang ist $k=1$. Dann zeigen wir $k+1$, indem wir f.a. davorigen $k$'s $1, ...., k$ annehmen, dass die Induktionsvoraussetzung gilt. 

Wir nutzen also alle Schritte *davor*, um den jeweils nächsten zu zeigen.


## Tipp 3

Im Induktionsverweis verwenden wir am Besten folgende 3 Schritte: 

1. _Induktions*anfang*_: Hierfür wähle das kleinstmögliche $k$. Wenn in der Aufgabe z.B. steht, dass $k\in \mathbb{N}$, dann wähle $k=0$. Wenn wir eine Rekursionsgleichung haben wie z.B. $R_n = R_{n-1}+R_{n+2}$, dann benötigen wir *zwei* Rekursionsanfänge.


2. _Induktions*voraussetzung*_: Hier nehmen wir an, dass der Term, der in der Aufgabenstellung vorgegeben ist, für irgendwas gilt. Wobei wir *irgendwas* sinnvoll wählen müssen, wobei am Häufigsten (bei uns) die folgenden Möglichkeiten auftrete:
     * **Ein einzelnes $k$**: Blablabla gilt für ein beliebiges $k$ (mit $k \in \mathbb{N}$ oder $k\in \mathbb{N}_{>0}$ oder wie auch immer die Aufgabenstellung den Wertebereich definiert)
     * **Alle $k$'s davor**: Blablabla gilt für alle $m\leq k$. Hierbei nutzen wir alle vorherigen Schritte, um den jeweils nächsten $k+1$'ten Schritt zu zeigen.
     * **Bestimmte $k$'s vorher**: Blablabla gilt für ein beliebiges $k$ und $k-1$ und ... wobei [*hier vernünftigen Wertebereich einsetzen, je nach Rekursionsgleichung*]


3. _Induktions*schritt*_: Je nachdem was wir in der Induktionsvoraussetzung angenommen haben, sieht der Induktionsschritt z.B. $k \rightarrow k+1$ oder $(k, k-1)\rightarrow k+1$ oder .... usw .... aus.

## Tipp 4

Um zu zeigen, dass für einen Ausdruck eine bestimmte geschlossene Form $T_n$ gilt, sollte der Induktionsschritt ungefähr diesem Muster folgen:

$$
T_{n+1}=\text{Hier rekursiven Ausdruck einsetzen}=...\overset{IV}{=} ... = \text{zu zeigende geschlossene Form}
$$
















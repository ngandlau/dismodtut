---
layout: post
title:  "Blatt 13 - Nachtrag Aufgabe 4 b) ii)"
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


## Aufgabe 4 b) ii)

**Induktionsanfang** (n=0)
Wir betrachten die nicht-rekursive Definition der Klammersprache $D_1$ und das Wort $w$ der Länge $n=0$, also das Wort $w=\epsilon$. Es gilt (1) $|w|_a=|w|_z$=0 und (2) $|w'|_a \leq |w'|_u = 0$ für alle Präfixe $w'$ von $w=\epsilon$, da $\epsilon$ der einzige Präfix von $\epsilon$ ist.

**Induktionsvoraussetzung (IV)**
Sei $u\in D_1$ mit $|u|=n$ für $n \in \mathbb{N}$. Es gelte (1) $|u|_a=|u|_z$ und (2) $|u'|_a \geq |u'|_z$ für alle Präfixe $u'$ von $u$.

**Induktionschritt**
Betrachte das Wort $w\in D_1$ mit $|w|=n+1$ für $n \in \mathbb{N}$. Da $|w|>0$ und $w \in D_1$ muss $w$ durch **R1** oder **R2** entstanden sein (R1 und R2 sind in der rekursiven Definition der Klammersprache in der Aufgabenstellung definiert). Wir betrachten demnach zwei Fälle: Fall 1, wo $w$ durch R1 entstanden ist und Fall 2, wo $w$ durch R2 entstanden ist.

---

**Fall 1:** $w$ ist durch R1 entstanden.
Wenn $w$ durch R1 entstanden ist, dann ist $w = auz $ für irgendein $u \in D_1$. Wir überprüfen die zwei Bedingungen:

(1) Gilt $\|w\|_a = \|w\|_z$?

$$|w|_a = |auz|_a = |u|_a + 1 \overset{IV}{=} |u|_z + 1 = |auz|_z = |w|_z$$

Also ja.

(2) Gilt $\|w'\|_a >= \|w\|_b$ f.a. Präfixe $w'$ von $w$?**

Ja. Betrachte Präfixe $w'$ von $w$: 

* Präfix $w'=\epsilon$ und $w'=w$ sind trivial. Sowohl (1) als auch (2) (siehe Induktionsanfang) sind erfüllt. 

* Präfix $w'=au'$ für irgendeinen Präfix $u'$ von $u$: 
 
$$|w'|_a = |au'|_a = |u'|_a + 1 \overset{IV}{\geq} |u'|_z + 1 = |au'|_z \geq |w'|_z$$

Folglich $\|w\'\|_a \geq \|w\|_z$. 

---

Jetzt müssten wir noch den Fall 2 überprüfen, indem $w$ durch R2 entstanden ist. Die Argumentation verläuft analog, und ist als Aufgabe für zu Hause gedacht. 

Viel Erfolg.
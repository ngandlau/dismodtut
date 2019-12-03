---
layout: post
title:  "Vollständige Induktion: Survival Guide"
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


## Beweis durch vollständige Induktion

Im Tutorium habe ich erwähnt, wie man die Induktionsannahme und den Induktionsanfang korrekt wählt. Das ganze habe ich nochmal etwas ausführlicher (und hoffentlich verständlicher) anhand eines Beispiels zusammengefasst.

## Beispiel

Gegeben sei folgende Rekursionsgleichung:

$$
\begin{aligned}
R_0 & = 0 \\
R_1 & = 1 \\
R_2 & = 2 \\
R_n & = R_{n-1} + R_{n-3} \quad \forall n \in \mathbb{N}, n \geq 3
\end{aligned}
$$

Wir sollen zeigen, dass irgendeine geschlossene Form $T_n=...$ für alle $n\in \mathbb{N}$ gilt.

**Was ist der Rekursionsschritt?**

Ich fange bewusst mit der Frage nach dem Rekursionsschritt an: Denn wenn wir wissen, wie der Rekursionsschritt aussehen wird, wird es einfacher fallen, den richtigen Induktionsanfang und die richtige Induktionsannahme zu wählen.

Wir haben den rekursiven Aufruf gegeben: $R_n = R_{n-1} + R_{n-3}$. Um also den $n$'ten Term zu berechnen, benötige ich $R_{n-1}$ und $R_{n-3}$.

Der Rekursionsschritt soll uns zu einem $n+1$ führen, also hat er die Form

$$
.... \rightarrow n+1 
$$

Was steht auf der linken Seite? Überlegen wir uns, was wir für $R_{n+1}$ benötigen. Wir betrachten dafür den gegebenen rekursiven Aufruf für $n+1$:

$$
R_{n+1}=R_{n+1-1}+R_{n+1-3}=R_{n}+R_{n-2}
$$

Um also $R_{n+1}$ zu berechnen, benötige ich $R_n$ und $R_{n-2}$. Deswegen ist mein Rekursionsschritt

$$
\boxed{
(n-2, n) \rightarrow n+1
}
$$

---

**Was ist unser Rekursionsanfang?**

Bei der Induktion machen wir, wie oben festgestellt, Induktionschritte der Form 

$$(n-2, n) \rightarrow n+1$$

Der erste mögliche Induktionsschritt ist der, wo $n-2=0$ ist, denn erst ab $R_0$ ist meine Rekursionsgleichung definiert. Damit ergibt sich $n-2=0 \Leftrightarrow n=2$ der kleinstmögliche Induktionsschritt:

$$(n-2, n) \rightarrow n+1  \quad \Longleftrightarrow \quad  (0, 2) \rightarrow 3$$

Für diesen Induktionsschritt benötigen wir also $R_0$ und $R_2$ um $R_3$ zu folgern. Das ist aber dann genau mein Rekursionsanfang!

$$
R_0 = 0 = \text{Vergleichen mit dem was rauskommt für }T_0 \\
R_2 = 2 = \text{Vergleichen mit dem was rauskommt für }T_2
$$

Reicht das? Noch nicht ganz: Wir hätten ein Problem, wenn wir auf $R_4$ folgern sollten, denn für $R_4$ gilt

$$R_4 = R_{4-1} + R_{4-3} = R_3 + R_1$$

Wir benötigen also für $R_4$ die Ergebnisse von $R_3$ und $R_1$. Das Ergebnis von $R_3$ erhielten wir durch den Induktionsschritt $(0, 2) \rightarrow 3$ mit Hilfe von $R_0, R_2$, die wir vorher händisch gezeigt haben. Das ist also kein Problem.

Allerdings können wir das Ergebnis von $R_1$ nicht durch einen Induktionsschritt herleiten, denn das würde unseren Wertebereich sprengen. Der Induktionsschritt hin zu $n+1=1$ sähe nämlich so aus:

$$(n-2, n) \rightarrow n+1 \quad \Longleftrightarrow \quad (-2,0) \rightarrow 1$$ 

Es gibt kein $R_{-2}$! Also müssen wir $R_1$ ebenfalls as Rekursionsanfang wählen.

Wir benötigen also insgesamt 3 Rekursionsanfänge:

$$
\boxed{
\begin{aligned}
R_0 = 0 = \text{Vergleichen mit dem was rauskommt für }T_0 \\
R_1 = 1 = \text{Vergleichen mit dem was rauskommt für }T_1 \\
R_2 = 2 = \text{Vergleichen mit dem was rauskommt für }T_2 \\
\end{aligned}
}
$$

---

**Was ist die Rekursionsannahme?**

Wir haben vorhin gesehen, dass Induktionsschritte die Form 

$$(n-2,n) \rightarrow n+1$$

haben. Also wird, wie auch oben gezeigt, die Rechnung im Induktionsschritt ungefähr so aussehen:

$$
R_{n+1}
= R_{n} + R_{n-2}
\overset{Ind.Annahme}{=} ... = T_{n+1}
$$

Wir benötigen also $R_n$ und $R_{n-2}$ um $R_{n+1}$ zu folgern. Naja, dann nehmen wir das doch an:

$$
\text{Ind.Annahme:} \quad 
\text{Für ein beliebiges n}\in \text{Wertebereich sei } T_n=... \text{ und } T_{n-2} \text{ wahr}. 
$$

Was ist nun der **Wertebereich** von $n$? Nach Definition von $T_n$ ist $T_n$ f.a. $n\in \mathbb{N}$ definiert. Also können wir $T_0$ und alles danach folgende $T_1, T_2, \dots$ berechnen. Da wir aber für den Rekursionsschritt ein $n$ benötigen, für das $T_n$ und $T_{n-2}$ existiert, gilt im "worst-case":

$$
T_{n-2}=T_{0} \quad \Longleftrightarrow \quad n-2 = 0 \quad \Longleftrightarrow \quad n=2
$$

Also erhalten wir die Induktionsannahme mit folgendem Wertebereich:

$$
\text{IA:} \quad 
\boxed{
\text{Für ein beliebiges n}\in \mathbb{N} \text{ mit } n\geq2 \text{ sei }  T_n=\dots \text{ und } T_{n-2}=\dots \text{ wahr}. 
}
$$


---
layout: post
title:  "Blatt 07 - Graphen-Induktionsbeweis"
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


## Lösung zu Aufgabe 7.3 b

Wir betrachten den Graphen $G_n=(V_n, E_n)$, wobei nach der Definition in der Aufgabenstellung $\|V_n\|=2n$.

Zu zeigen ist, dass der in der Aufgabenstellung angegebene ALG alle Graphen $G_n$ mit $n \in \mathbb{N}_{>0}$ mit genau $n$ Farben färbt.

<img src="{{site.baseurl}}/assets/b7_a3_1.png">
<img src="{{site.baseurl}}/assets/b7_a3_2.png">

Insgesamt wurden damit die Knoten in Schicht $n+1$ mit Farbe $n+1$ gefärbt, sodass der Graph $G_{n+1}$ insgesamt mit $n+1$ Farben gefärbt wurde. Und das war eben zu zeigen.
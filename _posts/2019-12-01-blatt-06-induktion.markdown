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

## Tipps

**Tipp 1** Wenn in einer Rekursionsgleichung $R_n$ der $n$'te Term abhängig ist von mehreren vergangen Werten, z.B. von $R_{n-1}, R_{n-4}$ wie in $R_n = 5 + R_{n-1} - R_{n-4}$, dann muss man 

* $R_{n-1}, R_{n-4}$ in der _Induktionsvoraussetzung_ erwähnen. Also irgendwas soll für $R_{n-1}, R_{n-4}$ gelten.
* Da wir von $R_{n-1}, R_{n-4}$ auf $R_n$ schließen, ist der Induktionsschritt sowas wie $(k, k-3) \rightarrow k+1$.

**Tipp 2** In der _Induktionsvoraussetzung_ ist es manchmal nützlich und/oder sogar *notwendig*, dass wir wenn wir $k \rightarrow k+1$ zeigen wollen, wir in der Induktionsvoraussetzung annehmen, dass die gegebene Gleichung für alle $m\leq k$ gilt.

Was passiert hier? Sagen wir der Induktionsanfang ist $k=1$. Dann zeigen wir $k+1$, indem wir f.a. davorigen $k$'s $1, ...., k$ annehmen, dass die Induktionsvoraussetzung gilt. 

Wir nutzen also alle Schritte *davor*, um den jeweils nächsten zu zeigen.




















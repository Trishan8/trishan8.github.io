---
title: "Cohomology of Eilenberg-Maclane Spaces"
description: "Nothing as such"
date: 2025-03-30
series: ["Steenrod algebra and spectral sequences"]
series_order: 3
---
{{< katex >}}

## Introduction

<!-- Why do we care about -->


Our goal is to show that $$ \mathcal{A} = \text{colim } H^{n+\ast}(K(Z_2,n);Z_2)$$

Let, $\iota_n$ be the fundamental class we define a map $\mathcal{A}\to H^{\ast}(K(Z_2,n),Z_2)$ by $Sq^I \mapsto Sq^I(\iota_n)$. We will show this is an isomorphism for degree $< 2n$. 

For this we will use *Serre spectral sequence*. There is nothing very deep about Serre spectral sequences, one can look at [this](https://trishan8.github.io/talk_5.html) for introductory parts and a few applications. The main take out from that would be the following theorem, 

> <a>Serre Spectral Sequence:</a> For a fibration $F \hookrightarrow E \to B$ there is a Spectral sequence $E^{p,q}$ with with the $E_2$ page looks like $$E_2^{p,q}= H^p(B;H^q(F))$$ and this spectral sequnce converges to $H^{p+q}(E)$.

<a style="color:yellow">Few terminologies</a>

- There is a special differential $\tau = d_n : E_n^{0,n-1}\to E^{n,0}_n$ is called the *transgression*.
- If $d_i(x)=0$ for $i<n$ and $d_n(x)=\tau(x)\neq 0$ then call $x$ transgressive.
- The steenrod squares commutes with the transgression. 

> <a style="color:yellow">Claim:</a> 



<head>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.7.1/katex.min.css">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.7.1/katex.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.7.1/contrib/auto-render.min.js"></script>
</head>
<body>
    <script>
      renderMathInElement(
          document.body,
          {
              delimiters: [
                  {left: "$$", right: "$$", display: true},
                  {left: "\\[", right: "\\]", display: true},
                  {left: "$", right: "$", display: false},
                  {left: "\\(", right: "\\)", display: false}
              ]
          }
      );
    </script>
</body>
</html>
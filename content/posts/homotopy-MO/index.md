---
title: "Thom-Splitting: Application of steenrod squares-1"
description: "Nothing as such"
date: 2025-04-30
series: ["Steenrod algebra and spectral sequences"]
series_order: 3
---

## Introduction

In this blog, we explore how Steenrod squares and the Steenrod algebra can be used to study problems in homotopy theory. Our main objective is to understand the **Thom splitting**, which states that the **Thom spectrum** $MO$ is weakly homotopy equivalent to the wedge sum  
$$
\bigvee_i \Sigma^i H\mathbb{Z}_2.
$$  
Here, $\mathbb{Z}_2$ refers to the field with two elements, not the 2-adic integers. Our goal is to construct a map
$$
f: MO \to \bigvee_i \Sigma^i H\mathbb{Z}_2,
$$
and then show that this map is a weak homotopy equivalence.

---

## Outline of the Argument

We will proceed in the following steps:

- First, compute $H^{\ast}(BO)$, where all (co)homology is taken with mod 2 coefficients.
- Dualize the cohomology ring to obtain a graded $Z_2$-algebra structure on $H_{\ast}(BO)$, which is free.
- Use the **Thom isomorphism** to identify $H_{\ast}(MO) \cong H_{\ast}(BO)$ as graded $\mathbb{Z}_2$-algebras.
- Show that $H_{\ast}(MO)$ is a **cofree graded comodule** over the dual Steenrod algebra $\mathcal{A}^{\ast}$.
- Dualizing again, we deduce that $H^{\ast}(MO)$ is a **free graded module** over the Steenrod algebra $\mathcal{A}$.


### Constructing the Map

From this structure, it follows that the graded homotopy group
$$
[MO, H\mathbb{Z}_2]
$$
is a free graded module over
$$
[H\mathbb{Z}_2, H\mathbb{Z}_2].
$$
Let $\{\alpha_i\}$ be a basis for this module. Then we obtain a canonical map of spectra:
$$
MO \to \prod_i \Sigma^{|\alpha_i|} H\mathbb{Z}_2 \to \bigvee_i \Sigma^{|\alpha_i|} H\mathbb{Z}_2,
$$
where the second map is the projection from the product to the wedge.

To show that this map is a weak homotopy equivalence, consider its **homotopy cofiber**. Since the map induces an isomorphism on mod-2 homology, the homology of the cofiber is trivial. By the **mod-2 Hurewicz theorem**, this implies the homotopy groups of the cofiber are also trivial. Hence, the map is a weak equivalence.

---

## Applications

The Thom splitting enables a straightforward computation of the ring $\pi_{\ast}(MO)$. Furthermore, by the **Thom–Pontryagin construction**, we know that $\pi_{\ast}(MO)$ is isomorphic to the ring of **unoriented cobordism classes**. Thus, the splitting allows us to explicitly compute this important cobordism ring.

## What is $MO$

Simply $MO$ is the Thom spectra corresponding to $BO$. 

### Little bit about Thom Spectra 

Let, $V \to X$ be a vector bundle over $X$(say it is a CW complex) and $S^V$ be the corresponding sphere bundle with the infinite section $s:X \to S^V$. Now we define Thom space, $$Th(V):= \text{Cofiber}({s})$$

<a style="color: yellow">Example:</a> The Thom space of the trivial bundle $X \times R^n \to X$ is $\Sigma^n X_{+}$.

We call a vector bundle *orientable* if there exist $\alpha \in H^{\dim V}(Th(V))$ such that it pulled back to a generator of $S^{\dim V}$ under the following pullback square. 
<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsNCxbMCwwLCJcXFJebiAiXSxbMSwwLCJWIl0sWzEsMSwiWCJdLFswLDEsInB0Il0sWzMsMl0sWzEsMl0sWzAsMV0sWzAsMiwiIiwwLHsic3R5bGUiOnsibmFtZSI6ImNvcm5lciJ9fV0sWzAsM11d&embed" width="304" height="304" style="border-radius: 8px; border: none;"></iframe>

If $V \to X$ and $W \to Y$ are two vector bundles we define $V \boxtimes W$ to be the the product-vector bundle on $X \times Y$. Now, $$Th(V \boxtimes W)= Th(V)\wedge Th(W)$$

----

With this we are ready to define $MO$. Recall that $BO(n)$ is the classifying space of all $n$-ranked real vector bundle. Let, $\gamma_n:EO(n)\to BO(n)$ be the uviversal tautological vector bundle. Then we define, $MO_n := Th(\gamma_n)$. Now note that, we have the following pull back diagram of vector bundles, <iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsNCxbMCwwLCJFTyhuKVxcb3BsdXMgXFxSIl0sWzEsMCwiRU8obisxKSJdLFsxLDEsIkJPKG4rMSkiXSxbMCwxLCJCTyhuKSJdLFszLDJdLFsxLDJdLFswLDFdLFswLDIsIiIsMCx7InN0eWxlIjp7Im5hbWUiOiJjb3JuZXIifX1dLFswLDNdXQ==&embed" width="475" height="304" style="border-radius: 8px; border: none;"></iframe>

This will give us a map from $Th(\gamma_n\oplus \varepsilon) \to Th(\gamma_{n+1})$, here $\varepsilon$ is the trivial line bundle. This is basically the structure map of the $MO$ spectra. 

**General construction:** In general if we have a map from a spectra $f:X\to BO$ then define $Th(f)_n = Th(f_n^{\ast}\gamma_n)$. For example :

 - The map $BSO \to BO$ gives rise to sthe spectrum $MSO$ whose homotopy ring is the un-orented cobordsim ring.
 - The map from $BU \to BO$ gives rise to $MU$ whose homotopy ring is the oriented cobordism ring. 
 - The map from $\ast \to BO$ gives rise to the sphere spectra whose homotopy ring gives rise to framed cobordism ring.

 ## Towards the main proof

 Recall that, $H_{\ast}(E;R) = [S,E\wedge HR]$ and $H^{\ast}(E;R)= [E, HR]$. Where $E$ is a spectra, $HR$ is the eilenberg maclane spectra and $S$ is the sphere spectra. Re call that $HR$ is a ring spectrum, if $E$ is a ring spectrum then $H_{\ast}(E;R)$ can be given a ring structure using the composition of following maps: 
 
 $$f\wedge g : S \to E \wedge HR \wedge E \wedge HR \simeq E \wedge E \wedge HR \wedge HR \to E \wedge HR$$ last map is smash of the multiplication maps of the ring spectrum. 

At the begining of the blog we have talked about this ring and the cohomology ring. 

### Step 1: $H_{\ast}(MO)$

  For the rest of the blog we will use $F$ for $Z/2Z$.

  > <a style="color:yellow"> Result 1:</a> As rings $H^{\ast}(BO(n);F)\simeq F[w_1,\cdots, w_n]$ where $w_i \in H^n(BO(n);F)$ is the whitney class of $BO(n)$.

To prove this consider the map $f : BO(1)^n \to BO(n)$ under $\gamma_1 \cdots \times \gamma_1 \to \gamma_n$. Note that $f^{\ast}$ is map from $H^{\ast}(BO(n))\to F[X]^{\otimes n} = F[x_1,\cdots, x_n]$ 

By the naturality of w.s-classes we get that $f^{\ast}(w(\gamma_n)) = w(\gamma_1 \times \cdots \gamma_1)$. Note that, $w(\gamma_1\times \cdots \gamma_1)= \sum s_i(x_1,\cdots,x_n)$ here $s_i$ means $i$-th symmetric polynomial. Thus the map $f^{\ast}$ is injective. Thus $H^{\ast}(BO(n))$ is isomorphic to the subring generated by the symmetric polynomial generated by $x_i$ which are precisely the whitney classes so the theorem is proved. 

---

Now we will dualize the above ap $f^{\ast}$ to get a map from $H_{\ast}(BO(1)^n) \to H_{\ast}(BO(n))$. Let, $y_i$ be the dual if $x^i$ then the dualize map is

 $$F[y_1,\cdots]^{\otimes n} \to  H_{\ast}(BO(n))$$ 

surjective where we have quoteinted by the symmetric polynomial. Now colimit commutes with homology (as it does with homotopy groups). Thus by taking colimit we get, $$H_{\ast}(BO) = \lim_n F[y_{i_1}\cdots y_{i_n}: i_1\leq \cdots \leq i_n] = F[y_1,y_2,\cdots]$$


> <a style="yellow">Thom isomorphism:</a> If $V \to X$ is a vector bundle of rank $n$ the following two spectra are weak equivalent in the category of specta $$HF \wedge Th(V) \equiv HF \wedge \Sigma^n X_{+} $$ 

Here we are not bothered about orientation. So what we get using Thom isomorphism is the following : 

$$[S, HF \wedge MO(n)] = [S, HF \wedge \Sigma^n BO(n)_{+}]$$ Taking the colimit over $n$ we get, 

$$H_{\ast}(MO;F) \simeq F[\tilde{y_i}: i \in \mathbb{N}]$$ here $\tilde{y}_i$ corresponds to the image of $y_i$ under the Thom isomorphism. Dualizing the above thing we get $$H^{\ast}(MO;F) = F[p_1,\cdots]$$ Here $p_i$ are duals of $\tilde{y}_i$.

### Step 2: $H^{\ast}(MO;F)$ as $\mathcal{A}$-module

For this step we need to understand what $\tilde{y}_i$ are. 

---

### Understanding $\tilde{y}_i$ and Steenrod Action

Recall that $H^{\ast}(BO;F)$ is generated by the Stiefel–Whitney classes $w_i$. The Steenrod algebra acts on these classes via the classical **Wu formulas**:
$$
Sq^j(w_i) = \sum_{k=0}^{j} \binom{i - j + k - 1}{k} w_{j-k}w_{i+k}.
$$
In particular, since $MO$ is obtained from $BO$ via the Thom isomorphism, the action of Steenrod squares on $H^{\ast}(MO)$ is determined by how they act on the Thom class.

Let $u \in H^n(Th(V))$ denote the Thom class of the bundle $V \to X$. The key relation is:
$$
Sq^i(u) = w_i(V) \cup u.
$$
Applying this to the universal bundle $\gamma_n$, we obtain
$$
Sq^i(u_n) = w_i(\gamma_n) \cup u_n,
$$
and hence, after taking colimits, we get for $MO$:
$$
Sq^i(u) = w_i \cup u.
$$

Thus the entire Steenrod algebra action on $H^{\ast}(MO)$ is generated by its action on the Thom class, and the multiplicative structure induced from $H^{\ast}(BO)$.

---

### Step 3: $H_{\ast}(MO)$ as $\mathcal{A}^{\ast}$-comodule

Dualizing the Steenrod action gives us the **coaction**
$$
\psi: H_{\ast}(MO) \to \mathcal{A}^{\ast} \otimes H_{\ast}(MO),
$$
turning $H_{\ast}(MO)$ into a comodule over the dual Steenrod algebra.  
By Thom isomorphism and the freeness of $H_{\ast}(BO)$, this coaction makes $H_{\ast}(MO)$ a **cofree graded comodule** over $\mathcal{A}^{\ast}$.

Consequently, the dual $H^{\ast}(MO)$ is a **free module** over $\mathcal{A}$.

---

### Step 4: The Splitting

From the above structure, we obtain:
$$
H^{\ast}(MO) \cong \mathcal{A} \otimes V
$$
for some graded vector space $V$. By the **Adams spectral sequence** argument, any spectrum whose mod-2 cohomology is a free $\mathcal{A}$-module splits as a wedge of Eilenberg–MacLane spectra. Therefore:
$$
MO \simeq \bigvee_i \Sigma^{|v_i|} H\mathbb{Z}_2,
$$
where $\{v_i\}$ corresponds to a basis of $V$.

This completes the proof of the **Thom splitting theorem**.

---

## Concluding Remarks

The use of Steenrod squares here is not merely computational — it provides a conceptual bridge between characteristic classes, cohomology operations, and stable homotopy theory. In upcoming blogs, we will explore:

- How to perform explicit Steenrod operations on Thom classes,
- The splitting for $MSO$ and $MU$,
- And the connection between Steenrod operations and **Adams spectral sequences** used in cobordism computations.

---

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
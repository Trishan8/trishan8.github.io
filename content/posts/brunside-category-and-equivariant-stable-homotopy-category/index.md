---
title: "Burnside Category and Equivariant stable homotopy category"
description: "Nothing as such"
date: 2025-03-21
tags: ["cohomology", "Algebra", "Algebraic Topology"] 
--- 
{{< katex >}}


It has been a long time since I wrote my first blog for this website. This time, I plan to continue writing regularly—at least once every two weeks. I'll mainly focus on topics I am currently learning or find fascinating. For now, I'll be writing a few blogs related to topics in equivariant homotopy theory.

## Why Equivariant Homotopy Theory?  

There are many reasons to study equivariant homotopy theory. One of the most famous and longstanding problems—the *Kervaire invariant problem*—was resolved using equivariant stable homotopy theory by M. Hill, M. Hopkins, and D. Ravenel. Their breakthrough was announced at the well-known [Atiyah 80+](https://www.maths.ed.ac.uk/~v1ranick/atiyah80.html) conference.  

However, my introduction to this subject was somewhat different. I participated in PCMI 2024 (organized by IAS), where I was introduced to $\mathbb{A}^1$-homotopy theory*. In a sense, this is a generalized form of homotopy theory, and the construction of the $\mathbb{A}^1$-homotopy category $\mathcal{H}_{k,\ast}$ is done in a highly formal setup. To better understand these formalisms, it helps to first study homotopy theories that can be approached in a more accessible way—equivariant homotopy theory being one such example. In particular, there is a connection between $G $-equivariant homotopy theory and $\mathbb{A}^1$-homotopy theory when $G$ is the Galois group of the field $k$.  

Moreover, equivariant homotopy theory has direct applications to geometric problems, such as equivariant $h$-cobordisms and related structures, which makes it even more important.




## Equivariant Stable Homotopy Category: $\text{Ho}(\mathcal{Sp}^G)$  

Just as in the non-equivariant setting, we have an equivariant stable homotopy category, and there are several models for this category. The objects in this category are called *spectra*. In equivariant homotopy theory, we mainly deal with *orthogonal $G$-spectra* (often referred to as *naive spectra*) or *genuine $G$-spectra*. However, in this blog, we may not go into the details of these spectra.  

Instead, we will consider the simplest possible model for $\text{Ho}(\mathcal{SP}^G)$. Let us begin with the category $\text{Top}_{G}$, which consists of $G$-spaces with morphisms given by equivariant continuous maps. If $f, g: X \to Y$ are two based $G$-maps between $G$-spaces, we say they are *$G$-equivariantly homotopic* (or *$G$-homotopic*) if there exists a $G$-equivariant map $H: X \wedge I \to Y$ (where $I$ has a trivial $G$-action) such that  

$$
H(x,0) = f(x), \quad H(x,1) = g(x), \quad \text{and} \quad H(\ast_X,t) = \ast_Y.
$$  

The *homotopy category* $\text{Ho}(\text{Top}_G)$ is then defined by formally inverting $G$-homotopy equivalences.  

To define the stable homotopy category, we need additional structure.  

### $G$-CW complexes

A $G$-CW complex is a space $X$ built as a colimit of $G$-spaces $X_n$, where $X_0$ is a discrete G-set and $X_n$ is obtained from $X_{n-1}$ by attaching cells of type $(G/H)\times D^n$ (H is not fixed). We can define weak equivalance of $G$-spaces. If $f:X\to Y$ is a map between two $G$-spaces then we call it $G$-weak equivalance if $f^H : X^H \to Y^H$ are weak equivalances for any $H \leq G$. Jut like non-equivarinat case we have,

> <a style="color:yellow">CW approximation Theorem:</a> There is a functor $\Gamma : Top_G \to G-CW$ along with a natural transformation $\gamma: 1_{Top_G} \Rightarrow \Gamma$ so that $\gamma(X)$ is weak equivalance for any $X \in Top_G$.

> <a style="color:yellow">Equivariant Whitehead Theorem:</a> If a map $f:X \to Y$ between two $G$-CW complex is a $G$-weak equivalance, it is a homotopy equivalance.


### Equivariant Homotopy Groups  

In the equivariant setting, we cannot define integer-graded homotopy groups as in the classical case because the sphere $S^n$ may not have a natural $G$-action for every $n$. Instead, we work with *faithful representations* of $G$. If $V$ is a faithful representation of $G$, the one-point compactification $S^V$ has a natural $G$-action, where $g \cdot \infty = \infty$.  

We define a suspension functor $\Sigma^V : \text{Top}_G \to \text{Top}_G$ by $X \mapsto S^V \wedge X$, and it follows that  

$$
S^V \wedge S^W \simeq S^{V \oplus W}.
$$  

> <a style="color:yellow">Equivariant Freudenthal Suspension Theorem:</a> Let $X$ be a $G$-CW complex and $Y$ a $G$-space. For any $G$-representations $V$ and $W$, the suspension map  $$ \Sigma^W: [S^V \wedge X , S^V \wedge Y] \to [S^{V \oplus W} \wedge X, S^{V \oplus W} \wedge Y]$$ is an isomorphism.  

Although we primarily focus on finite $G$-groups, for any compact Lie group $G$, there exists a *$G$-universe* $\mathcal{U}_G$, which contains every irreducible regular representation of $G$ as a direct summand. We define a category $s(G)$, where objects are finite-dimensional $G$-representations, and morphisms are given by inclusions.  

Using this structure, we define the *equivariant stable homotopy groups* by  

$$
[X,Y] = \text{colim } \Sigma^V[\Gamma X,Y]^G,
$$  

where the colimit is taken over inclusions in $s(G)$. With this, we define $\text{Ho}(\mathcal{SP}^G)$ as the category with objects given by $G$-spaces and morphisms defined by  

$$
\text{Ho}(\mathcal{SP}^G)(X,Y) = [X,Y].
$$  

<a style="color:yellow">Remark:</a> This homotopy category is equivalent to the category of *naive spectra* and it is equivalent to compact triangulated subcategory of stable homotopy category. However, this model is not the most useful for defining the equivariant stable homotopy category in practice. This category is known as Spanier-Whitehead category. For the sake of this blog we will denote this category as $Ho(Sp^G)$.

- This category is symmetric monoidal with respect to the smash product. 

**Draw-backs:** While this stable homotopy category is relatively easy to understand, many constructions such as pushouts, mapping cones, and other homotopy colimits may not always exist in this framework. This limitation motivates the search for better models of the homotopy category. However, different models present their own challenges. For instance, while the smash product is inherently well-defined in the original category, its existence and well-behaved properties are not always obvious in other models.


Whatever model we choose, it should come with a natural suspension functor $\Sigma$, and taking suspensions should not alter the class of morphisms. As we observed in the category we defined, we should have the equivalence  
$$ Ho(\mathcal{SP}^G) = Ho(\text{Top}_{G})[\Sigma^{-1}]. $$

With this we can define equivariant stable homotopy groups. For $X \in Top_G$ define $$\pi_k^G(X) = [S^k, X], k\geq 0$$ here $S^k$ comes with trivial $G$ action and $\pi_k^G(X) = [S^0,X\wedge S^{-k}]$ for $k<0$. 

## Burnside Category 

For a group $G$ we can define Burnside category $Burn_G$. The objects of this category is given by finite $G$-sets and morphisms are given by, 
$$Burn_G(S,T)= ( S\leftarrow U \rightarrow T )^{\wedge}$$ which is collection of such diagrams and under disjoint union we are taking the group completion. Here, composition are made by pullbacks as hown in the following diagram. 

<iframe class="quiver-embed" src="https://q.uiver.app/#q=WzAsNixbMCwyLCJTIl0sWzIsMiwiVCJdLFs0LDIsIlciXSxbMSwxLCJVIl0sWzMsMSwiViJdLFsyLDAsIlAiXSxbMywwXSxbMywxXSxbNCwxXSxbNCwyXSxbNSwzLCIiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNSw0LCIiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJkYXNoZWQifX19XSxbNSwwLCIiLDAseyJjdXJ2ZSI6Mn1dLFs1LDIsIiIsMix7ImN1cnZlIjotMn1dXQ==&embed" width="556" height="332" style="border-radius: 8px; border: none;"></iframe>

Note that $Burn_G(p,p)$ is abelian group generated by all finite $G$-sets. We know finite $G$-sets are disjoint union of the cosets $G/H$, thus this group is generated by cosets of the form $G/H$. We call this a Burnside group and denote it by $A(G)$. Infact it is a ring under direct product.

## Relation of $Ho(Sp^G)$ and $Burn_G$

We define a functor $\Phi: Burn_G \to Ho(Sp^G)$ that takes a finite $G$ set $S$ to $S_{+}$.  

- This is a map of Symmetric monoidal category. 
- This fuctor is fully faithful.
- The objects in $Burn_G$ are self dual. By the faithfull-ness of the above functor we get some objects of  $Ho(Sp^G)$ are dualizable. There is a more specific critation of  Spanier-Whitehead duality for the stable homotopy category.

The first point can be verified easily. For the second point we need to show $Burn_G(pt,pt)= \pi_0^G(S^0)$ and the third point follows from the second point. We will discuss how these are true in a upcoming blog. For that we need 

- Discussion of Macky functors
- Dual objects in $Ho(Sp^G)$
- Isotropic seperation sequence

<a style="color:yellow">Sketch of how we are going to use the above tools:</a> Firstly $S^0$ is the unital object in $Ho(Sp^G)$. The duality will  give us a map $$\chi (X): S^0 \to X \otimes DX \to DX \otimes X \to S^0$$ where the first map is coevolution and the last one is unital map. The induced map by $\Phi$ functor is actually the map $G/H \mapsto \chi(G/H_{+})$. We will show this is an isomorphism using Isotropic seperation sequence.

<html>
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




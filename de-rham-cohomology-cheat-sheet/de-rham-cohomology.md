# De Rham cohomology


Let $M$ be a smooth (often orientable, but not always) manifold of dimension $n$.


## Tangent bundle

**Definition:** The *tangent space* $T_pM$ at $p$ is defined as $$T_pM = \{\text{smooth paths }\alpha\colon(-1,1)\to M \mid 
\alpha(0)=p\}/\sim$$ where $\alpha\sim\beta$ iff $(\varphi\circ\alpha)'(0)=(\varphi\circ\beta)'(0)$ where $\varphi$ is some chart on a neighbourhood of $p$.

**Lemma:** $T_pM$ is a vector space of dimension $n$.

**Definition:** The *pushfoward* of a smooth map $f\colon M\to N$ of smooth manifolds is the map $f_*\colon T_pM\to T_{f(p)}N$ given by $f_*([\alpha])=[f\circ\alpha]$.

**Lemma:** Given a chart $(U,\varphi)$ around some point $p$ we have a basis of $T_pM$ consisting of elements $\frac{\partial}{\partial x_i}|_p = \varphi_*(e_i)$ where $\{e_i\}$ is the canonical basis of $\mathbb{R}^n$.

**Definition:** The *tangent bundle* $TM$ is defined as $\coprod_{p\in M}T_pM$.

**Lemma:** The map $\pi\colon TM\to M$ given by $\pi(T_pM)=p$ gives $TM$ the structure of a smooth vector bundle over $M$ of rank $n$.


## Cotangent bundle

**Definition:** The *cotangent space* $T^*_pM$ at $p$ is defined as the vector-space dual $(T_pM)^*$.

**Definition:** Given the basis $\left\{ \frac{\partial}{\partial x_i}|_p \right\}$ of $T_pM$ we have the dual basis $\{\mathrm{d}x^i|_p\}$ of $T^*_pM$ consisting of *differentials*.

**Definition:** The *pullback* of a smooth map $f\colon M\to N$ of smooth manifolds is the map $f^*\colon T^*_{f(p)}N\to T^*_pM$ given by $$f^*(\vartheta)\left(\sum_i\lambda_i\frac{\partial}{\partial x_i}|_p\right) = \vartheta\left(f_*\sum_i\lambda_i\frac{\partial}{\partial x_i}|_p\right).$$

**Example:** Let $f\colon M\to\mathbb{R}$ be smooth. Then $f_*\colon T_pM\to T_{f(p)}\mathbb{R}=\mathbb{R}$ and so $f_*\in T^*_pM$. Further, $f_*=\sum_i\frac{\partial\hat{f}}{\partial x_i}\mathrm{d}x^i|_p$ where $\hat{f}\colon\mathbb{R}^n\to\mathbb{R}$ is the local representation of $f$.

**Definition:** The *cotangent bundle* $T^*M$ is defined as $\coprod_{p\in M}T^*_pM$.

**Lemma:** The cotangent bundle is a smooth vector bundle of $M$ of rank $n$.


## Vector fields and tensors

**Definition/Lemma:** A section of a smooth vector bundle on $M$ is a *vector field* on $M$.

**Definition:** Given a vector space $V$ with basis $\{v_1,\ldots,v_n\}$ we define the *space of alternating $r$-tensors* as the vector space $\bigwedge^r V$ with basis $$\{v^*_{i_1}\wedge\ldots\wedge v^*_{i_r} \mid i_1 < \ldots < i_r\}$$ where the wedge product $\wedge$ satisfies $a\wedge b=-b\wedge a$ and $a\wedge a=0$.

**Note:** We can give a better definition using general tensors, but we don't. Just note that an element of $\bigwedge^r V$ is a multilinear $V^r\to\mathbb{R}$.

**Definition:** Given a smooth $f\colon M\to N$ of smooth manifolds we define, for all $r$, the *pullback* $f^*\colon\bigwedge^r(T_{f(p)}N)\to\bigwedge^r(T_pM)$ given by $$f^*(\vartheta)(X_1,\ldots,X_n)=\vartheta(f_*X_1,\ldots,f_*X_n)$$ where $X_i\in T_pM$.

**Definition:** The *(covariant) alternating $r$-tensor bundle* $\bigwedge^r TM$ is defined as $\coprod_{p\in M}\bigwedge^r(T_pM)$ and is a smooth vector bundle over $M$.


## Differential forms

**Definition:** A *differential $r$-form* is a smooth section of $\bigwedge^r TM$. The space of all differential $r$-forms on $M$ is denoted $\Gamma^r(M)$.

**Note:** A *differential $1$-form* is a smooth section of the cotangent bundle, and a differential $r$-form is in particular a map $M\to(T^*_pM)^r$.


**Definition:** Given a smooth section $X$ of $TM$ and $\omega\in\Gamma^r(M)$ we define the *contraction (with $X$)* as the differential $(r-1)$-form $i_X\omega$ given by $$(i_X\omega)(X_1,\ldots,X_{r-1})=\omega(X,X_1,\ldots,X_{r-1}).$$

**Lemma:** $i_X\circ i_X=0$.

**Lemma:** Let $\sigma\in\Gamma^r(M)$ and $\omega\in\Gamma^s(M)$. Then $$i_X(\sigma\wedge\omega)=(i_X\sigma)\wedge\omega+(-1)^r\sigma\wedge(i_X\omega).$$

**Definition:** Let $I=(i_1,\ldots,i_r)$. Then we write $\omega_I\mathrm{d}x^I$ to mean $\omega_{i_1\ldots i_r}\mathrm{d}x^{i_1}\wedge\ldots\wedge\mathrm{d}x^{i_r}$.

**Lemma:** For all $r$ there exist unique linear maps $\mathrm{d}^r\colon\Gamma^r(M)\to\Gamma^{r+1}(M)$ such that, for all $f\in\Gamma^0(M)$, $\omega\in\Gamma^r(M)$, and $\sigma\in\Gamma^s(M)$,

 - $\mathrm{d}^0f=f_*$;
 - $\mathrm{d}^{r+1}\circ\mathrm{d}^r=0$;
 - $\mathrm{d}^{r+s}(\omega\wedge\sigma)=\mathrm{d}^r\omega\wedge\sigma+(-1)^r\omega\wedge\mathrm{d}^s\sigma$.

Further, $\mathrm{d}$ is given by $\mathrm{d}(f\mathrm{d}x^I)=\mathrm{d}f\wedge\mathrm{d}x^I$.

**Lemma:** The differential $\mathrm{d}^r$ commutes with pullbacks, i.e. for smooth $f\colon M\to N$ and $\omega\in\Gamma^r(N)$ we have that $f^*\mathrm{d}^r\omega=\mathrm{d}^rf^*\omega$.

## Integration over top forms

**Definition:** Given an atlas $(U_\alpha,\varphi_\alpha)_{\alpha\in I}$ on a smooth manifold $M$, we say that $\{\psi_\alpha\}_{\alpha\in I}$ is a *corresponding partition of unity* if (for all $\alpha\in I$) all of the following hold:

 - $f_\alpha\colon M\to\mathbb{R}$ is smooth;
 - $\mathrm{supp}\,f_\alpha\subseteq U_\alpha$;
 - $\sum_{\alpha\in I}f_\alpha=1$.

**Definition:** A differential form is said to be a *top form* if it lives in the highest-degree non-zero $\Gamma^k(M)$, i.e. $\Gamma^{\dim M}(M)$ when $M$ is a smooth manifold.

**Definition:** Let $U\subset\mathbb{R}^n$ be open and $f\mathrm{d}x^1\wedge\ldots\wedge\mathrm{d}x^n$ a compactly-supported top form on $U$. Then we define $$\int_U f\mathrm{d}x^1\wedge\ldots\wedge\mathrm{d}x^n = \int_U f\mathrm{d}x_1\ldots\mathrm{d}x_n$$ where the right-hand side is Lebesgue integration.

**Definition:** Let $M$ be a smooth $n$-dimensional orientable manifold and $\omega\in\Gamma^n(M)$ a compactly-supported top form. Let $(U_i,\varphi_i)_{i=1,\ldots,m}$ be the charts corresponding to the support of $\omega$ (by compactness) and let $\{\psi_i\}$ be a corresponding partition of unity. Then we define $$\int_M \omega = \sum_{i=1}^m\int_{U_i}\psi_i\omega = \sum_{i=1}^m\int_{\varphi_i(U_i)}(\varphi_i^{-1})^*(\psi_i\omega).$$

**Definition:** Let $M$ be an orientable smooth $n$-manifold. Then a top form $\omega$ is said to be an *orientation form* if it is non-vanishing and positively-oriented at each point of $M$, i.e. its value evaluated at a positively-oriented basis at any point is positive.

**Lemma:** Let $M$ be an orientable smooth $n$-manifold. Then there exists an orientation form $\omega_0$. Further, $$\int_M\omega_0>0.$$


## De Rham cohomology

Let $M$ be a smooth orientable $n$-manifold.

**Definition:** The *de Rham complex* of $M$ is the cochain complex $(\Gamma^\bullet(M),\mathrm{d}^\bullet)$. The *de Rham cohomology* of $M$ is the cohomology of this complex, written $\mathrm{H}_{\text{dR}}^\bullet(M)$.

**Definition:** A differential $k$-form $\vartheta$ is said to be *closed* if $\mathrm{d}^k\vartheta=0$ (i.e. if it is a cycle) and *exact* if there exists some $(k-1)$-form $\omega$ such that $\vartheta=\mathrm{d}^{k-1}\omega$ (i.e. if it is a boundary).

**Lemma:** The pullback $f^*$ of a smooth $f\colon M\to N$ induces a map $f^*\colon\mathrm{H}_\text{dR}^\bullet(N)\to\mathrm{H}_\text{dR}^\bullet(M)$.

**Lemma:** The de Rham cohomology of $M$ is invariant under (smooth) homotopy, i.e. if $M\simeq N$ then $\mathrm{H}_\text{dR}^\bullet(M)\cong\mathrm{H}_\text{dR}^\bullet(N)$. In particular, if $f,g\colon M\to N$ are smooth and (smoothly) homotopic then $f^*=g^*$.

**Lemma:** Let $M$ be a smooth connected compact orientable $n$-manifold. Then integration of top forms gives an isomorphism $\int_M\colon\mathrm{H}_\text{dR}^n(M)\overset{\sim}{\to}\mathbb{R}$. If $M$ is instead non-orientable then $\mathrm{H}_\text{dR}^n(M)=0$


## Stokes' theorem

Let $M$ be a smooth orientable $n$-manifold.

**Definition:** Let $\sigma\colon\Delta_p\to M$ be a smooth singular $p$-simplex and $\omega\in\Gamma^p(M)$ a closed $p$-form. Then we define $$\int_\sigma\omega = \int_{|\Delta_p|}\sigma^*\omega$$ where the right-hand side is the integral of a top form over the submanifold (with corners) $|\Delta_p|\subset\mathbb{R}^p$. We can extend this linearly to any smooth $p$-chain $\sum_{i=1}^k\lambda_i\sigma_i$.

**Lemma:** Let $c$ be a smooth $p$-chain in $M$ and $\omega\in\Gamma^{p-1}(M)$. Then $$\int_{\partial c}\omega = \int_c\mathrm{d}\omega$$ where $\partial$ is the simplicial boundary map.

**Proof:** We only need to prove the statement for smooth $p$-simplices, since the result then follows by linearity, so let $\sigma$ be a smooth $p$-simplex. Now $$\int_\sigma\mathrm{d}\omega = \int_{\Delta_p}\sigma^*\mathrm{d}\omega = \int_{\Delta_p}\mathrm{d}\sigma^*\omega = \int_{\partial\Delta_p}\sigma^*\omega$$ by commutativity of the differential and pullbacks, and by definition. Next, using the definition of the coboundary map $\partial$ we see that $$\int_{\partial\Delta_p}\sigma^*\omega = \int_{\sum_{i=0}^p(-1)^i\Delta_p\circ F_{i,p}}\sigma^*\omega$$ where $F_{i,p}\colon\Delta_{p-1}\to\Delta_p$ is just $[0,1,\ldots,\hat{i},\ldots,p]$, i.e. the $i$-th face map. Then $$\int_{\sum_{i=0}^p(-1)^i\Delta_p\circ F_{i,p}}\sigma^*\omega = \sum_{i=0}^p(-1)^i\int_{\Delta_p\circ F_{i,p}}\sigma^*\omega = \sum_{i=0}^p(-1)^i\int_{\Delta_{p-1}}F_{i,p}^*\sigma^*\omega.$$ Finally, $$\sum_{i=0}^p(-1)^i\int_{\Delta_{p-1}}F_{i,p}^*\sigma^*\omega = \sum_{i=0}^p(-1)^i\int_{\Delta_{p-1}}(\sigma\circ F_{i,p})^*\omega = \sum_{i=0}^p(-1)^i\int_{\sigma\circ F_{i,p}}\omega = \int_{\partial\sigma}\omega.$$






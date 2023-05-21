### Lecture material

##### Part 1. Vector spaces

[Lecture 1](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/)

**Definition**. A *field* $F$ is a set with addition and multiplication, both of which are associate, commutative, have identities and inverses, and are distributive. 

**Definition**. A *vector space* $V$ over a field $F$ is a set with the two operations: addition ($+$) and multiplication ($\cdot$) by elements in $F$ (scalar) that satisfies the following axioms: 
* Associativity ($+$); 
* Existence of 0;
* Existence of inverse; 
* Commutativity;
(this is an Abelian group properties)
* Associativity ($\cdot$); 
* Distributivity for scalars; 
* Distributivity for vectors; 
* Existence of 1. 

**Definition**. A subset $W \in V$ is called a *subspace* if $W$ is a vector space with respect to the induced operations (i.e. the same addition and scalar multiplication as in $V$). 

[Lecture 2](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session02_2018_09_10.pdf)

***Statement***. Non-empty subset $W \subset V$ is a subspace $\Leftrightarrow$ $W$ is closed w.r.t the induced operations. 

***Statement***. Neutral element $0_V$ of $V$ equals neutral element $0_W$ of $W$. 

**Definition**. Let $V$ be a vector space over some field $F$. Then 
$$c_1 v_1 + \ldots + c_k v_k = \sum_{i = 1}^k c_i v_i$$
for $c_i \in F$, $v_i \in V$, $i \in \{1, \ldots k\}$ is called *linear combination*. 

**Definition**. For any subset $S \subset V$ we define 
$$\text{span} (S) = \{\text{all linear combinations } \sum_{i = 1}^k c_i s_i \text{ with }c_i \in F, s_i \in S, i \in \{1, \ldots, k\}, k \in \mathbb{N}\}$$
*Remark*. 
* For any subset $S \subset V$, $\text{span}(S)$ is a subspace;
* *$\text{span}(S)$ is the smallest subspace that includes $S$;
* if $W \subset V$ is a subspace, then $\text{span}(W) = W$. 

**Definition**. A subset $S \subset V$, s.t. $\text{span}(S) = V$ is called *generating set* (or *spanning set*). 

**Definition**. A minimal generating set is called a *basis* of $V$ (minimal means no element can be removed). 

**Definition**. A subset $S \subset V$ is called *linearly independent* if $\sum_{i = 1}^k c_i s_i = 0$ for $c_i \in F$, $s_i \in S$ always implies $c_i = 0$ $\forall i \in \{1, \ldots, k\}$. Otherwise, it's called *linearly dependent*. 

***Theorem***. Let $V$ be a vector space over a field $F$, and $E \subset V$ a subset. Then the following are equivalent: 
* $E$ is a basis of $V$; 
* $E$ is a maximal linearly independent set; 
* every $v \in V$ can uniquely be written as a linear combination of $e_i \in E$. 

[Lecture 3](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session03_2018_09_12.pdf)

**Definition**. $V$ is called a *finite dimensional* if it has finite basis. If not, it is called *infinite dimensional*. 

***Theorem***. If $V$ is finite dimensional, then the number of elements in a basis, does not depend on the basis. 

**Definition**. If $V$ has a basis with $n$ elements, then $n$ is called the dimension of $V$, i.e. $\text{dim} V = n$. 

[Lecture 4](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session04_2018_09_17.pdf)

***Theorem (Zorn's lemma)***. Let $S$ be a partially ordered set, s.t. every linearly ordered subset has an upper bound. Then $S$ has a maximal element. 

***Theorem***. Every vector space has a basis. 

##### Part 2. Maps

**Definition**. $m: S_1 \to S_2$ is called a *map* or *function*, if $V$, $W$ are vector spaces over a field $F$, $f: V \to W$ is called *linear* if $f(c_1 v_1 + c_2 v_2) = c_1 f(v_1) + c_2 f(v_2)$ $\forall c_1, c_2 \in F$, $v_1, v_2 \in V$. We define $\mathfrak{L}(V, W) = \{\text{all linear maps from } V \text{ to } W\}$ and $\mathfrak{L}(V) = \{\text{all linear maps from }V \text{ to } V\}$. 

***Lemma***. $\mathfrak{L}(V, W)$ is a vector space. 

***Lemma***. Let $\{v_1, \ldots, v_n\}$ be a basis in $V$ (in particular, $\text{dim} V = n < \infty$) and $\{w_1, \ldots, w_n\} \subset W$. Then there exists a unique linear map $f: V \to W$ with $f(v_i) = w_i$ $\forall i \in \{1, \ldots, n\}$. 

**Definition**. If $V$ is a vector space over $F$, then elements of $\mathfrak{L}(V, F)$ are called *functionals* of $V$. And $\mathfrak{L}(V, F) =: V^*$ is called a *dual space* if $V$. 

**Definition**. Let $\{v_1, \ldots, v_n\}$ be a basis of $V$ (finite dimension). Then $\{v_1^*, \ldots, v_n^*\} \subset V^*$, with $v_i^*(\sum_{j = 1}^n c_j v_j) = c_i$ ($v_i^*(v_j) = \delta_{ij}$) is called a *dual basis*. 

***Lemma***. The dual basis is indeed a basis. 

*Remark*. Wrong for infinite dimensions (not generating). 

[Lecture 5](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session05_2018_09_19.pdf) 

**Definition**. Bijective $f \in \mathfrak{L}(V, W)$ are called *isomorphisms*. If there exists an isomorphism between $V$ and $W$, then $V$ and $W$ are called *isomorphic*, and we write $V \cong W$. 

***Theorem***. Let $V$ and $W$ be finite dimensional vector spaces. Then they are isomorphic if and only if $\text{dim} V = \text{dim} W$. 

**Definition**. Isomorphisms that do not depend on "arbitrary choices" (e.g., basis) are called *canonical* or *natural isomorphisms*. Otherwise, they are called *non-canonical* or *accidental*. 

*Example (canonical isomorphism)*. Consider $\text{dim} V = n$ and isomorphism $V \to (V^*)^* = V^{**}$ (*double dual*). Let's define isomorphism $\varepsilon: V \to V^{**}$, $v \mapsto v^{**} = [f \mapsto f(v)]$ or $\varepsilon(v) = v^{**}$ with $v^{**}(f):= f(v)$ ($f \in V^*$). 

**Definition**. Let $f: V \to W$ be linear. Then *dual map* $f^*: W^* \to V^*$ is defined by 
$$f^*(w^*)(v) = w^*(f(v)) \quad \forall v \in V$$
[Lecture 6](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session06_2018_09_24.pdf)

***Theorem***. Dual map linear and unique. 

**Definition**. Let $f: V \to W$ be linear. Then 
* *kernel* or *null space* is $\text{ker} f = \{v \in V: f(v) = 0\} \subset V$; 
* *image* or *range* is $\text{im} f = \{w \in W: \exists v \in V \text{ with } f(v) = w\} \subset W$. 

*Remark*. Kernel and image are actually subspaces.  

***Lemma***. Let $f \in \mathfrak{L}(V, W)$. Then $f$ injective $\Leftrightarrow$ $\text{ker} f = \{0\}$. 

***Theorem (Fundamental theorem of linear maps)***. Let $f \in \mathfrak{L}(V, W)$ with $V$ fin-dim. Then 
$$\text{dim} V = \text{dim}(\text{im} f) + \text{dim}(\text{ker} f)$$
*Corollary*. Let $f \in \mathfrak{L}(V, W)$, $\text{dim} V < \infty$. Then 
$$f \text{ injective} \Leftrightarrow \text{dim} V = \text{dim} (\text{im} f)$$
Corollary. Let $f \in \mathfrak{L}(V, W)$, $\text{dim} V = \text{dim} W < \infty$. Then 
$$f \text{ isomorphism} \Leftrightarrow \text{ker} f = \{0\} \Leftrightarrow \text{im} f = W$$

##### Part 3. Matrices

[Lecture 7](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session07_2018_09_26.pdf)

**Definition**. Let $f \in \mathfrak{L}(V, W)$, where $V$ and $W$ are finite dimensional. We choose basis $B_V = \{v_1, \ldots, v_n\}$ of $V$ and $B_W = \{w_1, \ldots, w_m\}$ of $W$. $f$ defined by action on $v_k$, can be written as linear combination with $B_W$:
$$f(v_k) = \sum_{i = 1}^m a_{ik} w_i$$
which can be associated to matrix $A_{B_V, B_W} = (a_{ik})_{i \in \{1, \ldots, m\}, k \in \{1, \ldots, n\}}$. 

*Remark*. Composition of linear maps corresponds to matrix multiplication. 

**Definition**. *Basis change matrix* from $B_V$ to $B_V'$ is $T_{B_V B_V'}$. 

***Statement***. Let $f \in \mathfrak{L}(V, W)$, choose bases $B_V$ and $B_V'$ of $V$ and bases $B_W$ and $B_W'$ of $W$. Let $T_{B_V B_V'}$ be matrix of basis change $B_V$ to $B_V'$, $T_{B_W B_W'}$ of $B_W$ to $B_W'$. Let $A_{B_V B_W}$ be a matrix of $f$ in bases $B_V$, $B_W$, and $A_{B_V' B_W'}$ in bases $B_V'$, $B_W'$. Then 
$$A_{B_V' B_W'} = T_{B_W B_W'}^{-1} A_{B_V B_W} T_{B_V B_V'}$$
If $V = W$, i.e. $B_V = B_W$, $B_V' = B_W'$, we have $T_{B_V B_V'} = T_{B_W B_W'} = T$, hence 
$$A_{B_V' B_V'} = T^{-1} A_{B_V B_V} T,$$
this is called *conjugation* of by $T$. 

**Definition**. We can now define functionals $\varphi$, which are defined via $A_{B_V}$, but are actually independent of basis choice, i.e. $\varphi(f) = \varphi(A_{B_V}^f) = \varphi(A_{B_V'}^f)$. Such $\varphi$ are called *invariants*. 

*Examples*. Two important examples for $f \in \mathfrak{L}(V, V)$ are: 
* *Trace*. We define $\text{tr} f := \text{tr} A_{B_V}^f := \sum_i (A_{B_V}^f)_{ii}$ (sum of diagonal entries for some basis $B_V$); 
* *Determinant*. We define $\text{det} f := \text{det} A_{B_V}^f$. 

##### Part 4. Sums

**Definition**. Let $V_1, \ldots, V_1$ be subsets of vector space $V$. Then their *sum* is 
$$\sum_{i = 1}^n V_i = \left\{\sum_{i = 1}^n v_i \in V, \text{ s.t.  } v_i \in V_i, i \in \{1, \ldots, n\}\right\}$$
*Remark*. If $V_1, \ldots, V_n$ are subspaces of $V$, then their sum is their $\text{span}$. 

**Definition**. Let $V_1, \ldots, V_n$ be vector spaces. Then *external direct sum*
$$V = \bigoplus_{i = 1}^n V_i$$ is defined by
* $(v_1, \ldots, v_n) \in V$, $v_i \in V_i$; 
* $c(v_1, \ldots, v_n) + c'(v_1', \ldots, v_n') = (cv_1 + c'v_1', \ldots, cv_n + c'v_n')$.

***Theorem***. Let $V_1$, $V_2$ be subspaces of $V$, $\text{dim} V < \infty$. Then 
$$\text{dim}(V_1 \cap V_2) + \text{dim}(V_1 + V_2) = \text{dim} V_1 + \text{dim} V_2$$
[Lecture 8](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session08_2018_10_01.pdf)

**Definition**. Let $V_1, \ldots, V_n \subset V$ and $V_1, \ldots, V_n' \subset V$ be subspaces. We can say that $\{V_i\}$ and $\{V_i'\}$ are *identically arranged*, if there is a linear isomorphism $f: V \to V$, s.t. $f(V_i) = V_i'$. 

**Definition**. We can say that $V_1$ and $V_2$ are *in general position* if $\text{dim} V_1 \cap V_2$ is minimal. 

***Theorem***. Let $V_1, \ldots, V_n \subset V$ be subspaces with $\sum_{i = 1}^n V_i = V$. Then 
$$V = \bigoplus_{i = 1}^n V_i \Leftrightarrow V_{i_0} \cap \left( \sum_{i = 1, i \neq i_0}^n V_i\right) = \{0\} \quad 1 \leq i_0 \leq n \Leftrightarrow \sum_{i = 1}^n \text{dim} V_i = \text{dim} V$$
**Definition**. $p \in \mathfrak{L}(V)$ is a *projector* if $p^2 = p$ ($p^2 = p \circ p$). 

*Remark*. Let $V = \bigoplus_{i = 1}^n V_i$ be given, i.e. any $v$ can be uniquely written as $v = \sum_{i = 1}^n$ with $v_i \in V_i$. We can define $p_j(\sum_{i = 1}^n v_i) = v_j$, then $p_j$ clearly is a projector, $p_i p_j = 0$ for $i \neq j$, $\sum_{i = 1}^n p_i = \text{id}$, and $V_i = \text{im} p_i$. 

***Theorem***. Let $p_1, \ldots, p_n \in \mathfrak{L}(V)$ be projectors with $\sum_{i = 1}^n p_i = \text{id}$ and $p_i p_j = 0$ for all $i \neq j$, then
$$V = \bigoplus_{i = 1}^n \text{im} p_i$$
*Remark*. Mapping between direct sums is a direct sum of mappings. 

##### Part 5. Quotient spaces

**Definition**. Let $M \subset L$ be a subspace, $e \in L$, translation of $M$ by $e$ is $e + M = \{e + m: m \in M\}$ is an "affine subset". 

***Lemma***. Let $M_1, M_2 \subset L$ be subspaces, $e_1, e_1 \in L$. Then 
$$e_1 + M_1 = e_2 + M_2 \Leftrightarrow M_1 = M_2 = M \text{ and } e_1 - e_2 \in M$$
[Lecture 9](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session09_2018_10_08.pdf)

**Definition**. The *quotient space* (*factor space*) $L/M$ is defined as 
$$L/M = \{l + M : l \in L\}$$
with 
* addition $(l_1 + M) + (l_2 + M) = (l_1 + l_2) + M$; 
* scalar multiplication $c(l + M) = cl + M$.

**Lemma**. $L/M$ is a vector space. 

*Remark*. Equivalence relation. 

*Remark*. There is a canonical map $q: L \to L/M$, $l \mapsto q(l) = l + M$, called the *quotient map*. It is surjective, linear, linear image (fiber) of $\widetilde{l} + M$ is $\widetilde{l} + M$ (subset of $L$) and its kernel is $M$. 

***Theorem***. For $\text{dim} L < \infty$, we have $\text{dim}L/M = \text{dim}L - \text{dim}M$ (called *codimension* of $M$ in L).

**Definition**. Given $f: L \to M$ (linear), we can define $\text{coim} f := L/\text{ker} f$ (coimage of $f$), $\text{coker} f := M / \text{im} f$ (cokernel of $f$). 

*Remark*. Some important diagrams are in lecture notes. 

***Lemma (Universal property)***. Let $f: L \to M$, $g: L \to N$, then $h$ so that $hf = g$ exists iff $\text{ker} f \subset \text{ker} g$. If additionally $\text{im} f = M$, then $h$ is unique. 

[Lecture 10](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session10_2018_10_10.pdf)

**Definition**. The four fundamental spaces of a linear map $f$ are: $\text{ker} f$, $\text{coker} f$, $\text{ker} f^*$, $\text{coker} f^*$. 
$$\text{ker} f \subset L \xrightarrow{f} M \supset \text{im} f \quad \quad \text{im} f^* \subset L^* \xleftarrow{f^*} M^* \supset \text{ker} f^*$$
**Definition**. Let $M \subset L$ be a subspace. Then $M^{\perp} \subset L^*$, the *orthogonal complement* of $M$, is defined as $\{m^* \in L^* : m^*(m) = 0 \forall m \in M\}$. 

*Remark*. $M^{\perp}$ is a subspace. 

*Remark*. Important diagram is in lecture notes. 

***Lemma***. 
* For $M$ a subspace of $L$, $L^*/ M^{\perp} \cong M^*$ (canonical isomorphism); 
* For $M$ a subspace of $L$, $(L/M)^* \cong M^{\perp}$ (canonical isomorphism).

##### Part 6. Linear operators

[Lecture 11](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session11_2018_10_15.pdf)

*Remark*: In this chapter: $L$, $M$ are finite dimension vector spaces. 

***Theorem***. Let $f \in \mathfrak{L}(L, M)$. Then there are $\widetilde{L} \subset L$ and $M \subset M'$ such that $L = \text{ker} f \oplus \widetilde{L}$, $M = \text{im} f \oplus M'$ and $\widetilde{f}: \widetilde{L} \to \text{im} f$, $\widetilde{f} = f|_{\widetilde{L}}$ is an isomorphism. Also, there are bases of $L$ and $M$ such that the matrix $A_f$ of $f$ is a matrix with $A_{ii} = 1$ for $i \in \{1, \ldots, r\}$ with $r =: \text{rank} f$ and zeros everywhere else. 

*Remark*. This means that any $m \times n$ matrix can be brought into that form by basis change.

**Definition**. Let $\widetilde{L} \subset L$, $f \in \mathfrak{L}(L)$
* $\widetilde{L}$ is called *invariant* if $f(\widetilde{L}) \subset \widetilde{L}$;
* If $\widetilde{L}$ is invariant and $\text{dim} \widetilde{L} = 1$, then $\widetilde{L}$ is called a *proper subspace* (for $f$). Then $f|_{\widetilde{L}}(l) = \lambda l$ for some $\lambda \in F$, or $f|_{\widetilde{L}} = \lambda \text{id}_{\widetilde{L}}$, i.e. $f|_{\widetilde{L}}$ is multiplication by a constant. $\lambda$ is called *eigenvalue* of $f$ and any $\widetilde{L} \ni \widetilde{l} \neq 0$ is called *eigenvector*;
* If $\widetilde{L}$ is invariant and $f|_{\widetilde{L}}$ is multiplication by a constant, then $\widetilde{L}$ is *eigenspace*.

**Definition**. $f \in \mathfrak{L}(L)$ is called *diagonalizable*, if $L = \bigoplus_{i = 1}^n L_i$ with proper subspaces $L_i$ of $f$ (i.e. $\text{dim} L_i = 1$ for all $i$). 

*Remark*. This is equivalent to existence of a basis such that the matrix of $f$ is diagonalizable. 

**Definition**. For $f \in \mathfrak{L}$, we call $P_f(t) = \text{det}(t \cdot \text{id} - f)$ the *characteristic polynomial* of $f$.

*Remark*. The characteristic polynomial can be computed with matrix of $f$, and it is independent of basis choice. 

***Theorem***. $\lambda$ is an eigenvalue of $f$ iff $\lambda$ is a root of $P_f(t)$ in $F$.  

[Lecture 12](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session12_2018_10_17.pdf)

*Remark*. In the lecture notes, there are some examples. 

**Definition**. A polynomial $Q$ *annihilates* $f$ if $Q(f) = 0$. $Q(t) = \sum_{i = 0}^n c_i t^i$ with $c_n = 1$ and minimal $n$ such that still $Q(t) = 0$ is called *minimal polynomial*.

*Remark*. There is a polynomial with degree $\leq n^2$ which annihilates $f$. Minimal polynomial is unique. 

***Theorem (Cayley-Hamilton)***. $P_f(f) = 0$.

**Definition**. 
* $l \in L$ is called a *root vector* of $f$ if $(f - \lambda)^r(l) = 0$ for some $r > 0$;
* If $\lambda$ is additionally an eigenvalue, then such $l$ which are non-zero are called *generalized eigenvector*;
* *Generalized eigenspace* $G(\lambda) = \{\text{generalized eigenvectors to } \lambda\} \cup \{0\}$.

##### Part 7. Jordan form

[Lecture 13](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session13_2018_10_29.pdf)

**Definition**. $f$ is called *nilpotent* if $f^j = 0$ for some $j$.  

***Theorem (abstract Jordan decomposition)***. Let $f \in \mathfrak{L}(L)$ with $\text{dim} L = n < \infty$, and $L$ a vector space over the algebraically closed field $F$. Then $L = \bigoplus_i G(\lambda_i)$ and $f = \bigoplus_i f_i$ with $f_i: G(\lambda_i) \to G(\lambda_i)$, where the $\lambda_i$ are the distinct eigenvalues. 

***Lemma***. Let $f \in \mathfrak{L}(L)$ and $\text{dim} L = n$. Then $L = \text{ker} f^n \oplus \text{im} f^n$. 

***Lemma***. $G(\lambda) = \text{ker}(f - \lambda)^n$. 

***Lemma***. Let $\lambda_1, \ldots, \lambda_n$ be the distinct eigenvalues with corresponding generalized eigenvectors $l_1, \ldots, l_m$. Then $l_1, \ldots, l_m$ are linearly independent. 

***Lemma***. $\text{ker} p(f)$ and $\text{im} p(f)$ are invariant for any polynomial $p$. 

*Corollary*. $L$ has a basis of generalized eigenvectors. 

*Corollary*. $f$ has simple spectrum $\Rightarrow$ $f$ is diagonalizable. 

*Remark*. 
* Multiplicity of eigenvalue $\lambda = \text{dim} G(\lambda)$, so $\text{dim} L$ is a sum of multiplicities of all eigenvalues. 
* An $r \times r$ matrix of the form 
$$J_r(\lambda) = 
	\begin{pmatrix}
		\lambda & 1 & 0 & \cdots & 0 \\ 
		0 & \lambda & 1 & \cdots & 0 \\ 
		0 & 0 & \lambda & \cdots & 0 \\ 
		\vdots & \vdots & \vdots & \ddots & \vdots \\ 
		0 & 0 & 0 & \cdots & \lambda
	\end{pmatrix}
$$
is called a *Jordan block*. 
* $J$ with Jordan blocks on a diagonal is called a *Jordan matrix*. 
* A Jordan basis of $f$ is a basis such that $f$ is represented by Jordan matrix, i.e. has *Jordan normal form*: there is non-singular $X$ s.t. $X^{-1} A_f X = J$. 

[Lecture 14](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session14_2018_11_05.pdf)

***Theorem (Jordan normal form)***. Every $f \in \mathfrak{L}(L)$ has a Jordan basis. 

***Lemma***. Let $g \in \mathfrak{L}(L)$ be nilpotent. Then there are $l_1, \ldots, l_n \in L$ and integers $m_1, \ldots, m_n > 0$ such that $g^{m_n}(l_1), g^{m_1 - 1}(l_1), \ldots, g(l_1), l_1, \ldots, g^{m_n}(l_n), \ldots, g(l_n), l_n$ is a basis of $L$ and $g^{m_i + 1}(l_i) = 0$ for all $i \in \{1, \ldots, n\}$. 

*Remark*. 
* Nonzero vectors $l, g(l), \ldots, g^k(l)$ such that $g^{k + 1}(l) = 0$ are called a *sting* of $g$; 
* Every nilpotent $g$ has a *Jordan matrix*. 

[Lecture 15](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session15_2018_11_07.pdf)

***Remark***. Some useless shit about decomplexification is in lecture notes. 

##### Part 8. Bilinear forms

[Lecture 16](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session16_2018_11_12.pdf)

**Definition**. Let $L_1$, $L_2$, $M$ be vector spaced over the field $F$. Then $f: L_1 \times L_2 \to M$, $(l_1, l_2) \mapsto f(l_1, l_2)$ is called *bilinear map* if it is linear with respect to both variables. 

**Definition**. If $M = F$, then such $f$ are called *bilinear forms*. 

*Remark*. We study bilinear forms $L \times \overline{L} \to F$ or $L \times \overline{L} \to \mathbb{C}$; these are called *inner products*. We write $L \times \overline{L} \to \mathbb{C}$ as a *sesquilinear form* $g: L \times L \to \mathbb{C}$, i.e, $g(al_1, bl_2) = a\overline{b} g(l_1, l_2)$ (linear in first, autilinear in second argument). 

**Definition**. *Gram matrix* is $G = (g(e_i, e_j))_{i, j = 1, \ldots, n}$.

*Remark*. 
* Bilinear: $g^T(l, m) := g(m, l)$; $G$ changes to $G^T$; 
* Sesquilinear: $\overline{g}^T(l, m) := \overline{g(m, l)}$ (still linear in first argument); $G$ changes to $\overline{G}^T$. 

**Definition**. 
* *Symmetric*: $g^T = g$ ($G$ symmetric), orthogonal geometry; 
* *Antisymmetric* or *symplectic*: $g^T = -g$ ($G$ antisymmetric); 
* *Hermitian*: $\overline{g}^T = g$ ($G$ Hermitian) (note: $\overline{g}^T(l, l) = \overline{g}(l, l) = \overline{g(l, l)} = g(l, l)$ is real).

**Definition**. Let $(L, g)$ be an inner product space. Then $l_1$, $l_2$ are called *orthogonal* if $g(l_1, l_2) = 0$. $L_1, L_2 \subset L$ are orthogonal if $g(l_1, l_2) = 0$ for all $l_1 \in L_1$, $l_2 \in L_2$. 

*Remark*. If $g = \pm g^T$, then $g(l_1, l_2) = 0$ iff $\pm g^T(l_1, l_2) = 0$ iff $g(l_2, l_2) = 0$. 

**Definition**. 
* $\text{ker} g = \{m \in L: g(m, l) = 0 \forall l \in L\}$; 
* If $\text{ker} g = \{0\}$, then $g$ is called *non-degenerate*; 

*Remark*. 
* $\text{ker} g = \text{ker} \widetilde{g}$, where $\widetilde{g}: L \to \overline{L^*}$ by rule $\widetilde{g}(l)(m) := g(l, m)$; 
* $g$ is non-degenerate iff $G$ is non-singular;
* $\text{rank} g := \text{dim }\text{im} \widetilde{g} = \text{rank} G$. 

[Lecture 17](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session17_2018_11_14.pdf)

**Definition**. Let $(L_1, g_1)$ and $(L_2, g_2)$ be inner product spaces. A linear isomorphism $f: L_1 \to L_2$ is called *isometry* if $g_1(l, l') = g_2(f(l), f(l'))$ $\forall l, l' \in L_1$. $(L_1, g_1)$ and $(L_2, g_2)$ are called isometric if there is an isometry for them. 

Remark. Some classifications are in lecture notes. 

**Definition**. A subspace $L_0 \subset L$ is called 
* *non-degenerate* if $g|_{L_0}$ is non-degenerate; 
* *isotropic* if $g|_{L_0} = 0$. 

**Definition**. The *orthogonal complement* $L_0^{\perp}$ of $L_0 \subset L$ is
$$L_0^{\perp} := \{l \in L : g(l_0, l) = 0 \text{ for all } l_0 \in L_0\} \subset L$$

[Lecture 18](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session18_2018_11_19.pdf)

***Lemma***. Let $(L, g)$ be an inner product with space with $\text{dim} L < \infty$. Then 
* $L_0 \subset L$ non-degenerate $\Rightarrow$ $L = L_0 \oplus L_0^{\perp}$; 
* $L_0 \subset L$ and $L_0^{\perp}$ non degenerate $\Rightarrow$ $(L_0^{\perp})^{\perp} = L_0$. 

***Theorem***. Let $(L, g)$ be an inner product space with $\text{dim} L < \infty$. Then $L = \bigoplus_{i = 1}^m L_i$, where $L_i$'s'are pairwise orthogonal and
* 1-dimensional for symmetric and Hermitian forms; 
* 1-dimensional degenerate or 2-dimensional non-degenerate for symplectic forms.

**Definition**. $(r_0, r_+, r_-)$ is called *signature* of $(L, g)$, where
* $r_0 = \text{dim} \text{ ker} g$; 
* $r_+$ is a number of positive $L_i$'s;
* $r_-$ is a number of negative $L_i$'s.

[Lecture 19](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session19_2018_11_21.pdf)

**Theorem**. 
* Symplectic over $\forall$ field $F$, symmetric over $\mathbb{C}$ up to isometry determined by $n$, $r_0$; 
* (Inertia theorem or Sylvester's law of inertia) Symmetric over $\mathbb{R}$, Hermitian over $\mathbb{C}$: up to isometry determined by signature, independent of choice of orthogonal decomposition. 

*Corollary*. 
* Orthogonal and Hermitian spaces have an *orthogonal basis* $g(e_i, e_j) = 0$ for $i \neq j$, Gram matrix looks like 
$$
\begin{pmatrix}
	E_{r_+} & 0 & 0 \\ 
	0 & -E_{r_-} & 0 \\ 
	0 & 0 & 0_{r_0}
\end{pmatrix}
$$
* Symplectic spaces hace a symplectic basis $\{e_1, \ldots, e_r, \widetilde{e_1}, \ldots, \widetilde{e_r}, e_1', \ldots, e_{n - 2r}'\}$ with $g(e_1, \widetilde{e_i}) = -g(\widetilde{e_i}, e_i) = 1$ and all other combinations equal to 0.  Gram matrix looks like 
$$
\begin{pmatrix}
	0 & E_{r} & 0 \\ 
	-E_{r} & 0 & 0 \\ 
	0 & 0 & 0
\end{pmatrix}
$$
##### Part 9. Orthogonalization

[Lecture 20](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session20_2018_11_26.pdf)

**Definition**. Let $h: L \times L \to F$ be a bilinear form, then $q: L \to F$, $q(l) = h(l, l)$ is called a *quadratic form*. A symmetric bilinear form $g$ such that $q(l) = g(l, l)$ is called *polarization* of $q$. 

***Algorithm (Gram-Schmidt orthogonalization)***. 
- Start with  $e_1 = e_1'$;
- Say $e_{1}, \ldots, e_{i-1}$ already given. Then look for $e_i=e_i' - \sum_{j=1}^{i-1} Y_j e_j \quad\left(Y_j \in F\right)$
- Need $g\left(e_{i}, e_j\right)=0$ $\forall j=l_1, \ldots,-1 \Rightarrow 0=g\left(e_i^{\prime}, e_j\right)-Y_j g\left(e_{j, e_j}\right)$
$$
\begin{aligned}
	& \Rightarrow Y_j=\frac{g\left(e_i^{\prime}, e_j\right)}{g\left(e_{j, e_j}\right)} \\
	& \Rightarrow e_i=e_i^{\prime}-\sum_{j=1}^{i-1} \frac{g\left(e_{i}, e_j'\right)}{g\left(e_j, e_j\right)} e_j
\end{aligned}
$$
*Remark*. Some examples of polynomials and orthogonalizations are in lecture notes. 

[Lecture 21](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session21_2018_11_28.pdf)

**Definition**. A *Euclidean space* $(L, g)$ is a real vector finite dimension space $L$, with symmetric and positive defined inner product $g$ ($g(l, l) > 0$ for $l \neq 0$, or $r_0 = r_- = 0$). A *unitary space* $(L, g)$ is a complex vector space $L$ with Hermitian and positive defined inner product $g$. 

*Remark*. Write as follows: $g(l, m) =: \langle l, m \rangle$, $\sqrt{\langle l, l \rangle} =: ||l||$ (lenght), and such $g$ is called *scalar product. 

***Statement (Cauchy-Schwarts-Bunyakovskii)***. $|\langle l_1, l_2\rangle| \leq ||l_1|| \cdot ||l_2||$ with equality iff $l_1$ and $l_2$ linearly independent. 

*Remark*. *Triangle inequality* for lenght holds, hence $||\cdot||$ is a norm and $d(l_1, l_2) = ||l_1 - l_2||$ is a *metric*. *Angles* in Euclideans space are defined as follows: 
$$\cos \varphi = \frac{\langle l_1, l_2\rangle}{||l_1||\cdot ||l_2||}$$
Distance between objects is defined as a minimum between their points. 

[Lecture 22](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session22_2018_12_03.pdf)

**Definition**. Isometries on Euclidean (unitary) spaces are called *orthogonal (unitary) operators*. 

**Lemma**. $f$ is isometry iff 
* $||f(l)|| = ||l|| \quad \forall l \in L$; 
* $\{e_j\}_{j = 1, \ldots, n}$ basis of $l$, $G$ Gram matrix of scalar product, $U$ matrix of $f$, then $U^TG U = G$; 
* $f$ maps any ONB into another ONB; 
* matrix $U$ of $f$ in any ONB satisfies $U^T U = E_n$.

***Theorem***. 
* $f$ unitary iff $f$ diagonizable in some ONB with $|\lambda_j = 1|$ ($\lambda_j$ eigenvalue, $j \in \{1, \ldots, n\}$); 
* $f$ orthogonal iff in some ONB the matrix of $f$ is 
$$
\begin{pmatrix}
	U(\varphi_1) & \cdots & 0 & 0 & \cdots & 0 & 0 & \cdots & 0 \\ 
	\vdots & \ddots & \vdots & \vdots & \ddots & \vdots & \vdots & \ddots & \vdots \\ 
	0 & \cdots & U(\varphi_n) & 0 & \cdots & 0 & 0 & \cdots & 0 \\ 
	0 & \cdots & 0 & 1 & \cdots & 0 & 0 & \cdots & 0 \\ 
	\vdots & \ddots & \vdots & \vdots & \ddots & \vdots & \vdots & \ddots & \vdots \\ 
	0 & \cdots & 0 & 0 & \cdots  & 1 & 0 & \cdots & 0 \\ 
	0 & \cdots & 0 & 0 & \cdots & 0 & -1 & \cdots & 0 \\ 
	\vdots  & \ddots & \vdots & \vdots & \ddots & \vdots & \vdots & \ddots & \vdots \\ 
	0 & \cdots & 0 & 0 & \cdots & 0 & 0 & \cdots & -1 
\end{pmatrix}
$$
with 
$$
U(\varphi) = 
\begin{pmatrix}
	\cos \varphi & -\sin \varphi \\ 
	\sin \varphi & \cos \varphi
\end{pmatrix}
$$
[Lecture 23](http://math.jacobs-university.de/petrat/teaching/2018_fall_linear_algebra/Session23_2018_12_05.pdf)

**Definition**. $f: L \to L$ with $\langle f(l_1), l_2 \rangle = \langle l_1, f(l_2) \rangle$ $\forall l_1, l_2 \in L$ is called *self-adjoint*. 

***Lemma***. Let $f: L \to L$ be diagonizable in some basis with real eigenvectors. Then $f$ is self-adjoint. 

***Theorem***. 
* (Spectral theorem) $f: L \to L$ is self-adjoint iff $f$ diagonizeable in some ONB with real eigenvectors; 
* If $f: L \to L$ is self-adjoint, then eigenvectors for different eigenvalues are orthogonal. 

**Definition**. *Normal operators* are $\{f : ff^* = f^*f\}$. 
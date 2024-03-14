# Linear Algebra Done Right Notes

[TOC]



## Chapter 1 Vector Spaces

**Properties of complex arithmetic.** commutativity, associativity, identities, inverse, distributivity.

**Definition (Tuple).** A list if length $n$ : $(x_1,\ldots,x_n)$ is an $n$​​​-tuple.

------

**Definition 1.19 (Vector Space).** A vector space $(V,+,\cdot)$ is a set $V$ along with an addition on $V$ and a scalar multiplication on $V$​ such that the following properties hold: commutativity, associativity, additive identity, additive inverse, multiplicative identity, distributive properties.

**Note.** The set $V$ can be a set of functions, for the rest of the notes, $V$ denotes a vector space.

**Notation.** Given a set $S$, $\mathbf{F}^S$ denotes the set of functions from $S$ to $\mathbf{F}$.

**Example.** $\mathbf{R}^{[0,1]}$ is the set of real-valued functions on the interval $[0,1]$.

**Example.** $\mathbf{F}^S$​ is a vector space.

------

**Definition (Subspace).** A subset $U$ of $V$ is called a subspace of $V$ if $U$ is also a vector space (using the same addition and scalar multiplication as on $V$​ ).

**Note.** We do not use notation $U \subseteq V$ because both of them are vector spaces instead of sets. In general in algebra there is no special notation for substructures.

**Definition (Sum of Subsets).** $U_1+\cdots+U_m=\{u_1+\cdots+u_m:u_1\in U_1,\ldots,u_m \in U_m\}.$​

**Intuition.** The set (space) of all possible sums of elements of given sets $U_1,\cdots,U_m$​.

------

**Definition (Direct Sum).** If $\forall u \in U_1+\cdots+U_m, \exists! u_j \in U_j: u = \sum_j u_j$, then denote the sum by $U_1 \oplus \cdots \oplus U_m$​​ and call it a **direct sum**.

**Intuition.** The definition of direct sum requires that every vector in the sum have a unique representation as an appropriate sum.

**Lemma.** $U_1+\cdots+U_m$ is a direct sum if and only if $u_1+\cdots+u_m=0 \Rightarrow \forall j :u_j = 0$.

**Lemma.** Suppose $U$ and $W$ are subspaces of $V$. Then $U+W$ is a direct sum if and only if  $U\cap W = \{0\}$​​.

**Note.** In the above lemma, though $U$ and $W$ are subspaces instead of subsets. We can denote $U \cap W$ the intersection of two subspaces, which is also a vector space.

**Intuition.** Sums of subspaces are analogous to unions of subsets. Similarly, direct sums of subspaces are analogous
to disjoint unions of subsets. No two subspaces of a vector space can be disjoint, because both contain $0$. So disjointness is replaced,at least in the case of two subspaces, with the requirement that the intersection equals $\{0\}$.

## Chapter 2 Finite-Dimensional Vector Space

**Definition (Linear Combination).** A linear combination  of a list $v_1, \ldots, v_m$ of vectors in $V$: $a_1v_1+\cdots+a_mv_m$ where $a_1,\ldots,a_m \in \mathbf{F}$.

**Definition 2.5 (Span).** $\text{span}(v_1,\ldots,v_m)=\{a_1v_1+\cdots+a_mv_m:a_1,\ldots,a_m\in \mathbf{F}\}$.

**Note.** $\text{span}():=\{0\}$.

**Definition (Polynomial).** A function $p:\mathbf{F} \to \mathbf{F}$ is called a polynomial with coefficients in $\mathbf{F}$ if：
$$
\exist a_0,\ldots,a_m \in \mathbf{F}, \forall z \in \mathbf{F}: p(z)=  a_0+a_1z+a_2z^2+\cdots+a_mz^m
$$
**Definition ($\mathcal{P}(\mathbf{F})$).** The set of all polynomials with coefficients in $\mathbf{F}$.

**Note.** $p(\cdot)$ is a function and $\mathcal{P}(\mathbf{F})$ is a vector space over $\mathbf{F}$, a subspace of $\mathbf{F}^\mathbf{F}$.

**Definition (Degree of Polynomial).** $p \in \mathcal{P}(\mathbf{F})$ is said to have degree $m$ if $a_m \neq 0$, denoted by $\text{deg } p=m$.

**Note.** The polynomial that is identically $0$ is said to have degree $-\infty$. $\text{deg } 0 = -\infty$.

**Definition ($\mathcal{P}_m(\mathbf{F})$).** For $m$ a nonnegative integer, $\mathcal{P}_m(\mathbf{F})$ denotes the set of all polynomials with coefficients in $\mathbf{F}$ and degree at most $m$​​.

------

**Definition 2.17 (Linearly Dependent).** $v_1,\ldots,v_m$​ is linearly dependent if
$$
\exist a_1,\ldots,a_m \in \mathbf{F}, \text{ not all }0:a_1v_1+\cdots+a_mv_m=0.
$$
**Lemma 2.21 (Linear Dependence Lemma).** Suppose $v_1,\ldots,v_m$ is a linearly dependent list in $V$. Then there exists $j \in \{1,2,\ldots,m\}$ such that:

(a) $v_j \in \text{span}(v_1,\ldots,v_{j-1})$;

(b) if the $j^{\text{th}}$ term is removed from $v_1,\ldots,v_m$, the span of the remaining list equals $\text{span}(v_1,\ldots,v_{m})$​​.

**Note.** Spanning list $v_1, \ldots, v_m$ can be linearly dependent.

**Lemma 2.23.** Length of linearly independent list $\leq$​​ length of spanning list. (Proof by Lemma 2.21)

------

**Definition 2.27 (Basis).** $v_1,\ldots,v_n$​ is a basis of $V$ if it is linearly independent and spans $V$​.

**Intuitive.** Basis is a spanning list that is also linearly independent.

**Theorem.** $v_1,\ldots,v_n$ is a basis of $V$ if and only if
$$
\forall v \in V, \exist! a_1,\ldots,a_n \in \mathbf{F}:v=a_1v_1+\cdots+a_nv_n.
$$
**Lemma.** Spanning list contains a basis.

**Lemma.** Linearly independent list extends to a basis.

**Theorem.** Suppose $V$ is finite-dimensional and $U$ is a subspace of $V$, then there exists subspace $W$ of $V$, s.t. $V=U\oplus V$.

**Intuitive.** This is analogous to the complement of a set. Every subspace of a finite-dimensional vector space can be
paired with another subspace to form a direct sum of the whole space.

------

**Definition 2.36 (Dimension).** The dimension of a finite-dimensional vector space $V$ is the length of any basis of $V$, denoted by $\text{dim }V$​.

**Lemma.** Spanning list of the right length is a basis.

**Lemma.** Linearly independent list of the right length is a basis.

**Theorem (Dimension of a sum).** $\text{dim}(U_1+U_2)=\text{dim }U_1+\text{dim }U_2-\text{dim}(U_1 \cap U_2)$​.

## Chapter 3 Linear Maps

**Definition 3.2 (Linear Map).** A function $T:V \to W$ with:

​	additivity: 	$\forall u,v \in V: T(u+v) = Tu+Tv$;

​	homogeneity:   $\forall \lambda \in \mathbf{F}, v \in V: T(\lambda v)=\lambda(Tv)$​.  (齐次)

**Notation.** The set of all linear maps from $V$ to $W$ is denoted $\mathcal{L}(V,W)$.

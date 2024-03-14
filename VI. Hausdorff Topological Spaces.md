# VI. Hausdorff Topological Spaces

## A. Open Sets – Three Steps

### Step One: Euclidean space

**Definition (Euclidean $k$-space).** $\mathbf{R}^k = \{x=(x_1,x_2,\ldots,x_k): x_n \in \mathbf{R}\}$ is the set of k-element tuples of real numbers.

**Definition (Open Ball).** Given $x \in \mathbf{R}^k$ and $r>0$, the **open ball of center $x$ and radius $r$** is 
$$
\mathbb{B}[x;r)=\{y \in \mathbf{R}^k:|y-x|<r\}.
$$
**Definition (Open set in $\mathbf{R}^k$).** A subset $U$ of $\mathbf{R}^k$ is **open** if and only if
$$
\forall x \in U, \exists r>0: \mathbb{B}[x;r) \subseteq U.
$$
**Intuition.** From every point $x$ in $U$, moving in any direction is allowed in $U$, at least for distances below $r$​.

**Definition (Topology).** $\mathcal{T}=\{U \subseteq \mathbf{R}^k: U \text{~~is an open set}\}$, the usual "topology" on $\mathbf{R}^k$.

**Definition (Neighborhoods).** $\mathcal{N}(x) =\{S \in \mathcal{P}(X): \exists U \in \mathcal{T} \text{~~and~~} x \in U \subseteq S\}$, the set of neighborhoods of $x$.


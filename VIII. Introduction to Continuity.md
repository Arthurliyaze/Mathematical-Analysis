# VIII. Introduction to Continuity

## A. The Big Picture—Continuity on a HTS

**Definition (Topological Characterization of Continuity).** Let $f:X \to Y$ be a [single-valued] mapping. To say, $f$ **is continuous** [**on **$(X,\mathcal{T}_X)$] means
$$
\forall G \in \mathcal{T}_Y, ~~~~f^{-1}(G)\in \mathcal{T}_X.
$$
**Intuition.** Every open subset $G$ of $Y$, the preimage $f^{-1}(G)$ is an open subset of $X$.

**Lemma.** $f:X \to Y$ *is continuous if and only if* $f^{-1}(C)$ *is closed for every closed set* $C$ *in* $Y$​.

*Proof.* First we prove that $\forall W \subseteq Y$, $f^{-1}(W^c)=f^{-1}(W)^c$.

$(\Rightarrow)$ If $x \in f^{-1}(W^c)$, then $f(x) \in W^c$, i.e. $f(x) \notin W$. Thus $x \in f^{-1}(W)^c$.

$(\Leftarrow)$ If $x \in f^{-1}(W)^c$, then $f(x) \notin W$, i.e. $f(x) \in W^c$. Thus $x \in f^{-1}(W^c)$.

Since a set $C \subseteq Y$ is closed if and only if $C^c$ is open,

$(\Rightarrow)$ Let $C$ be any closed subset of $Y$. Then $C^c$ is open, so the continuity implies that $f^{-1}(C^c)= f^{-1}(C)^c$ is open, i.e. $f^{-1}(C)$ is closed.

$(\Leftarrow)$ Similar. 															$\square$

## UA 4.4 Continuous Functions on Compact Sets

**Theorem 4.4.1 (Preservation of Compact Sets).**  *Let $f:A \to \mathbf{R}$ be continuous on $A$. If $K \subseteq A$ is compact, then $f(K)$​ is compact as well.*   

**Definition 4.4.4 (Uniform Continuity).** A function $f:A \to \mathbf{R}$ is *uniformly continuous on* $A$ if for every $\epsilon >0$ there exists a $\delta >0$ such that for all $x,y \in A$, $|x-y|<\delta$ implies $|f(x)-f(y)| < \epsilon$​.

**Intuition.** The key distinction between asserting that $f$ is “uniformly continuous on $A$” versus simply “continuous on $A$” is that, given an $\epsilon > 0$, a single $\delta > 0$ can be chosen that works simultaneously for all points $c$ in $A$.

**Example.** The function $h(x) = \sin (1/x)$ is continuous on $(0,1)$​ but not uniformly continuous (near zero). 

**Theorem 4.4.7 (Uniform Continuity on Compact Sets).** *A function that is continuous on a compact set$K$ is uniformly continuous on $K$.*


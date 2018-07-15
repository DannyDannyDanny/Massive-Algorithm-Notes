
### Question 1
### Question 2 The Highest α-Free Ancestor Problem

Let $T$ be a rooted tree with $n$ nodes. Each leaf in $T$ is assigned a label from a set of colors $C$. Given a node $v ∈ T$, the subtree rooted at $v$, denoted $T(v)$, is the tree consisting of $v$ and all descendants of $v$. A subtree $T(v)$ is $α$-free if it does not contain a leaf with label $α$. We are interested in efficient data structures for $T$ that support the following query. Let $l$ be a leaf in $T$ and $α$ a color in $C$.

$HFA(l, α)$: return the highest ancestor $a$ of $l$ such that $T(a)$ is $α$-free.

Give a linear-space data structure for $T$ that supports fast $HFA$ queries. Ignore the preprocessing time.

#### Solution in $O(\log(n))$ time
No additional changes are made to the original tree. To perform $HFA(\alpha,l)$


Starting at leaf $$l$$, traverse the parents and if all children are \alpha-free continue to the grandparents, otherwise return the leaf. Continue recursively checking greater-grandparents and all greater-grandchildren until the the subtree at some grandparent is no longer \alpha-free.

Ideas for alternative solution: Find most closely related alpha node and do LCA. Return LCA nodes child on $l$'s side.


### Question 3
### Question 4
### Question 5
### Question 6

### Question 7 - String Reversal

Let S be a string of length $N$ stored in $O(N/B)$ blocks.

We want to compute the reverse string $S^R$ of $S$.


#### Algorithm to reverse S in the I/O model.

$B$ is I/O block size and $n$ is Length of string $S$

* Divide $S$ into substrings - such that any two substrings can be loaded in one I/O.
* Read the first and last substrings into memory and reverse each substring.
* Write the reversed substrings each to the others original position.
* Working inwards, repeat the process for each pair of substrings until S has been reversed.

The whole process takes $O(n/B)$ I/Os.



#### Algorithm to reverse S in the cache oblivious model.

* Half the string into substrings recursively until any two substrings fit into **memory**.
* Read the first and last substrings into memory and reverse each substring.
* Write the reversed substrings each to the others original position.
* Working inwards, repeat the process for each pair of substrings until S has been reversed.

The algorithms runs in $O(n/M)$ I/Os

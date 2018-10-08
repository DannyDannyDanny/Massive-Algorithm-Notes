# Hashing
The idea:
* Mapping data of an arbitrary size, **U**, to a fixed size, **S**.
* Used for the dictionary problem (*lookup, insert, delete*).
* Given a **key**, a **hash function** returns a **hash value**.
* Three types of hashing: *Chained, Universal, Perfect*
* Space complexity: `O(n)`.
* Time complexity: `O(1)`.

## Chained Hashing
* An array, `A` of linked-lists.
* `A[i]` is the linked-list containing keys in `S` that hash to `i`.

![as](/figs/chained_hashing.png)
* Time complexity is `O(1)` assuming:
  * `h` is chosen uniformly at random among all functions from `U` to {0,..., m-1}
  * We can store `h` in `O(n)` space.
  * We can evaluate `h` in `O(1)` time
* Expected time `O(1)`
* Space complexity: `O(n)`

## Universal Hashing
* implies probability for collisions is uniform for any two keys.
* uses a family of functions mapping U to {0, ..., m-1}.
* uses prime number `p` and random number `a`.
* the hashing function makes a linear combination from `x` by multiplying digitis of `a` in base `p` and taking the it's modul `p` value.
* For any `x≠y` in `U` and `h` chosen uniformly at random in `H`, implies  `Pr(h(x) = h(y)) ≤ 1/m`
* Expected time `O(1)`

## Perfect (FKS) Hashing
* Combines:
  * `O(n^2)` collision-free `(1/2)` hash-functions
  * `O(n)` collision-prone `(1/2n)` hash-functions
  * ... in a multi-level data-structure
  * Compact dictionary of loose dictionaries
* Static dictionary - for preprocessed data-structures.

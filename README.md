
### Question 1
### Question 2
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
* Read the first and last substrings into memory and reverse.
* Write the reversed substrings each to the others original position.
* Working inwards, repeat the process with the next two $B/2$ long substrings from either end.

The whole process takes $O(n/B)$ I/Os.



#### Algorithm to reverse S in the cache oblivious model.

* Half the string into substrings recursively until any two substrings fit into memory.
* Load first and last substrings into memory and reverse each.
* Write each reversed substring in place of the others original position.


> wait this is exactly the same....

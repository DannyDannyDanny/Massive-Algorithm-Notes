## Questions for assignments:

## Questions for slides:

#### Week 11 - External Memory

##### Slide 18 (Solution 2. Table Partitioning)
The theorem says we can solve the SPIIG in the I/O model in $O(n^2/MB + n/B)$ I/Os. Where does added $n/B$ come from? Is it for reading the strings S,T from disk?

##### Slide 22
The algorithm fills in the quadrant recursively, does that mean the algorithm recursively subdivides the quadrants into smaller sub-quadrants until each sub-quadrant fits into memory?

...And if so how does it know the division fits into memory without knowing the memory and block size?

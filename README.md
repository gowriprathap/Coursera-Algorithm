# Coursera Algorithm Week 4

### 1. How many different minimum cuts are there in a tree with n nodes (ie. n−1 edges)?

The number of minimum cuts is the number of edges, so the number of minimum cuts is n-1.

### 2. Let "output" denote the cut output by Karger's min cut algorithm on a given connected graph with n vertices, and let p = 1/(nC2). Which of the following statements are true?

The probability of finding a fixed minimum cut is lower bounded p.
So, for every graph G with n nodes there is a minimum cut (A,B) so that Pr[out=(A,B)] ≥ p.
Similarly, for every graph G with n nodes and every min cut (A,B) of G, Pr[out=(A,B)] ≥ p.
It is possible for a graph to exist and a in-cut such that the probability of finding it is atmost p, when the graph has only two nodes and one edge. In this case, the probability of finding the min cut is 1 (and hence p = 1). Hence there exists a graph G with n nodes and a min cut (A,B) of G, such that Pr[out=(A,B)] ≤ p

### 3. Let .5 < α < 1 be some constant. Suppose you are looking for the median element in an array using RANDOMIZED SELECT (as explained in lectures). What is the probability that after the first iteration the size of the subarray in which the element you are looking for lies is ≤ α times the size of the original array?

Let the size of the array be N and the pivot be the xth number in the sorted array.
When (1−α)N < x < αN, the median will be in the array smaller than of equals to αN.
The probability of the pivot lying in that range is p = 1 − (1 − α) − (1 − α), which is the whole range minus the forbidden ones. That is, p = 2α − 1.

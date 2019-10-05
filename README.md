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

### 4. Let 0 < α < 1 be a constant, independent of n. Consider an execution of RSelect in which you always manage to throw out at least a 1 − α fraction of the remaining elements before you recurse. What is the maximum number of recursive calls you'll make before terminating?

In the initial call we have n elements. We throw out 1 − α fraction of elements, so in the first recursive call we have n - n(1 − α), which is nα. So, in the first recursive call, there are at most αn elements. This goes on till the dth recursive call, where we have at most (α^d)* n elements. Let the recursion stop at the dth recursive call, then (α^d)* n ≤ 1. If we log on both sides, we get d = −log(n) log(α).

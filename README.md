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

### 5. The minimum s-t cut problem is the following. The input is an undirected graph, and two distinct vertices of the graph are labelled "s" and "t". The goal is to compute the minimum cut (i.e., fewest number of crossing edges) that satisfies the property that s and t are on different sides of the cut. Suppose someone gives you a subroutine for this s-t minimum cut problem via an API. Your job is to solve the original minimum cut problem (the one discussed in the lectures), when all you can do is invoke the given min s-t cut subroutine. (That is, the goal is to reduce the min cut problem to the min s-t cut problem.) Now suppose you are given an instance of the minimum cut problem -- that is, you are given an undirected graph (with no specially labelled vertices) and need to compute the minimum cut. What is the minimum number of times that you need to call the given min s-t cut subroutine to guarantee that you'll find a min cut of the given graph?

Let s be one of the vertex and t varies across. The process is done by picking the smallest one, hence we need at most n − 1 calls.

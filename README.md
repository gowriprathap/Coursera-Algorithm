# Coursera Algorithm Week 4

1. How many different minimum cuts are there in a tree with n nodes (ie. n−1 edges)?

The number of minimum cuts is the number of edges, so the number of minimum cuts is n-1.

2. Let "output" denote the cut output by Karger's min cut algorithm on a given connected graph with n vertices, and let p = 1/(nC2). Which of the following statements are true?

The probability of finding a fixed minimum cut is lower bounded p.
So, for every graph G with n nodes there is a minimum cut (A,B) so that Pr[out=(A,B)] ≥ p.
Similarly, for every graph G with n nodes and every min cut (A,B) of G, Pr[out=(A,B)] ≥ p.
It is possible for a graph to exist and a in-cut such that the probability of finding it is atmost p, when the graph has only two nodes and one edge. In this case, the probability of finding the min cut is 1 (and hence p = 1). Hence there exists a graph G with n nodes and a min cut (A,B) of G, such that Pr[out=(A,B)] ≤ p

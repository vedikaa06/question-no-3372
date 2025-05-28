# question-no-3372
Solution to the question no 3372 on leet code 

3372. Maximize the Number of Target Nodes After Connecting Trees I
There exist two undirected trees with n and m nodes, with distinct labels in ranges [0, n - 1] and [0, m - 1], respectively.

You are given two 2D integer arrays edges1 and edges2 of lengths n - 1 and m - 1, respectively, where edges1[i] = [ai, bi] indicates that there is an edge between nodes ai and bi in the first tree and edges2[i] = [ui, vi] indicates that there is an edge between nodes ui and vi in the second tree. You are also given an integer k.

Node u is target to node v if the number of edges on the path from u to v is less than or equal to k. Note that a node is always target to itself.

Return an array of n integers answer, where answer[i] is the maximum possible number of nodes target to node i of the first tree if you have to connect one node from the first tree to another node in the second tree.

Note that queries are independent from each other. That is, for every query you will remove the added edge before proceeding to the next query.

build() Function:

Builds an adjacency list from the edges.

For each node, performs DFS to count how many nodes can be reached within k steps (or k-1 for the second tree).

In maxTargetNodes():

count1[i]: Number of nodes reachable from node i in edges1 within k.

count2: Same as above but for edges2 and within k-1.

maxCount2: The maximum value in count2.

res[i]: count1[i] + maxCount2 — this is the final result for each node in the first tree.

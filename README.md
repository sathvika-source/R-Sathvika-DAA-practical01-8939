# R-Sathvika-DAA-practical01-8939

This repository contains implementations of classic sorting, greedy, dynamic programming, and graph algorithms for the DAA (Design and Analysis of Algorithms) practical assignment.

## Implemented algorithms

- **Bubble Sort** — Repeatedly compares adjacent elements and swaps out-of-order pairs. Complexity: best O(n), average/worst O(n²). Stable and in-place.
- **Merge Sort** — Recursively divides and merges sorted halves. Complexity: O(n log n) in all cases. Stable, but requires extra space.
- **Insertion Sort** — Builds a sorted sequence by inserting each element into its correct position. Complexity: best O(n), average/worst O(n²). Stable and in-place.
- **Quick Sort** — Uses a pivot and partitions the elements recursively. Average complexity: O(n log n); worst case O(n²). Usually in-place and not stable.
- **Selection Sort** — Repeatedly selects the minimum element from the unsorted portion. Complexity: O(n²) in all cases. In-place and not stable by default.

## Practical 2 — Greedy Algorithms

- **Activity Selection** — Selects activities by earliest finish time to maximize the number of non-overlapping activities. Complexity is O(n log n) with sorting, or O(n) after sorting.
- **Fractional Knapsack** — Takes items in decreasing value-to-weight ratio order. Complexity is O(n log n) due to sorting, and the greedy solution is optimal for this fractional variant.
- **Huffman Coding** — Combines the two least-frequent nodes using a priority queue. Complexity is O(n log n), and it produces an optimal prefix-free code.

## Practical 3 — Dynamic Programming

- **Longest Common Subsequence (LCS)** — Finds the longest subsequence shared by two sequences. Complexity is O(mn) time and space.
- **0/1 Knapsack** — Determines the maximum value within a weight capacity while allowing each item to be used once. Complexity is O(nW), with O(W) space possible.
- **Matrix Chain Multiplication** — Finds the minimum-cost parenthesization of a matrix chain. Complexity is O(n³) time and O(n²) space.

## Practical 4 — Graph Algorithms

- **DFS** — Explores graph branches deeply using recursion or a stack. Complexity is O(V + E).
- **BFS** — Explores a graph level by level using a queue. Complexity is O(V + E).
- **Dijkstra's Algorithm** — Computes shortest paths from a source in a graph with non-negative edge weights. Complexity is O((V + E) log V).
- **Bellman-Ford** — Computes shortest paths in graphs that may contain negative edges and detects negative cycles. Complexity is O(VE).
- **Kruskal's Algorithm** — Builds an MST by selecting edges in ascending weight using disjoint sets. Complexity is O(E log E).
- **Prim's Algorithm** — Grows an MST from a starting vertex using a priority queue. Complexity is O((V + E) log V).

## Practical 5 — 0/1 Knapsack

The `DAA Practical-05.ipynb` notebook uses dynamic programming to find the maximum value that fits within a given capacity. It uses a DP table in which each state considers whether to include or exclude an item. Complexity is O(nW) time and O(nW) space; the space can be optimized to O(W).

## Practical 6 — Matrix Chain Multiplication

The `DAA Practical-06.ipynb` notebook uses interval dynamic programming to find the least-cost multiplication order for a sequence of matrices. For every interval, it tests possible split points and stores the minimum cost. Complexity is O(n³) time and O(n²) space.

## Practical 7 — Coin Change

The `DAA Practical_07.ipynb` notebook uses a 1D DP array to find the minimum number of coins needed to form a target amount, allowing unlimited copies of each denomination. Complexity is O(amount × k) time and O(amount) space. It returns -1 when the amount cannot be formed.

## Practical 8 — Graph Traversal

- **BFS** — Traverses nodes level by level using a queue and is useful for shortest paths in unweighted graphs.
- **DFS** — Traverses deeply along each branch using recursion or a stack and is useful for cycle detection and connected components.
- Both traversals have O(V + E) time complexity.

## Practical 9 — Prim's Algorithm

The `DAA_Practical_09.ipynb` notebook implements Prim's algorithm to construct a Minimum Spanning Tree (MST). Starting from vertex A, it uses a min-heap to repeatedly select the minimum-weight edge connecting the visited set to an unvisited vertex. The example graph produces an MST with total weight 6.

- Complexity: O((V + E) log V) with a priority queue.
- Properties: Produces a minimum-cost spanning tree for a connected, weighted graph.

## Practical 10 — Kruskal's Algorithm

The `DAA_Practical_10.ipynb` notebook implements Kruskal's algorithm for finding an MST. It sorts all edges by weight and adds each edge to the tree only if it does not create a cycle, using a disjoint-set/union-find data structure with path compression and union by rank. The example graph produces a total MST weight of 6.

- Complexity: O(E log E) because of edge sorting; DSU operations are nearly constant amortized time.
- Properties: Greedy, works on weighted undirected graphs, and produces a minimum-cost spanning tree.

## Practical 11 — Floyd-Warshall Algorithm

The `DAA_Practical_11.ipynb` notebook implements the Floyd-Warshall algorithm to find shortest paths between every pair of vertices. It initializes a distance matrix and repeatedly considers each vertex as an intermediate node to improve existing paths.

- Complexity: O(V³) time and O(V²) space.
- Properties: All-pairs shortest paths; supports graphs with negative edge weights but not negative cycles; the example returns a complete shortest-distance matrix.

## Practical 12 — Travelling Salesman Problem

The `DAA_Practical_12.ipynb` notebook solves the Travelling Salesman Problem (TSP) using dynamic programming and bitmask state representation. For each subset of cities and final city, it stores the minimum route cost and reconstructs the optimal tour. The example with four cities returns the tour `[0, 2, 3, 1, 0]` with minimum distance 80.

- Complexity: O(n² · 2ⁿ) time and O(n · 2ⁿ) space.
- Properties: Exact solution for the symmetric TSP implementation, requiring a distance matrix and a tour that returns to the starting city.

## How to run

Open `DAA_practial01.ipynb` in Jupyter or Google Colab and execute the notebook cells. The other practical notebooks can be opened and run in the same way.

## Notes

- Timing results are illustrative for small example inputs; use larger randomized inputs for meaningful performance comparisons.
- The notebooks include simple examples and comments to explain each implementation.

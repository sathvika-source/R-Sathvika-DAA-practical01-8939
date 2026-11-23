# R-Sathvika-DAA-practical01-8939

This repository contains practical implementations of fundamental Design and Analysis of Algorithms (DAA) concepts. The notebooks demonstrate sorting, greedy strategies, dynamic programming, graph traversal, shortest paths, minimum spanning trees, and exact optimization problems using Python.

## Practical 1 — Sorting Algorithms

The `DAA_practial01.ipynb` notebook compares five fundamental sorting techniques and demonstrates how their selection of elements, swapping strategy, stability, and space requirements differ.

- **Bubble Sort**
  - Repeatedly compares adjacent elements and swaps them when they appear in the wrong order.
  - Performs one less comparison in each pass after the largest remaining element reaches its correct position.
  - Complexity: best O(n) with an early-termination check, average O(n²), worst O(n²).
  - Properties: stable and in-place.

- **Merge Sort**
  - Uses divide-and-conquer to divide the input into two halves, sort them recursively, and merge the sorted halves.
  - The merging step is the main operation and preserves the relative order of equal elements.
  - Complexity: O(n log n) in the best, average, and worst cases.
  - Properties: stable, but it requires additional array space and is less space-efficient for direct in-place use.

- **Insertion Sort**
  - Builds a sorted subarray one element at a time by shifting larger elements right and inserting the current element at the correct position.
  - Adapts well to small arrays and data that is already nearly sorted.
  - Complexity: best O(n), average O(n²), worst O(n²).
  - Properties: stable and in-place.

- **Quick Sort**
  - Chooses a pivot, partitions the array around it, and recursively sorts the smaller and larger partitions.
  - Typical performance depends on pivot selection; balanced partitions give the fastest execution.
  - Complexity: average O(n log n), worst O(n²), and best O(n log n).
  - Properties: usually in-place and generally faster in practice, although it is not stable by default.

- **Selection Sort**
  - Finds the minimum element from the unsorted portion and places it at the next sorted position.
  - It completes a maximum of n − 1 swaps even if the input is in reverse order.
  - Complexity: O(n²) in the best, average, and worst cases.
  - Properties: in-place and not stable by default.

**Practical goal:** Understand the working principles, time-space trade-offs, stability, and practical suitability of basic sorting algorithms.

## Practical 2 — Greedy Algorithms

This practical demonstrates greedy design, where a locally optimal choice is made at each step with the expectation of producing a globally optimal result for suitable problem structures.

- **Activity Selection**
  - Sorts activities by finishing time or processes them in that order.
  - Always chooses the next compatible activity that finishes earliest.
  - Complexity: O(n log n) with sorting, O(n) after sorting.
  - Property: greedy choice is optimal because choosing the earliest finishing activity leaves the maximum remaining time.

- **Fractional Knapsack**
  - Calculates the value-to-weight ratio of every item and takes the highest-ratio items first.
  - Items may be included completely or as a fraction if the knapsack is not large enough for all of them.
  - Complexity: O(n log n) due to sorting.
  - Property: optimal for the fractional knapsack; it does not provide a general solution for the 0/1 variant.

- **Huffman Coding**
  - Creates a binary prefix code by repeatedly combining the two least-frequent symbols.
  - A priority queue or min-heap maintains the nodes in frequency order.
  - Complexity: O(n log n) for n symbols.
  - Property: produces an optimal variable-length code for the given symbol frequencies without prefix ambiguity.

**Practical goal:** Learn to identify greedy-choice and optimal-substructure conditions and compare greedy solutions with problems that require dynamic programming.

## Practical 3 — Dynamic Programming

This practical introduces optimal substructure and overlapping subproblems. Instead of repeatedly solving the same subproblems, the notebook builds and reuses memoized or tabulated states.

- **Longest Common Subsequence (LCS)**
  - Compares two sequences and finds the longest subsequence appearing in the same relative order in both.
  - Each DP state considers matching or skipping characters and reconstructs the final sequence from the table.
  - Complexity: O(mn) time and O(mn) space.
  - Property: useful for sequence similarity, edit comparison, and pattern analysis.

- **0/1 Knapsack**
  - Considers every item once and decides whether inclusion improves the value within the remaining capacity.
  - `dp[i][w]` represents the best value from the first i items at capacity w.
  - Complexity: O(nW) time and O(nW) space, or O(W) with a 1D table.
  - Property: exact solution for indivisible items; unlike fractional knapsack, arbitrary fractions are not allowed.

- **Matrix Chain Multiplication**
  - Evaluates every possible parenthesization of a matrix chain and stores the minimum cost for each interval.
  - Uses a DP table indexed by the starting and ending matrix positions.
  - Complexity: O(n³) time and O(n²) space.
  - Property: demonstrates interval DP and optimal split-point reconstruction.

**Practical goal:** Understand how recurrence relations, base cases, state tables, and reconstruction are used to solve optimization problems exactly.

## Practical 4 — Graph Algorithms

This practical covers graph representation, traversal, shortest paths, and minimum spanning trees. The algorithms differ according to graph type, edge weights, and required output.

- **Depth-First Search (DFS)**
  - Explores the deepest available branch before backtracking.
  - Uses recursion or an explicit stack.
  - Complexity: O(V + E).
  - Applications: cycle detection, connected components, path search, and topological sorting of DAGs.

- **Breadth-First Search (BFS)**
  - Explores all neighbors at the current level before moving to the next level.
  - Uses a queue and can track levels or parent nodes.
  - Complexity: O(V + E).
  - Applications: shortest paths in unweighted graphs and level-order traversal.

- **Dijkstra's Algorithm**
  - Starts from a source and repeatedly selects the unvisited vertex with the smallest known distance.
  - Uses a min-heap for efficient priority selection and updates tentative distances.
  - Complexity: O((V + E) log V) with a priority queue.
  - Limitation: valid for graphs with non-negative edge weights.

- **Bellman-Ford Algorithm**
  - Repeatedly relaxes every edge to improve known shortest paths.
  - Allows an extra pass to detect negative-weight cycles.
  - Complexity: O(VE).
  - Advantage: handles negative edge weights and reports negative cycles that make shortest paths undefined.

- **Kruskal's Algorithm**
  - Sorts edges by increasing weight and greedily selects edges that do not form cycles.
  - Uses union-find operations to determine whether two vertices are already connected.
  - Complexity: O(E log E).

- **Prim's Algorithm**
  - Grows a tree from one starting vertex.
  - Adds the minimum-weight edge crossing from the visited part to the unvisited part.
  - Complexity: O((V + E) log V) with a heap.

**Practical goal:** Choose graph algorithms based on graph size, edge weights, connectivity, and the required result.

## Practical 5 — 0/1 Knapsack

The `DAA Practical-05.ipynb` notebook implements the 0/1 Knapsack problem using dynamic programming. Given item weights, values, and a maximum capacity, it determines the maximum value that can be carried without exceeding the capacity. Each item is considered only once and may either be excluded or included.

- DP relation: decide between skipping the current item and including it if it fits.
- Time complexity: O(nW), where n is the number of items and W is capacity.
- Space complexity: O(nW), or O(W) with a one-row optimization.
- Property: produces the exact maximum, unlike a greedy fractional knapsack.
- Notebook behavior: reads item weights, values, and capacity, then prints the maximum achievable value.

**Practical goal:** Apply tabulation to an indivisible-item resource-allocation problem and understand the trade-off between time and memory.

## Practical 6 — Matrix Chain Multiplication

The `DAA Practical-06.ipynb` notebook finds the optimal way to parenthesize a chain of matrices so that the number of scalar multiplications is minimized. It uses an interval DP table where `dp[i][j]` stores the minimum cost for matrices i through j.

- For every possible split k, it combines the left and right subchain costs with the cost of multiplying the resulting matrices.
- Time complexity: O(n³).
- Space complexity: O(n²).
- Property: records the optimum cost and demonstrates how interval subproblems combine to produce a global optimum.
- Notebook behavior: reads matrix dimensions and prints the minimum multiplication cost.

**Practical goal:** Learn an interval-based DP pattern and distinguish optimal substructure from merely repeated multiplication.

## Practical 7 — Coin Change

The `DAA Practical_07.ipynb` notebook solves the minimum-coins coin-change problem. Unlimited copies of each coin denomination may be used, and the objective is to form a target amount with the fewest coins.

- A 1D DP array stores the minimum number of coins needed for every amount from 0 to the target.
- For each amount, the implementation evaluates every denomination that fits.
- Time complexity: O(amount × k), where k is the number of denominations.
- Space complexity: O(amount).
- Property: returns -1 when no combination can form the target amount.
- Reconstruction can be added if the selected coin sequence, rather than only the count, is required.

**Practical goal:** Use one-dimensional DP to solve an unbounded-choice optimization problem and handle infeasible targets.

## Practical 8 — Graph Traversal

The `DAA Practical-08.ipynb` practical demonstrates two standard methods for systematically visiting graph vertices. Both traverse every reachable vertex and edge once under normal implementation assumptions.

- **Breadth-First Search (BFS)**
  - Starts at a source and visits vertices in increasing distance from the source.
  - Uses a queue and marks vertices as discovered to prevent repeated processing.
  - Useful for shortest paths in unweighted graphs and level-based exploration.

- **Depth-First Search (DFS)**
  - Explores each branch as deeply as possible before moving to a sibling.
  - Uses recursion or an explicit stack and tracks visited vertices.
  - Useful for cycle detection, path existence, connected components, and topological sorting.

- Time and space: O(V + E) for traversal, with space depending on queue, stack, and visited-storage requirements.

**Practical goal:** Compare level-wise and depth-wise exploration and understand when each ordering is useful.

## Practical 9 — Prim's Algorithm

The `DAA_Practical_09.ipynb` notebook implements Prim's algorithm for constructing a Minimum Spanning Tree (MST) from a connected weighted graph.

- It begins with a chosen starting vertex and marks it as visited.
- All edges from the visited set are placed in a min-heap.
- The minimum-weight edge to an unvisited vertex is added along with that vertex.
- Each newly visited vertex contributes its crossing edges to the heap.
- The example graph begins at A and produces an MST of total weight 6.

- Time complexity: O((V + E) log V) with a binary heap.
- Space complexity: O(V + E).
- Property: greedy and exact for finding a minimum spanning tree on connected, undirected graphs with non-negative weights.

**Practical goal:** Understand how a growing connected tree and priority queue find a minimum-cost spanning structure.

## Practical 10 — Kruskal's Algorithm

The `DAA_Practical_10.ipynb` notebook implements Kruskal's algorithm using a disjoint-set/union-find data structure.

- It collects the graph's unique undirected edges and sorts them by ascending weight.
- Union-find tracks whether vertices belong to the same connected component.
- Each edge is added only if it joins two different components, preventing cycles.
- The process stops after V − 1 edges have been selected.
- The example graph produces an MST containing five edges with total weight 6.

- Time complexity: O(E log E), dominated by sorting.
- DSU operations: nearly O(α(V)) amortized with path compression and union by rank.
- Property: greedy and exact for weighted undirected graphs; the result is an MST rather than necessarily a unique edge set.

**Practical goal:** Learn how cycle prevention using union-find combines with edge-sorting to build an MST.

## Practical 11 — Floyd-Warshall Algorithm

The `DAA_Practical_11.ipynb` notebook computes shortest paths between every pair of vertices using Floyd-Warshall dynamic programming.

- It initializes direct edge distances and uses infinity for unavailable pairs.
- Diagonal distances are set to zero.
- For each intermediate vertex k, it tests whether paths i → k → j are shorter than known paths i → j.
- The resulting matrix contains the shortest distance for every ordered pair.

- Time complexity: O(V³).
- Space complexity: O(V²).
- Property: supports negative edge weights and is particularly suitable for dense graphs or all-pairs queries.
- Limitation: negative cycles invalidate shortest-path distances, although cycle detection can be added.
- The example graph produces shortest distances for all six vertices.

**Practical goal:** Understand all-pairs shortest-path optimization through repeated intermediate-vertex relaxation.

## Practical 12 — Travelling Salesman Problem

The `DAA_Practical_12.ipynb` notebook solves the Travelling Salesman Problem using Held-Karp dynamic programming and bitmask subsets.

- A mask represents the set of cities already visited.
- The DP state stores the minimum cost of reaching a city after visiting a particular subset.
- Initial states represent paths beginning at city 0 and visiting one city i.
- Larger subsets are evaluated before the tour closes by returning to city 0.
- Parent information is retained to reconstruct the optimal path.
- The example 4-city matrix produces the tour `[0, 2, 3, 1, 0]` with minimum distance 80.

- Time complexity: O(n² · 2ⁿ).
- Space complexity: O(n · 2ⁿ) for a memoized implementation.
- Property: exact solution for small to medium instances, but exponential growth makes it unsuitable for very large n.

**Practical goal:** Apply subset dynamic programming to a classic NP-hard optimization problem and compare its exact state-based solution with brute-force permutation search.

## How to run

1. Open a notebook in Jupyter Notebook, JupyterLab, or Google Colab.
2. Upload or clone the repository and ensure the notebook working directory contains the repository files.
3. Run the cells sequentially from top to bottom.
4. Enter values when prompted for practicals that accept keyboard input.
5. Observe the output tables, traversal sequences, costs, or optimal paths printed by the notebook.

## Notes

- The implementations are intended for learning and demonstration rather than production-scale performance comparisons.
- Timings may vary by Python version, environment, and input size.
- Randomized or larger datasets provide more meaningful practical comparisons for sorting and graph algorithms.
- Comments and simple examples are included to clarify the purpose of each implementation step.

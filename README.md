# R-Sathvika-DAA-practical01-8939

This repository contains implementations of classic sorting algorithms for the DAA (Design and Analysis of Algorithms) practical assignment. The Jupyter notebook demonstrates each algorithm with ex[...]

## Implemented algorithms (concise descriptions)

- Bubble Sort
  - What it does: Repeatedly scans the list, comparing adjacent elements and swapping them when out of order until the list is sorted.
  - Complexity: Best O(n), Average/Worst O(n^2).
  - Properties: Stable, in-place.

- Merge Sort
  - What it does: Uses divide-and-conquer to split the list into halves, recursively sort them, then merge the sorted halves.
  - Complexity: Best/Average/Worst O(n log n).
  - Properties: Stable, not in-place (requires extra space for merging).

- Insertion Sort
  - What it does: Builds the sorted list one element at a time by inserting each element into its correct position among the already-sorted elements.
  - Complexity: Best O(n), Average/Worst O(n^2).
  - Properties: Stable, in-place. Efficient for small or nearly-sorted inputs.

- Quick Sort
  - What it does: Picks a pivot, partitions the list into elements less than, equal to, and greater than the pivot, and recursively sorts the partitions.
  - Complexity: Average O(n log n), Worst O(n^2) (rare with good pivot selection).
  - Properties: Typically not stable, can be implemented in-place; generally fast in practice.

- Selection Sort
  - What it does: Repeatedly selects the minimum element from the unsorted portion and swaps it into position.
  - Complexity: Best/Average/Worst O(n^2).
  - Properties: Not stable by default, in-place.

## Practical 2 — Greedy Algorithms (summary)

This practical explores greedy algorithm techniques and common greedy problems. The emphasis is on making locally optimal choices that lead to globally optimal solutions for specific problem classes.

- Activity Selection
  - What it does: Chooses the maximum number of non-overlapping activities by always selecting the next activity that finishes earliest.
  - Complexity: O(n log n) if sorting by finish times is required; O(n) after sorting.
  - Properties: Optimal for the activity-selection problem using the greedy strategy.

- Fractional Knapsack
  - What it does: Maximizes total value by taking fractions of items with the highest value-to-weight ratio first.
  - Complexity: O(n log n) due to sorting by ratio.
  - Properties: Greedy solution is optimal for the fractional variant (not for 0/1 knapsack).

- Huffman Coding (if included)
  - What it does: Builds an optimal prefix-free binary code for a set of symbols by repeatedly combining the two least-frequent nodes.
  - Complexity: O(n log n) using a priority queue.
  - Properties: Produces an optimal variable-length encoding for given symbol frequencies.

## Practical 3 — Dynamic Programming (summary)

This practical focuses on dynamic programming (DP): solving complex problems by combining solutions to overlapping subproblems with optimal substructure. Examples demonstrate tabulation and memoization approaches.

- Longest Common Subsequence (LCS)
  - What it does: Finds the longest sequence present in the same relative order in two sequences by building a DP table of subproblem solutions.
  - Complexity: O(m * n) time and O(m * n) space for sequences of lengths m and n.
  - Properties: Classic DP example illustrating reconstruction of the solution from the table.

- 0/1 Knapsack (DP)
  - What it does: Computes the maximum value achievable with a weight capacity by considering whether to include each item using a DP table.
  - Complexity: O(n * W) time and O(n * W) space (W = capacity); can be optimized to O(W) space.
  - Properties: Exact solution for the 0/1 knapsack using DP (greedy does not work in general).

- Matrix Chain Multiplication
  - What it does: Finds the optimal parenthesization to minimize scalar multiplications when multiplying a chain of matrices using DP.
  - Complexity: O(n^3) time and O(n^2) space for n matrices.
  - Properties: Demonstrates DP on intervals and how optimal split points are recorded and used.

## How to run
- Open DAA_practial01.ipynb in Jupyter or Google Colab and execute the cells to see each algorithm's implementation, example runs, and timing output.

## Notes
- The notebook's timing is illustrative for small examples; use larger randomized inputs to compare performance meaningfully.
- Comments and simple examples are included in the notebook to help understand each implementation.

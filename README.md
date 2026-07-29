# R-Sathvika-DAA-practical01-8939

This repository contains implementations of classic sorting algorithms for the DAA (Design and Analysis of Algorithms) practical assignment. The Jupyter notebook demonstrates each algorithm with example inputs and simple timing measurements.

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

## How to run
- Open DAA_practial01.ipynb in Jupyter or Google Colab and execute the cells to see each algorithm's implementation, example runs, and timing output.

## Notes
- The notebook's timing is illustrative for small examples; use larger randomized inputs to compare performance meaningfully.
- Comments and simple examples are included in the notebook to help understand each implementation.

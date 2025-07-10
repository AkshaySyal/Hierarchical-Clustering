# Hierarchical-Clustering
This project implements hierarchical clustering using a disjoint set data structure to iteratively merge the closest points (single linkage) on the moons dataset, then visualizes the resulting clusters when cut at K=2, K=5, and K=10

# Problem Statement
<img width="1898" height="136" alt="image" src="https://github.com/user-attachments/assets/06e97a8c-62bf-4a6d-9489-c984f0237ce9" />

# Solution Summary
- Implemented a **custom hierarchical clustering algorithm** (bottom-up) on the **moons dataset** (1,500 points).

- **Algorithm Details**:
  - Calculated all pairwise **Euclidean distances** and stored them in a sorted list (`heap`).
  - Used a **Disjoint Set Union (DSU)** data structure with:
    - Optimized `find` (with path compression).
    - `union` functions for efficient cluster merging.
  - Merged the two closest clusters iteratively (single linkage), consuming the smallest distance from the heap.
  - Continued merging until reaching a predefined number of clusters **K**.

- **Key Insights**:
  - Demonstrated hierarchical clustering **from first principles**.
  - Showcased the **efficiency of DSU** for managing dynamic clusters.
  - Highlighted hierarchical clustering’s **flexibility**:
    - Can “cut” the hierarchy at various levels (e.g., K = 2, 5, 10) to explore different granularities.

- **Visualization**:
  - Used `matplotlib.pyplot` to plot results.
  - Color-coded points by **cluster ID**.
  - Provided an intuitive visual understanding:
    - For K=2: identified two dominant clusters.
    - For higher K (5, 10): revealed finer groupings.

- **Conclusion**:
  - Successfully built and visualized a hierarchical clustering algorithm.
  - Combined algorithmic rigor (DSU) with clear visual insights on cluster formation.

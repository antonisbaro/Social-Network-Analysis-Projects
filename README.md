# Social Network Analysis & Graph Machine Learning Projects

This repository showcases a series of projects from the "Social Network Analysis" course, implemented in Python. The projects cover fundamental concepts in graph theory, network topology analysis, community detection, and machine learning, using both synthetic and real-world datasets.

---

## 📈 Project 1: Analysis & Comparison of Network Topologies

This project provides a comparative study of various fundamental graph models. The goal is to understand their structural properties by calculating and analyzing key network metrics, and then use these insights to characterize a real-world network.

### Methodology & Analysis
-   **Synthetic Graph Generation**: Generated a suite of synthetic graphs using `NetworkX`, representing distinct topologies (Regular, Erdos-Renyi, Barabasi-Albert, Watts-Strogatz, etc.).
-   **Structural Metrics Calculation**: For each graph, a comprehensive set of metrics was computed, including Clustering Coefficient, Path Length, and various Centrality Measures (Degree, Closeness, Betweenness, Katz, PageRank).
-   **Real-World Network Characterization**: Analyzed the "Game of Thrones" character interaction network, comparing its metrics to the synthetic models to identify its underlying topology.

---

## 👨‍👩‍👧‍👦 Project 2: Community Detection in Synthetic and Real-World Networks

This project explores and evaluates various algorithms for community detection, a core task in network analysis aimed at discovering densely connected subgroups within a graph.

### Methodology & Evaluation
-   **Algorithm Implementation**: Applied three classic community detection algorithms to both synthetic graphs and real-world networks (American College Football, Game of Thrones, email-Eu-core):
    1.  **Girvan-Newman**: A divisive algorithm based on iteratively removing edges with the highest edge betweenness.
    2.  **Greedy Modularity Maximization**: A fast, agglomerative algorithm that optimizes for the modularity score.
    3.  **Spectral Clustering**: A technique that uses the eigenvalues of the graph's Laplacian matrix to find communities.
-   **Partition Quality Assessment**: Evaluated the discovered communities using two key metrics:
    -   **Performance**: Measured how well the partitioning separates the graph into distinct, non-overlapping groups.
    -   **Modularity**: Quantified the strength of the division of a network into modules (or communities).
-   **Ground-Truth Comparison**: For the `email-Eu-core` dataset, the results were compared against the known ground-truth communities (university departments) to objectively assess the accuracy of each algorithm.
-   **Key Insight**: The analysis revealed a crucial trade-off: optimizing for **modularity** tends to find fewer, larger, and more isolated communities, while optimizing for **performance** often results in many smaller, internally dense clusters.

---

## 🔗 Project 3: Link Prediction in a Protein-Protein Interaction Network

This project focuses on the classic problem of link prediction in a biological network (KONECT PDZBase dataset). The goal is to predict future or undiscovered interactions between proteins.

### Methodology & Pipeline
-   **Problem Formulation**: Framed the task as a supervised binary classification problem by defining positive samples (removable edges) and negative samples (non-existent edges).
-   **Feature Engineering with Graph Embeddings**: Used the **Node2Vec** algorithm to learn low-dimensional feature representations (embeddings) for each protein.
-   **Classification & Critical Evaluation**: Trained a `RandomForestClassifier` and identified the **Accuracy Paradox** due to severe class imbalance, highlighting the importance of using appropriate evaluation metrics (like F1-score or AUC) in real-world scenarios.

---

## 💻 Technologies Used

-   **Core Libraries**: `Python`, `NetworkX`, `Pandas`, `Matplotlib`, `NumPy`
-   **Machine Learning / Graph ML**: `Scikit-learn`, `Node2Vec`

---

## ✍️ Author

-   Antonios Barotsakis

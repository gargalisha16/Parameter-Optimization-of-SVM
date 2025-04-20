# Parameter-Optimization-of-SVM
Iris Dataset Clustering Assignment

This project focuses on applying unsupervised clustering techniques to the well-known Iris dataset, incorporating various preprocessing strategies and clustering algorithms. The effectiveness of each approach is assessed using three commonly used clustering evaluation metrics.

Dataset Overview

Source: sklearn.datasets.load_iris()

Features: Four numerical attributes representing the physical characteristics of iris flowers

Target: Iris species (used solely for reference and not for model training)

Clustering Algorithms Implemented

K-Means Clustering

Agglomerative (Hierarchical) Clustering

Mean Shift Clustering

Preprocessing Techniques Explored

Raw: No modifications

Normalized: StandardScaler

Transformed: PowerTransformer

PCA: Principal Component Analysis (reduced to 2 components)

Normalized + Transformed: Combination of StandardScaler and PowerTransformer

Normalized + Transformed + PCA: StandardScaler and PowerTransformer followed by PCA (2 components)

Evaluation Metrics Used

Silhouette Score (higher values indicate better-defined clusters)

Calinski-Harabasz Index (higher values suggest more distinct clusters)

Davies-Bouldin Score (lower values are preferable)

Summary of Results
Clustering was performed with 2, 3, 4, and 5 clusters for both KMeans and Hierarchical algorithms. Mean Shift determined the number of clusters based on the estimated bandwidth.

Top Performing Configuration

Algorithm: Hierarchical Clustering

Preprocessing: PCA

Number of Clusters: 2

Silhouette Score: 0.7112

This configuration delivered the most compact and well-separated clusters among all combinations.

Key Observations

Hierarchical Clustering with PCA showed the best overall performance.

KMeans provided stable results but had slightly lower silhouette scores.

Mean Shift's effectiveness varied depending on preprocessing and bandwidth.

Combining normalization with transformation improved results in certain scenarios, especially for Hierarchical Clustering.

PCA contributed positively by reducing dimensionality and improving clustering quality in some cases.

Silhouette Score Comparison
A chart was used to visualize the silhouette scores across all combinations of preprocessing methods and clustering algorithms.

Conclusion
The success of clustering models is significantly affected by preprocessing choices. In this project, Hierarchical Clustering paired with PCA preprocessing produced the best clustering separation according to the silhouette score. This highlights the importance of experimenting with various preprocessing and clustering combinations when working on real-world datasets.









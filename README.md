# Parameter-Optimization-of-SVM

# Iris Dataset Clustering Assignment

This project applies unsupervised clustering techniques to the Iris dataset, exploring the impact of various preprocessing strategies and clustering algorithms. Clustering performance is evaluated using standard clustering metrics to determine the most effective approach.

## 📁 Dataset

- **Source**: `sklearn.datasets.load_iris()`
- **Features**: 4 numerical attributes describing the morphology of iris flowers
- **Target**: Iris species (used only for evaluation, not for training)

## ⚙️ Clustering Algorithms Used

- K-Means Clustering  
- Agglomerative (Hierarchical) Clustering  
- Mean Shift Clustering  

## 🔧 Preprocessing Techniques

- **Raw**: No transformation applied  
- **Normalized**: StandardScaler  
- **Transformed**: PowerTransformer  
- **PCA**: Principal Component Analysis (2 components)  
- **Norm + Trans**: StandardScaler followed by PowerTransformer  
- **Norm + Trans + PCA**: StandardScaler + PowerTransformer + PCA (2D)

## 📏 Evaluation Metrics

- **Silhouette Score**: Higher values indicate better-defined clusters  
- **Calinski-Harabasz Index**: Higher values reflect better separation  
- **Davies-Bouldin Score**: Lower values signify better clustering

## 📋 Results Summary

Clustering was conducted with 2, 3, 4, and 5 clusters for both KMeans and Hierarchical methods. Mean Shift determined the number of clusters automatically based on bandwidth estimation.

## 🏆 Best Clustering Configuration

| Algorithm     | Preprocessing | Number of Clusters | Silhouette Score |
|--------------|----------------|--------------------|------------------|
| Hierarchical | PCA            | 2                  | 0.7112           |

This configuration produced the most compact and well-separated clusters among all tested setups.

## 📌 Observations

- Hierarchical Clustering with PCA yielded the highest overall performance.
- KMeans showed consistent results but slightly lower silhouette scores.
- Mean Shift's results were variable, depending on preprocessing and bandwidth.
- Normalization combined with transformation improved clustering in certain cases, especially for Hierarchical Clustering.
- PCA helped reduce dimensionality and enhanced clustering performance in some scenarios.

## 📈 Silhouette Score Visualization

A chart was generated to compare silhouette scores across different combinations of preprocessing techniques and clustering algorithms.

## ✅ Conclusion

Clustering effectiveness is significantly influenced by preprocessing choices. In this project, Hierarchical Clustering combined with PCA preprocessing delivered the best results based on the silhouette score. This highlights the importance of experimenting with multiple preprocessing and clustering strategies when analyzing real-world datasets.










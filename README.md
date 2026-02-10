# 🧠 Unsupervised Learning & Anomaly Detection Project

This project demonstrates core concepts of **Unsupervised Machine Learning**, divided into two major parts:

* **Part 1 → Clustering Algorithms**
* **Part 2 → Anomaly Detection & Dimensionality Reduction**

The objective is to explore structure in unlabeled data, detect patterns, identify dense regions, and discover anomalies without predefined labels.

---

# 📂 Project Structure

```
├── Part1_Clustering.ipynb
├── Part2_Anomaly_Detection.ipynb
├── dataset.csv
└── README.md
```

---

# 🚀 Part 1 – Clustering Algorithms

## 📌 What is Clustering?

Clustering is an unsupervised learning technique used to group similar data points together based on feature similarity.

Goal:

> Maximize intra-cluster similarity and minimize inter-cluster similarity.

No labeled output is required.

---

## 1️⃣ K-Means Clustering

A centroid-based clustering algorithm.

### Working:

1. Choose number of clusters (K)
2. Initialize centroids randomly
3. Assign points to nearest centroid (Euclidean distance)
4. Update centroids
5. Repeat until convergence

### Objective:

Minimize Within-Cluster Sum of Squares (WCSS):

[
WCSS = \sum ||x_i - \mu_k||^2
]

### Key Characteristics:

* Works well for spherical clusters
* Sensitive to outliers
* Requires predefined K

---

## 2️⃣ Hierarchical Clustering

Builds clusters using a tree-like structure (Dendrogram).

### Types:

* Agglomerative (bottom-up)
* Divisive (top-down)

### Linkage Methods:

* Ward
* Complete
* Average
* Single

### Advantages:

* No need to specify number of clusters initially
* Useful for understanding hierarchical relationships

---

## 3️⃣ DBSCAN (Density-Based Clustering)

Density-Based Spatial Clustering of Applications with Noise.

### Key Parameters:

* `eps` → radius of neighborhood
* `min_samples` → minimum points to form dense region

### Concepts:

* Core Points
* Border Points
* Noise Points

### Advantages:

* Detects arbitrary shaped clusters
* Handles noise effectively
* No need to define number of clusters

Unlike K-Means, DBSCAN can identify outliers automatically.

---

# 🚀 Part 2 – Anomaly Detection & Dimensionality Reduction

This part focuses on identifying abnormal data points and reducing dimensional complexity.

---

## 1️⃣ Isolation Forest

An ensemble-based anomaly detection algorithm.

### Core Idea:

Anomalies are easier to isolate than normal points.

It randomly:

* Selects a feature
* Splits values
* Builds isolation trees

### Key Insight:

* Shorter path length → More likely anomaly
* Longer path length → Normal data

Efficient for high-dimensional datasets.

---

## 2️⃣ Local Outlier Factor (LOF)

Density-based anomaly detection method.

### Concept:

Compares local density of a point with its neighbors.

If a point has significantly lower density than its neighbors → Outlier.

### LOF Score:

* ≈ 1 → Normal
* > 1 → Possible anomaly

Useful when anomalies are context-dependent.

---

## 3️⃣ Noise Detection

Noise refers to:

* Random errors
* Irrelevant data
* Extreme outliers

Techniques used:

* DBSCAN noise labeling
* LOF scoring
* Isolation Forest anomaly score

Noise removal improves clustering performance and model stability.

---

## 4️⃣ PCA (Principal Component Analysis)

Dimensionality Reduction technique.

### Why PCA?

* Reduce feature space
* Remove multicollinearity
* Improve visualization
* Reduce computational cost

PCA transforms features into orthogonal components ordered by variance.

Example:
10 features → Reduced to 2 principal components.

Explained Variance Ratio helps determine retained information.

---

# 📊 Comparison of Techniques

| Method           | Type                     | Requires Labels | Detects Noise | Requires K |
| ---------------- | ------------------------ | --------------- | ------------- | ---------- |
| K-Means          | Clustering               | No              | No            | Yes        |
| Hierarchical     | Clustering               | No              | No            | No         |
| DBSCAN           | Clustering               | No              | Yes           | No         |
| Isolation Forest | Anomaly Detection        | No              | Yes           | No         |
| LOF              | Anomaly Detection        | No              | Yes           | No         |
| PCA              | Dimensionality Reduction | No              | No            | No         |

---

# 🛠 Preprocessing Techniques Used

* Data Cleaning
* Scaling (StandardScaler / MinMaxScaler)
* Feature Engineering
* Outlier Handling
* Dimensionality Reduction (PCA)

Scaling is critical because distance-based algorithms are sensitive to magnitude differences.

---

# 📈 Visualization

* Cluster scatter plots
* Dendrogram
* DBSCAN cluster + noise visualization
* PCA projection plots
* Anomaly detection plots

---

# 🎯 Key Learnings

* Different clustering algorithms behave differently depending on data distribution.
* Density-based methods handle noise better than centroid-based methods.
* Isolation Forest is highly efficient for anomaly detection.
* LOF works well for local density anomalies.
* PCA improves performance and visualization in high-dimensional data.

---

# 🧪 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* SciPy

---

# 🏁 Conclusion

This project provides a complete understanding of:

* Clustering Techniques
* Density-Based Methods
* Anomaly Detection Algorithms
* Noise Identification
* Dimensionality Reduction

It demonstrates how unsupervised learning can extract hidden structure and detect irregular patterns in real-world datasets.


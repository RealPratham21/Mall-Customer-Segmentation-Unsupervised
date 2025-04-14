# 📊 Customer Segmentation Using Clustering Algorithms
**Credits**: Prathamesh Bhamare.
**Linkedin**: https://www.linkedin.com/in/prathamesh-bhamare-7480b52b2/

This project applies and compares multiple clustering algorithms — **KMeans**, **Agglomerative Clustering**, and **DBSCAN** — to perform customer segmentation based on various combinations of customer features such as:

- Age
- Annual Income
- Spending Score

The primary goal is to understand the grouping behavior of customers using unsupervised learning techniques and evaluate the quality of these groupings with clustering metrics.

---

## 📁 Dataset

- Source: [Mall Customer Segmentation Dataset](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial)
- Features Used:
  - `Age`
  - `Annual Income`
  - `Spending Score`

---

## 📌 Clustering Techniques Used

The following algorithms were applied and evaluated on different combinations of features:

1. **KMeans**
2. **Agglomerative Clustering (Hierarchical)**
3. **DBSCAN (Density-Based)**

Each model's clustering quality was evaluated using:

- **Silhouette Score**: Higher is better (range: -1 to 1)
- **Davies-Bouldin Score**: Lower is better (range: 0 to ∞)

---

## 📈 Evaluation Results

| Algorithm            | Features Used                               | Clusters / Eps | Silhouette Score | Davies-Bouldin Score |
|----------------------|----------------------------------------------|----------------|------------------|-----------------------|
| KMeans               | Spending Score, Annual Income                | 5              | **0.5539**        | 0.5726                |
| Agglomerative        | Spending Score, Annual Income                | 5              | 0.5530           | 0.5782                |
| DBSCAN               | Spending Score, Annual Income                | eps=9          | **0.5567**        | **0.5134**            |
| KMeans               | Age, Spending Score                          | 3              | 0.4537           | 0.8239                |
| Agglomerative        | Age, Spending Score                          | 5              | 0.4037           | 0.8285                |
| DBSCAN               | Age, Spending Score                          | eps=5.85       | 0.3256           | 0.6855                |
| KMeans               | Age, Annual Income, Spending Score           | 6              | 0.4510           | 0.7515                |
| Agglomerative        | Age, Annual Income, Spending Score           | 6              | 0.4431           | 0.7685                |
| DBSCAN               | Age, Annual Income, Spending Score           | eps=6          | **0.6676**        | **0.4406**            |
| KMeans               | Age, Annual Income, Age, Spending Score      | 6              | 0.4507           | 0.7521                |
| DBSCAN               | Age, Annual Income, Age, Spending Score      | eps=7          | 0.5436           | 0.5916                |
| Agglomerative        | Age, Annual Income, Age, Spending Score      | 6              | 0.4428           | 0.7690                |

---

## ✅ Observations

- **DBSCAN** performed surprisingly well on the 3D dataset (`Age`, `Annual Income`, `Spending Score`) with the **highest silhouette score (0.6676)** and **lowest Davies-Bouldin score (0.4406)**.
- In 2D cases, **KMeans** and **DBSCAN** often had comparable results, but DBSCAN outperformed in scenarios with better-defined density-based clusters.
- **Agglomerative Clustering** produced reasonably good clusters but typically underperformed slightly compared to the other methods in terms of evaluation metrics.

---

## 🛠 Tools & Libraries

- `scikit-learn`
- `matplotlib`
- `seaborn`
- `numpy`
- `pandas`

---

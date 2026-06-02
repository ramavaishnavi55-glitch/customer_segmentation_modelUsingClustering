# customer_segmentation_modelUsingClustering
Customer segmentation model is about dividing customers into n groups with the help of K means algorithm and using features like Gender , income , Expenditure . The model is trained without labels.

# Customer Segmentation using K-Means Clustering

## Project Overview

This project performs customer segmentation using the K-Means Clustering algorithm. Customer data is grouped based on annual income and spending score to identify different purchasing behaviors and customer categories.

The project demonstrates how unsupervised machine learning can discover hidden patterns in data without using target labels.

---

## Problem Statement

Businesses often serve customers with different spending habits and income levels. Understanding these customer groups helps organizations create targeted marketing campaigns and improve customer engagement.

The objective of this project is to segment customers into meaningful clusters based on their annual income and spending score.

---

## Dataset Features

| Feature                | Description                       |
| ---------------------- | --------------------------------- |
| CustomerID             | Unique customer identifier        |
| Gender                 | Customer gender                   |
| Age                    | Customer age                      |
| Annual Income (k$)     | Annual income in thousand dollars |
| Spending Score (1-100) | Customer spending score           |

---

## Technologies Used

* Python
* Pandas
* Matplotlib
* Scikit-Learn

---

## Project Workflow

### 1. Data Loading

* Loaded the Mall Customers dataset using Pandas.
* Verified the dataset structure using:

  * head()
  * shape
  * info()

### 2. Feature Selection

Selected:

* Annual Income (k$)
* Spending Score (1-100)

These features provide clear customer purchasing patterns suitable for clustering.

### 3. Elbow Method

Applied the Elbow Method to determine the optimal number of clusters.

The method evaluates WCSS (Within Cluster Sum of Squares) for different values of K and identifies the point where improvement begins to slow down.

Optimal value selected:

**K = 5**

### 4. K-Means Clustering

Applied the K-Means algorithm using:

```python
KMeans(
    n_clusters=5,
    init='k-means++',
    random_state=42
)
```

The algorithm grouped customers into five clusters based on their similarity.

### 5. Cluster Visualization

Visualized customer clusters using a scatter plot:

* X-axis → Annual Income (k$)
* Y-axis → Spending Score (1-100)

Centroids were highlighted to represent the center of each cluster.

---

## Cluster Analysis

### Cluster 1 – Low Income, Low Spending

* Budget-conscious customers
* Lower purchasing activity
* Responsive to discounts and offers

### Cluster 2 – Low Income, High Spending

* High spending behavior despite lower income
* Frequent shoppers
* Potential loyal customers

### Cluster 3 – Medium Income, High Spending

* Active and valuable customers
* Consistent purchasing behavior
* Strong customer engagement

### Cluster 4 – High Income, Medium-High Spending

* Premium customer segment
* Significant contribution to business revenue
* Suitable for premium services

### Cluster 5 – High Income, Moderate Spending

* High earning customers
* Untapped business potential
* Ideal target for personalized marketing

---

## Results

Successfully segmented customers into five distinct groups based on income and spending behavior.

The clustering results can help businesses:

* Improve customer targeting
* Design personalized marketing campaigns
* Increase customer retention
* Understand customer purchasing patterns

---

## Learning Outcomes

Through this project, I learned:

* Unsupervised Machine Learning
* K-Means Clustering
* Elbow Method
* Customer Segmentation
* Cluster Visualization
* Centroid Analysis
* Business Interpretation of Clusters

---

## Future Improvements

* Use the complete Mall Customers dataset
* Include additional features such as Age and Gender
* Compare K-Means with Hierarchical Clustering
* Experiment with DBSCAN clustering
* Develop an interactive customer segmentation dashboard

---

## Conclusion

This project demonstrates the practical application of K-Means Clustering for customer segmentation. By analyzing annual income and spending score, customers were grouped into meaningful clusters that can help businesses make data-driven marketing and customer engagement decisions.


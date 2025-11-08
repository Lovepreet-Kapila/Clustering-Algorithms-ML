**Unsupervised Clustering:** 
DBSCAN, KMeans, & PCAA hands-on exploration of clustering techniques using Python and scikit-learn. 
This project demonstrates how different unsupervised learning algorithms group data based on similarity and structure. This notebook compares two major clustering types:Centroid-Based (KMeans): Groups data by finding central points (centroids).Density-Based (DBSCAN): Groups data by finding areas of high concentration.
It also uses Principal Component Analysis (PCA) to visualize these high-dimensional clusters in 2D.

**Objectives**
Implement KMeans and find optimal clusters using the "Elbow Method."
Implement DBSCAN and understand the effect of its eps and min_samples parameters.
Apply PCA to reduce dataset dimensionality for visualization.
Compare and contrast the results of density-based vs. centroid-based clustering.

**Tech Stack** 
**Language:** Python 3

**Libraries:** Scikit-Learn (for KMeans, DBSCAN, PCA), Pandas, NumPy

**Visualization:** Matplotlib, Seaborn

**Tools:** Jupyter Notebook

**Techniques Explored**:

1. **KMeans Clustering (Centroid-Based)**: Partitions data into $k$ distinct, non-overlapping clusters. It assigns data points to the nearest cluster mean (centroid).

   **Key Features:**
   Requires the number of clusters ($k$) to be specified beforehand.
   Uses the Elbow Method to help estimate the optimal $k$.
   Fast and efficient on large datasets.
   Works best when clusters are spherical and evenly sized.

2.**DBSCAN (Density-Based)**: Groups together points that are closely packed, marking points that lie alone in low-density regions as outliers (noise).

**Key Features:**
   Does not require the number of clusters to be specified.
   Can find arbitrarily shaped clusters (e.g., non-spherical).
   Excellent at identifying noise/outliers (a key advantage).
   Sensitive to parameters: eps (distance) and min_samples (density).
   
3. **Principal Component Analysis (PCA)**: A dimensionality reduction technique. It transforms the data into a new set of "principal components" that capture the maximum possible variance.

   **Key Features:**
Used here to visualize 3+ dimensional data in 2D.
Helps to see how well the clustering algorithms actually separated the data.
Reduces noise by filtering out dimensions with low variance.

**What I Learned**

**No "One-Size-Fits-All":** The choice of clustering algorithm is critical. KMeans failed where DBSCAN succeeded (and vice-versa) depending on the data's shape and density.

**Hyperparameter Tuning:** Learned the impact of tuning $k$ in KMeans (using the elbow plot) and eps in DBSCAN, which completely changes the cluster results.

**DBSCAN for Noise:** Discovered that DBSCAN is a powerful tool for outlier detection, which is something KMeans cannot do natively.

**PCA is for Visualization:** Realized how difficult it is to "see" clusters without a tool like PCA. It's an essential technique for interpreting unsupervised models.

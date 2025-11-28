Report: Clustering and PCA (Example 03.1 and 03.2)

Clustering analysis was performed on Portuguese 2019 Agricultural Census data.

Two main goals guided the analysis:
- Perform clustering on the original dataset (Example 03.1)
- Improve clustering quality by applying PCA and removing outliers (Example 03.2)

The final result compares clusters produced before and after dimensionality reduction and outlier removal.

Data Exploration:
- The dataset contains 3068 observations and 16 variables
- Numerical variables include education, labour structure, production value, area
- Three variables (freguesia, municipality, NUTS2) are categorical and were removed before clustering
- Initial plots showed strong variability and many outliers

Clustering on Raw Data (Example 03.1)
Process:
- Standardized the numerical variables
- K-Means: elbow method suggested ~4 clusters
- Agglomerative clustering (Ward linkage): also suggested 4 clusters
- PCA used only for visualization

Outcome:
- Clusters existed but were distorted by extreme outliers
- PCA scatterplot was heavily biased by a few samples
- Cluster separation was unclear

Improving Clustering with PCA + Outlier Removal (Example 03.2)
Outlier Removal:
- Isolation Forest removed 286 outliers (~10%)
- Data distributions became more regular

PCA:
- 2 components retained ~64% of variance
- PCA plot showed a clearer structure compared to the raw data

Clustering on PCA Data
- K-Means with 4 clusters
- Agglomerative clustering also with 4 clusters
- Both produced more stable and visually separated clusters

Overall:
PCA + outlier removal significantly improved clustering quality and visualization. The patterns became clearer and the clusters more stable

Conclusions:
- Outliers strongly affect unsupervised learning and should be removed
- PCA helps simplify data and improves cluster visualization
- K-Means and Agglomerative clustering give consistent results after preprocessing

- The improved workflow is: clean -> scale -> PCA -> cluster -> interpret

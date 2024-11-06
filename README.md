# Wine Quality Analysis, Clustering, and PCA

## Project Overview

This project involves analyzing the red wine dataset (`winequality-red.csv`) to explore the relationships between wine features, perform clustering with K-Means, and reduce dimensionality using Principal Component Analysis (PCA). The following steps are carried out:

1. **Data Exploration & Preprocessing**
2. **Clustering using K-Means**
3. **Principal Component Analysis (PCA) for Dimensionality Reduction**

## Project Goals

The goal of this project is to:
- Analyze and preprocess a red wine dataset to explore how various features correlate with each other.
- Perform clustering on the wine dataset to identify groups of wines with similar characteristics using K-Means clustering.
- Apply PCA to reduce the dimensionality of the dataset and visualize the results in two dimensions.

## Steps Overview

### Step 1: Data Exploration
In this initial step, we explored and understood the dataset by performing the following:

- **Basic Statistics**: We calculated basic statistics to understand the distribution of features in the dataset.
- **Correlation Heatmap**: A heatmap was used to visualize the correlation between different features and identify any potential patterns.
- **Quality Distribution**: A countplot was created to visualize the distribution of wine quality ratings.

### Step 2: Data Preprocessing
Data preprocessing was performed to ensure that the data was ready for modeling:

- **Skewness Handling**: Features with high skewness were transformed using the Yeo-Johnson Power Transformer to make the data more normally distributed.
- **Outlier Handling**: Outliers were removed using the Interquartile Range (IQR) method. Extreme values were replaced with the median of the respective feature.
- **Label Encoding**: The `quality` column, representing wine quality ratings, was label-encoded into numeric values for consistency in further analysis.

### Step 3: Feature Scaling
StandardScaler was used to scale the features, ensuring that all features have a mean of 0 and a standard deviation of 1. This helps prevent features with larger magnitudes from dominating the clustering algorithm.

### Step 4: K-Means Clustering
The K-Means clustering algorithm was used to identify groups of wines with similar characteristics:

- **Elbow Method**: We used the Elbow Method to determine the optimal number of clusters (k). In this project, we found that the optimal number of clusters is `k=4`.
- **Clustering**: After determining the optimal k, K-Means clustering was applied to the scaled dataset to assign cluster labels to the wines.

### Step 5: Visualizing Clusters
After performing clustering, we visualized the resulting clusters:

- **PCA Visualization**: Principal Component Analysis (PCA) was used to reduce the dataset from high-dimensional space to just two dimensions (PC1 and PC2). The clusters were then visualized in a 2D plot.

## Conclusion
In this project, we successfully:

- Explored and preprocessed the wine dataset, addressing skewness, outliers, and scaling the features.
- Applied K-Means clustering to group wines with similar characteristics.
- Visualized the clusters using PCA to reduce the dimensions and see how the wines group in 2D space.

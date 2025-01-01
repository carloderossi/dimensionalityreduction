# Mushroom Dataset Dimensionality Reduction Project

## Overview

This project focuses on applying dimensionality reduction techniques to the Mushroom Dataset. The aim is to reduce the number of features while maintaining as much information as possible, facilitating easier visualization and better model performance.

## Dataset

The Mushroom Dataset contains several categorical features describing various physical characteristics of mushrooms, with the target variable indicating whether the mushroom is edible or poisonous.

## Objective

The objective of this project is to apply various dimensionality reduction techniques and evaluate their effectiveness in preserving the important information within the dataset.

## Approach

1. **Data Preprocessing**:
   - Handling missing values
   - Encoding categorical variables
   - Normalizing the data
   - Splitting the dataset into training and testing sets

2. **Exploratory Data Analysis (EDA)**:
   - Analyzing the distribution of features
   - Visualizing the data using various plots

3. **Dimensionality Reduction Techniques**:
   - Principal Component Analysis (PCA)
   - t-Distributed Stochastic Neighbor Embedding (t-SNE)
   - Linear Discriminant Analysis (LDA)

4. **Evaluation**:
   - Comparing the explained variance ratio for PCA
   - Visualizing the clusters formed by t-SNE and LDA
   - Assessing the impact of dimensionality reduction on classification performance

## Results

The results section includes:
- **PCA**: Explained variance ratio and scree plot
- **t-SNE**: Visualization of clusters
- **LDA**: Visualization of clusters and explained variance

## Model Recommendation

### Comparing PCA, t-SNE, and Autoencoders

**Principal Component Analysis (PCA):**
- **Purpose:** Dimensionality reduction while preserving variance.
- **Variance Retention:**
  - 95% Variance: 59 components.
  - 90% Variance: 50 components.
  - 85% Variance: 42 components.
- **Interpretability:** Transforms data into uncorrelated axes.
- **Speed:** Computationally efficient.
- **Use Cases:** Exploratory data analysis, noise reduction, and feature extraction.

**t-Distributed Stochastic Neighbor Embedding (t-SNE):**
- **Purpose:** Visualizing high-dimensional data in 2D or 3D.
- **Perplexity Variations:**
  - Perplexity = 30: Detailed, tight clusters.
  - Perplexity = 50: Balanced local and global structures.
  - Perplexity = 100: Broader patterns with larger clusters.
- **Interpretability:** Powerful for visualizing clusters, but axes are not directly interpretable.
- **Speed:** Computationally intensive.
- **Use Cases:** Visualizing clustering behavior and gaining insights into data structure.

**Autoencoders:**
- **Purpose:** Data compression and reconstruction using neural networks.
- **Bottleneck Layer Variations:**
  - Bottleneck Size 10: Best reconstruction with lower loss.
  - Bottleneck Size 5: Good balance between compression and reconstruction.
  - Bottleneck Size 3: Higher loss, less effective reconstruction.
- **Interpretability:** Less interpretable compared to PCA, but captures complex non-linear relationships.
- **Speed:** Training can be slow, performance depends on architecture and hyperparameters.
- **Use Cases:** Complex data compression, denoising, and feature learning for downstream tasks.

### Recommendation

Choosing the right model depends on your specific goals and dataset characteristics:

**For Dimensionality Reduction and Feature Extraction:**
- **PCA** is robust due to its interpretability and efficiency, making it suitable for further analysis and machine learning tasks.

**For Visualization and Understanding Data Structure:**
- **t-SNE** is ideal for visualizing high-dimensional data in a lower-dimensional space, providing intuitive visual insights.

**For Advanced Data Compression and Feature Learning:**
- **Autoencoders** are preferred for capturing intricate patterns in complex, non-linear data.

### Final Decision

**PCA**: Recommended for reducing dimensionality for further analysis or machine learning models while maintaining interpretability and efficiency.

### Next Steps

#### Limitations of PCA

1. **Linearity:**
   - **Limitation:** Captures only linear relationships.
   - **Improvement:** Use kernel PCA to capture non-linear relationships.

2. **Sensitivity to Scaling:**
   - **Limitation:** Sensitive to feature scale.
   - **Improvement:** Standardize or normalize the data before applying PCA.

3. **Interpretability of Components:**
   - **Limitation:** Principal components can be difficult to interpret.
   - **Improvement:** Use varimax rotation for better interpretation.

4. **Variance-Based:**
   - **Limitation:** Maximizes variance, not always the most informative features.
   - **Improvement:** Complement PCA with Linear Discriminant Analysis (LDA).

5. **Sensitivity to Outliers:**
   - **Limitation:** Sensitive to outliers.
   - **Improvement:** Pre-process data to handle outliers or use robust PCA methods.

#### Improving PCA

1. **Kernel PCA:**
   - Capture non-linear relationships using kernel functions.

2. **Standardization/Normalization:**
   - Ensure features contribute equally using StandardScaler or MinMaxScaler.

3. **Rotation Techniques:**
   - Simplify component interpretation with varimax rotation.

4. **Hybrid Approaches:**
   - Combine PCA with LDA for retaining variance and class separability.

5. **Handling Outliers:**
   - Detect and handle outliers with robust scaling or robust PCA methods.

6. **Dimensionality Selection:**
   - Retain components based on cumulative explained variance (e.g., 95%).

### Conclusion

#### Comparison Between KernelPCA and PCA

**KernelPCA:**
- **Linear Kernel:** Distinct clusters for edible and poisonous mushrooms, with slightly different distribution.
- **Polynomial Kernel:** More complex clustering pattern with tighter clusters.
- **RBF Kernel:** Non-linear separation with clearer distinction, capturing complex relationships.

**PCA:**
- **Principal Components:** Captures linear relationships, maximizing variance.
- **Interpretability:** Easier to interpret linear combinations of original features.
- **Efficiency:** Computationally efficient and straightforward to implement.

#### Conclusion: KernelPCA vs. PCA for the Mushroom Dataset

**KernelPCA** is preferred for capturing complex, non-linear relationships and improving class separation in the Mushroom dataset. It offers flexibility with different kernel functions and demonstrates a nuanced understanding of data structure. For tasks requiring non-linear separation, KernelPCA is a better choice. However, for linear relationships and simplicity, **PCA** remains effective and explainable.

Depending on data characteristics and analysis goals, choose KernelPCA for flexibility and complex datasets, or PCA for simplicity and efficiency. If computational resources and complexity are not major constraints, KernelPCA is optimal.


## References

- [Mushroom Dataset](https://archive.ics.uci.edu/ml/datasets/Mushroom)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)

## Author

Carlo De Rossi

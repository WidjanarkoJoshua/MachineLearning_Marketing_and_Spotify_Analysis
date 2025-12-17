# Unsupervised Learning for Marketing and Spotify Campaign Insights

## Recruiter TL;DR
- **Problem:** Marketing and media platforms often need to segment users and content with limited or noisy labels.
- **Solution:** Applied unsupervised learning to uncover latent structure and improve downstream campaign prediction.
- **Data:** Spotify audio feature data and a real-world marketing campaign dataset.
- **Approach:** K-Means, Gaussian Mixture Models (EM), PCA, ICA, Random Projection, and neural network feature augmentation.
- **Key Result:** Clustering features improved rare-response detection in marketing campaigns and produced interpretable segments for Spotify-style content promotion.
- **Skills Demonstrated:** Customer segmentation, campaign analytics, unsupervised learning, feature engineering, and applied machine learning.

---

## Overview
This project explores how unsupervised learning techniques can support marketing decision-making and content-based campaigns when labeled data is limited. Clustering and dimensionality reduction were applied to two datasets to uncover hidden structure and evaluate how these representations affect downstream predictive performance.

---

## Motivation
Marketing teams and media platforms such as Spotify must often:
- Segment users or content without explicit labels
- Work with high-dimensional, noisy behavioral data
- Improve targeting and personalization under uncertainty

Unsupervised learning provides tools to discover natural segments, reduce redundancy, and enhance supervised models without requiring additional labels.

---

## Datasets

### Spotify Songs Dataset
- Audio features describing musical structure and style
- Popularity metrics excluded to focus on intrinsic characteristics
- High feature correlation and non-Gaussian distributions
- Used to identify clusters useful for playlist curation and promotional campaigns

### Marketing Campaign Dataset
- Customer demographics, purchasing behavior, and engagement metrics
- Binary outcome indicating campaign responsiveness
- Strong class imbalance
- Used to evaluate segmentation quality and predictive uplift

---

## Methods

### Clustering
- K-Means
- Gaussian Mixture Models (Expectation Maximization)
- Evaluated using silhouette score and cluster stability

### Dimensionality Reduction
- Principal Component Analysis (PCA)
- Independent Component Analysis (ICA)
- Random Projection

### Supervised Model Augmentation
- Neural network trained on:
  - Original features
  - Dimension-reduced features
  - Original features augmented with cluster labels
- Performance evaluated using accuracy, recall, precision, and specificity

---

## Results and Insights
- Spotify data favored K-Means due to correlated, non-Gaussian features
- Dimensionality reduction improved cluster cohesion
- Cluster labels improved identification of rare positive responders in marketing campaigns
- Overall accuracy changes were modest, but segmentation improved actionable targeting
- For Marketing, was able to notice customer segments that do not respond to engagement campaigns and avoid wasting resources
- Also find customers in which we can find customers that are receptive and should be pushed for greater profit
- For Spotify, Clustering allows for targeted recommendation systems to find similar songs regardless of popularity

---

## Technologies Used
- Python 3.10
- TensorFlow
- scikit-learn
- NumPy
- pandas
- SciPy
- Matplotlib

---

## Future Work
- Apply segments to live A/B marketing experiments
- Compare against tree-based and linear campaign models
- Extend analysis to temporal user behavior
- Evaluate segment stability over time

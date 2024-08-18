# Comparative Analysis of Classical and Quantum K-means Clustering Algorithms

## 1. Introduction

Clustering analysis is critical in data mining and pattern recognition. The K-means algorithm, known for its simplicity and effectiveness, faces challenges with computational complexity and accuracy in complex datasets. Quantum computing promises enhanced computational efficiency, potentially improving clustering tasks. This project explores the performance of classical and quantum K-means algorithms using a custom dataset with varied cluster characteristics.

## 2. Problem Statement

We compare the classical K-means algorithm with a quantum K-means algorithm using a custom-generated dataset. The goal is to evaluate clustering accuracy, efficiency, and the impact of quantum effects.

## 3. Objectives

1. **Accuracy Assessment:** Compare clustering accuracy between quantum and classical K-means algorithms.
2. **High-Dimensional Handling:** Analyze the quantum algorithm's effectiveness on high-dimensional datasets.
3. **Computational Efficiency:** Evaluate quantum K-means for speedup and resource utilization.
4. **Quantum Effects:** Study the impact of qubit count and quantum circuit parameters on performance.

## 4. Methodology

### 4.1 Dataset

A synthetic dataset was generated using the `make_blobs()` function from `sklearn.datasets`, featuring:
- **n_samples:** 100
- **n_features:** 3
- **centers:** User-defined
- **cluster_std:** 2

### 4.2 Implementation Details

1. **Data Generation:** Synthetic data with defined parameters.
2. **Preprocessing:** Normalization of features.
3. **Quantum K-means Algorithm:**
   - **Centroid Initialization:** Random initialization of centroids.
   - **Quantum Distance Calculation:** Utilizes qubits for encoding data points and centroids, applying quantum gates and measurements to calculate distances.
   - **Assignment and Update:** Assign data points to nearest centroids and update centroids iteratively.
   - **Evaluation:** Accuracy compared with classical K-means.
4. **Classical K-means Algorithm:** Implemented for benchmark using Euclidean distance.

### 4.3 Quantum Algorithm Details:
   - **Qubit Encoding:** Data points and centroids encoded into qubits.
   - **Distance Calculation:** Based on quantum interference and measurements.

## 5. Results and Analysis

- **Experimental Setup:** 
  - **Classical K-means:** 100 iterations, 5 clusters.
  - **Quantum K-means:** Executed on a quantum simulator with a depth of 3.

- **Evaluation Metrics:**
  - **Best Accuracy:** Classical K-means 0.97, Quantum K-means 0.93
  - **Average Accuracy:** Classical K-means 0.93, Quantum K-means 0.91
  - **ARI Score:** Classical K-means 0.91, Quantum K-means 0.81
  - **NMI Score:** Classical K-means 0.89, Quantum K-means 0.82

- **Findings:** 
  - Classical K-means outperformed quantum K-means in accuracy and alignment with ground truth.
  - Quantum K-means demonstrated potential but showed limitations in current implementation.

## 6. Conclusion and Future Work

### 6.1 Conclusion

The study demonstrated that classical K-means clustering was more effective than quantum K-means for the given dataset. While quantum K-means shows promise, it requires further optimization and development to match classical methods' accuracy and efficiency.

### 6.2 Future Work

1. **Hybrid Approaches:** Explore combining classical and quantum methods for enhanced performance.
2. **Real-World Applications:** Test quantum K-means on real-world datasets.
3. **Optimization:** Develop optimization techniques specific to quantum K-means.
4. **Noise Handling:** Assess quantum K-means robustness to noisy data and develop noise-resistant techniques.

This research contributes to understanding quantum K-means clustering and paves the way for future advancements in quantum computing applications for clustering tasks.

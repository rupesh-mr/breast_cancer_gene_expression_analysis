
# Clustering Analysis of Breast Cancer Gene Expression Data (GSE45827)

This repository contains the code and analysis for our project on **unsupervised learning techniques applied to gene expression data** to identify subtypes of breast cancer. The dataset used is GSE45827 from the CuMiDa collection.

## 📁 Repository Contents

- `Code.ipynb`: Jupyter notebook with complete implementation including preprocessing, dimensionality reduction, clustering, and evaluation.
- `Report.pdf`: Final project report detailing the methodology, analysis, and findings.


## 📊 Project Overview

This study applies various clustering techniques to breast cancer gene expression data to identify potential subtypes and biomarkers.

### Objectives

- Apply clustering algorithms to discover hidden patterns or subgroups.
- Evaluate clustering performance against known subtype classifications.
- Identify potential biomarker genes for each discovered cluster.

### Dataset

- **Source**: [CuMiDa - GSE45827](https://www.kaggle.com/datasets/brunogrisci/breast-cancer-gene-expression-cumida)
- **Samples**: 151
- **Features**: 54,676 gene expression values
- **Known Classes**: 6 (Luminal A/B, HER2-enriched, Basal-like, Claudin-low, Normal-like)

---

## ⚙️ Methodology

### 🔬 Preprocessing

- Background correction and quantile normalization
- Removal of low variance genes
- Feature selection via ANOVA F-test (only for supervised insights)
- Dimensionality reduction using:
  - PCA (Principal Component Analysis)
  - UMAP (Uniform Manifold Approximation and Projection)

### 🤖 Clustering Algorithms

- K-Means (Euclidean and Mahalanobis)
- Agglomerative Clustering (with Cosine distance)
- DBSCAN
- Gaussian Mixture Models (GMM)
- Fuzzy C-Means (FCM)

### 📈 Evaluation Metrics

- **Silhouette Score**
- **Adjusted Rand Index (ARI)**
- **Purity Score**

---

## 🔍 Key Insights

- Optimal clustering across most methods was found at **k = 3**, despite the six known subtypes.
- **Agglomerative Clustering with Cosine Distance** and **GMM** performed best.
- Several **potential biomarker genes** were identified via statistical testing (t-test).
- UMAP provided superior nonlinear dimensionality reduction over PCA.
- DBSCAN underperformed due to high-dimensionality challenges.

---

## 📄 References

- Bruno Grisci. [CuMiDa Breast Cancer Dataset](https://www.kaggle.com/datasets/brunogrisci/breast-cancer-gene-expression-cumida)
- Nascimento et al. (2016), *Breast cancer diagnosis with ELM and thermography*. [Link](https://onlinelibrary.wiley.com/doi/full/10.1155/2016/4273813)

---
## 🧪 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/rupesh-mr/breast_cancer_gene_expression_analysis
   cd breast_cancer_gene_expression_analysis
   ```

2. Open and run the notebook:
   ```bash
   jupyter notebook Code.ipynb
   ```

---

## 📬 Contact

For questions or collaborations, reach out via [email](mailto:rupeshmr2005@gmail.com).

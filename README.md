# Bank Marketing Analysis: Customer Segmentation and Deposit Subscription Prediction

## 📖 Project Overview

This project applies data mining and machine learning techniques to analyze customer behavior in bank telemarketing campaigns. The objective is to segment customers based on campaign interaction characteristics and predict whether a customer will subscribe to a term deposit product.

The project combines unsupervised learning (K-Means and DBSCAN clustering) with supervised learning (Random Forest classification) to create a comprehensive data-driven analysis pipeline.

---

## 🎯 Objectives

- Perform comprehensive data preprocessing on the Bank Marketing Dataset.
- Compare customer segmentation performance between K-Means and DBSCAN.
- Build a predictive model for term deposit subscription using Random Forest.
- Handle class imbalance using SMOTE.
- Evaluate model performance using Stratified K-Fold Cross Validation.

---

## 📂 Dataset

**Dataset:** Bank Marketing Dataset

**Source:** UCI Machine Learning Repository

**Reference:**
Moro, S., Cortez, P., & Rita, P. (2014). A Data-Driven Approach to Predict the Success of Bank Telemarketing.

Target Variable:

- `y = yes` → Customer subscribes to a term deposit.
- `y = no` → Customer does not subscribe.

Dataset Size:

- 45,211 observations
- 17 variables

---

## ⚙️ Methodology

### 1. Exploratory Data Analysis (EDA)

- Dataset overview
- Missing value analysis
- Class imbalance analysis
- Feature distribution visualization

### 2. Data Preprocessing

- Missing value handling
- Domain-based imputation for `pdays` and `poutcome`
- Feature encoding
- Winsorization for outlier treatment
- Data leakage detection and removal
- PCA for multicollinearity reduction
- Log transformation
- Feature scaling

### 3. Clustering

#### K-Means

- Elbow Method
- Silhouette Score Evaluation
- Optimal cluster selection

#### DBSCAN

- Grid Search for:
  - `eps`
  - `min_samples`
- Noise detection
- Cluster quality evaluation

### 4. Classification

#### Random Forest

- Stratified 5-Fold Cross Validation
- SMOTE for class imbalance handling
- Threshold Adjustment (0.35)

---

## 📊 Results

### Clustering Performance

| Metric | K-Means | DBSCAN |
|----------|----------|----------|
| Silhouette Score | 0.6284 | 0.5127 |
| Davies-Bouldin Index | 0.5655 | 1.0718 |
| Number of Clusters | 3 | 4 |
| Noise Points | 0 | 12 |

K-Means produced better cluster separation and compactness compared to DBSCAN.

---

### Random Forest Performance

| Metric | Score |
|----------|----------|
| Accuracy | 0.8349 |
| F1 Macro | 0.6757 |
| F1 Minority Class | 0.4485 |
| AUC-ROC | 0.7792 |

Classification Report:

| Class | Precision | Recall | F1-Score |
|---------|-----------|---------|---------|
| No Subscription | 0.94 | 0.87 | 0.90 |
| Subscription | 0.37 | 0.57 | 0.45 |

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Imbalanced-Learn (SMOTE)

---

## 📈 Key Features

- End-to-end data mining workflow
- Advanced preprocessing techniques
- Customer segmentation using multiple clustering methods
- Class imbalance handling with SMOTE
- Threshold optimization for minority class detection
- Model evaluation with cross-validation

---

## 📁 Repository Structure

```text
├── data/
│   └── bank_marketing.csv
│
├── notebook/
│   └── bank_marketing_analysis.ipynb
│
│
└── README.md
```

---

## 🚀 How to Run

1. Clone the repository

```bash
git clone https://github.com/yourusername/bank-marketing-analysis.git
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Open the notebook

```bash
jupyter notebook
```

4. Run all cells sequentially.

---

## 👥 Authors

Data Mining Project

Bachelor of Data Science

Universitas Airlangga

Group 8

- Aditya Saputra
- Dendy Agus
- Steven Malow Purba
- Satrio Akhmad Kurniawan

---

## 📚 References

- Breiman, L. (2001). Random Forests.
- Chawla, N. V. et al. (2002). SMOTE.
- Ester, M. et al. (1996). DBSCAN.
- Moro, S. et al. (2014). Bank Marketing Dataset.
- Han, J., Pei, J., & Tong, H. (2023). Data Mining: Concepts and Techniques.

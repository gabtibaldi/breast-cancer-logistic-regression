# Breast Cancer Tumor Classification (Logistic Regression)

This repository contains a complete end-to-end binary classification pipeline using the **Breast Cancer Wisconsin (Diagnostic)** dataset from `sklearn.datasets`.  
The goal is to predict whether a tumor is **malignant (0)** or **benign (1)** using 10 numerical features (the `_mean` variables).

The project is implemented in a single Jupyter Notebook and focuses on both **model performance** and **interpretability for business/clinical decision-making**.

---

## 1. Project Overview

**Main objective:**  
Build and evaluate a Logistic Regression model to classify breast tumors based on morphological features extracted from digitized images of fine needle aspirates (FNA) of breast masses.

**Key aspects covered:**

- Exploratory Data Analysis (EDA)
- Data preprocessing (IQR capping / winsorization)
- Model building with `LogisticRegression` in a `Pipeline`
- Stratified 5-fold cross-validation (OOF predictions)
- Evaluation with multiple metrics:
  - Accuracy, Balanced Accuracy
  - F1-score
  - ROC–AUC and PR–AUC (Average Precision)
  - Confusion Matrix
- Model interpretability:
  - Coefficients and odds ratios
  - Most influential features
  - Analysis of decision threshold and “gray zone” around 0.5

This notebook is intended as a **didactic example** of how to structure a clean, end-to-end classification experiment for tabular data.

---

## 2. Dataset

- **Source:** `sklearn.datasets.load_breast_cancer`
- **Name:** Breast Cancer Wisconsin (Diagnostic)
- **Size:** 569 observations
- **Target:**
  - `0` = malignant  
  - `1` = benign
- **Features used:** only the 10 `_mean` variables:
  - mean radius  
  - mean texture  
  - mean perimeter  
  - mean area  
  - mean smoothness  
  - mean compactness  
  - mean concavity  
  - mean concave points  
  - mean symmetry  
  - mean fractal dimension  

The notebook uses a **compact version** of the dataset for clarity and interpretability.

---

## 3. Repository Structure

```text
.
├── breast_cancer_en.ipynb   # Main notebook (EDA, modeling, evaluation, interpretation)
└── README.md                # Project documentation

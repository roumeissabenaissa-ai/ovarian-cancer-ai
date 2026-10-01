# Ovarian Cancer Classification: Feature Extraction and Selection

## Overview

This project presents a comparative study of feature extraction and feature selection methods for the classification of high-dimensional biomedical data. 

The study focuses on an Ovarian Cancer Mass Spectrometry dataset containing **253 samples** and **15,154 spectral features**. The main objective is to identify relevant and informative features while reducing the dimensionality and complexity of the dataset. Several machine learning classifiers and feature selection approaches were evaluated and compared.

---

## Objectives

The main objectives of this project are to:

* Explore and analyze a high-dimensional biomedical dataset.
* Evaluate machine learning models without preprocessing.
* Apply data preprocessing techniques.
* Reduce dimensionality using PCA.
* Compare Filter, Wrapper, and Embedded feature selection methods.
* Evaluate the impact of selected features on classification performance.
* Identify a small subset of informative features for ovarian cancer classification.

---

## Dataset

* **Dataset:** Ovarian Cancer Mass Spectrometry
* **Source:** UCI Machine Learning Repository
* **Samples:** 253
* **Features:** 15,154 spectral features (based on mass-to-charge ($m/z$) values)
* **Target Variable:** Class
  * **Cancer:** 162 samples
  * **Normal:** 91 samples

---

## Methodology

The project follows several key stages:

### 1. Exploratory Data Analysis
The dataset was analyzed to investigate feature types, missing values, class distribution, feature distributions, outliers, and feature correlations. *(Note: No missing values were detected in the dataset.)*

### 2. Classification Without Preprocessing
Several machine learning classifiers were initially evaluated without feature extraction or selection:
* K-Nearest Neighbors (KNN)
* Support Vector Machine (SVM)
* Decision Tree
* Naive Bayes

Models were evaluated using Accuracy, Precision, Recall, and F1-score.

### 3. Data Preprocessing
* Feature standardization
* Class balancing using **SMOTE**
* Dimensionality reduction using **PCA** (configured to preserve approximately 90% of the total variance)

### 4. Feature Extraction
Principal Component Analysis (PCA) was used to transform the original high-dimensional feature space into a smaller set of principal components (retaining **12 principal components** while preserving ~90% of the variance).

### 5. Feature Selection
Three main categories of feature selection methods were investigated:
* **Filter Methods:** Chi-Square, Mutual Information, mRMR (Minimum Redundancy Maximum Relevance)
* **Wrapper Method:** SFS (Sequential Forward Selection)
* **Embedded Methods:** Decision Tree, Random Forest, Lasso Regression, SVM-RFE (Support Vector Machine Recursive Feature Elimination)

### 6. Feature Combination
The top features obtained from the best-performing selection approaches were combined and further analyzed. The final analysis identified **three highly influential features**:
1. `MZ224.09159`
2. `MZ437.0239`
3. `MZ245.24466`

---

## Results

### Classification Without Preprocessing
| Model | Accuracy |
| :--- | :--- |
| **SVM** | 98.04% |
| **KNN** | 93.14% |
| **Decision Tree** | 91.18% |
| **Naive Bayes** | 90.20% |

### PCA and Feature Selection
After dimensionality reduction and feature selection, models maintained high performance:
| Model | Accuracy |
| :--- | :--- |
| **SVM** | 97.1% |
| **Decision Tree** | 96.9% |
| **KNN** | 95.1% |
| **Naive Bayes** | 95.1% |

### Feature Selection Experiments
Using the three selected features (`MZ224.09159`, `MZ437.0239`, `MZ245.24466`), Logistic Regression, SVM, KNN, Naive Bayes, Decision Tree, and Random Forest were evaluated. Several models achieved accuracy close to or equal to **1.0**.

---

## Main Findings

* High-dimensional biomedical data can make classification challenging when the number of features far exceeds the number of samples.
* Preprocessing and dimensionality reduction successfully simplify the learning problem.
* Feature selection retains informative variables while considerably reducing dimensionality.
* Filter, Wrapper, and Embedded methods offer distinct advantages in identifying relevant features.
* Combining features selected by different approaches can produce a compact, high-performing feature subset.

We compared **Feature Selection** and **Feature Extraction** methods for high-dimensional biomedical data.

Our results showed that **Feature Selection was more effective in our experiments**, as it allowed us to:

- Considerably reduce the number of features.
- Retain the most informative original features.
- Achieve the **highest classification accuracy**.

Overall, Feature Selection provided a **smaller and more informative feature subset while maintaining better classification performance**.
---


## Technologies

* Python
* Machine Learning & Scikit-learn
* PCA & SMOTE
* Feature Selection & Statistical Analysis
* Biomedical Data Analysis


# Author

**Hamdane Salsabil & Benaissa Roumeissa**

Master 1 – SDIA

2025 / 2026

**Team Project**

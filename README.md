# Ovarian Cancer Classification: Feature Extraction and Selection

## Overview

This project presents a comparative study of **feature extraction and feature selection methods** for the classification of high-dimensional biomedical data.

The study focuses on an **Ovarian Cancer Mass Spectrometry dataset** containing 253 samples and 15,154 spectral features. The objective is to identify relevant features and evaluate their impact on machine learning classification.

## Dataset

**Dataset:** Ovarian Cancer Mass Spectrometry

- **Samples:** 253
- **Features:** 15,154 spectral features
- **Target variable:** Class
- **Classes:**
  - Cancer: 162 samples
  - Normal: 91 samples

The features represent measurements obtained from mass spectrometry data, with feature names based on mass-to-charge (`m/z`) values.

## Project

The project explores different approaches for feature extraction and feature selection, including:

- PCA (Principal Component Analysis)
- Chi-Square
- Mutual Information
- mRMR (Minimum Redundancy Maximum Relevance)
- SFS (Sequential Forward Selection)
- Decision Tree
- Random Forest
- Lasso Regression
- SVM-RFE (Support Vector Machine Recursive Feature Elimination)

Several machine learning classifiers were evaluated, including:

- KNN
- SVM
- Decision Tree
- Naive Bayes
- Logistic Regression
- Random Forest

## Technologies

- Python
- Scikit-learn
- Machine Learning
- PCA
- SMOTE
- Feature Selection
- Biomedical Data Analysis

## Authors

- Benaissa Roumeissa
- Hamdane Salsabil

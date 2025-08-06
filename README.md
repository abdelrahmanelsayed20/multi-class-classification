

# Multi-Class Network Traffic Classification

This repository presents a robust and modular approach to performing multi-class classification on network traffic data. The models were trained and evaluated using the CICIoT2023 dataset, focusing on accurate categorization of various benign and malicious network activities.

---

## 📦 Dataset

- File: `train.csv`
- Type: Tabular (numerical and categorical)
- Target Column: `label`
- Classes: 34 attack types + benign traffic
- Task: Multi-class classification

---

## 🚀 Approaches

### 1. Data Preprocessing

- Missing Value Handling: Replaced with median for numeric columns.
- Duplicate Removal: All duplicate rows removed.
- Encoding:
  - Label Encoding for target column.
  - One-hot encoding for categorical features.
- Feature Scaling: RobustScaler or StandardScaler used depending on experiment.
- Feature Selection: `SelectKBest` with ANOVA F-statistic, or RFE used to reduce dimensionality.

---

### 2. Models Implemented

| Model              | Notes                                      |
|-------------------|--------------------------------------------|
| Random Forest      | Ensemble of decision trees (baseline)      |
| XGBoost            | Gradient boosting (fast & accurate)        |
| LightGBM           | Leaf-wise boosting (memory efficient)      |
| Stacking Classifier| Combines RF, XGB, and LGBM via logistic regression |

All models are evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score (macro and weighted)
- Confusion Matrix

---

### 3. Handling Imbalanced Data

- SMOTE (Synthetic Minority Oversampling Technique) was used to balance the class distribution during training.
- Stratified train/test splits to preserve class ratios.

---

## 📊 Results Summary

| Model              | Accuracy | F1 Score | Precision | Recall |
|-------------------|----------|----------|-----------|--------|
| Random Forest      | ~        | ~        | ~         | ~      |
| XGBoost            | ~        | ~        | ~         | ~      |
| LightGBM           | ~        | ~        | ~         | ~      |
| Stacked Ensemble   | ~        | ~        | ~         | ~      |

(Detailed reports are printed via classification_report and visualized via matplotlib.)

---

## 🧪 Evaluation & Visualization

- Histograms of quantitative features
- Boxplots for outlier analysis
- Correlation heatmaps
- Label distribution plots
- Performance bar charts comparing classifiers

---

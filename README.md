#  Breast Cancer Classification using KNN & Logistic Regression

##  Project Overview
This project focuses on building and comparing machine learning models to classify breast cancer tumors as **Malignant** or **Benign** using clinical features extracted from cell nucleus images.

Two classification algorithms were implemented and evaluated:
- **K-Nearest Neighbors (KNN)**
- **Logistic Regression**

The project emphasizes proper **EDA**, **feature scaling**, **model evaluation**, and **model comparison**, following a real-world machine learning workflow.

---

##  Problem Statement
Early and accurate detection of breast cancer is critical for effective treatment.  
The objective of this project is to develop reliable classification models that can assist in predicting whether a tumor is malignant or benign based on numerical diagnostic features.

---

## Dataset Information
- **Dataset:** Breast Cancer Wisconsin (Diagnostic)
- **Source:** Built-in `scikit-learn` dataset
- **Samples:** 569
- **Features:** 30 numerical features
- **Target:**
  - `0` → Malignant
  - `1` → Benign
- **Missing Values:** None

The dataset contains measurements related to tumor size, shape, texture, and concavity.

---

## Exploratory Data Analysis (EDA)
EDA was performed to understand feature behavior and class separation.

Key findings:
- Malignant tumors tend to have larger radius, area, and irregular boundaries.
- Features such as `mean radius`, `mean area`, `mean concavity`, and `worst area` show strong class separation.
- Significant variation in feature scales confirmed the necessity of feature scaling.
- Correlation analysis revealed strong relationships among size-related features.

---

## Data Preprocessing
- Feature–target separation
- Train–test split with stratification
- Feature scaling using **StandardScaler** (mandatory for KNN)

---

## Models Implemented

### K-Nearest Neighbors (KNN)
- Distance-based classification
- Optimal value of `K` selected using error-rate analysis
- Sensitive to feature scaling

**Final Performance:**
- Accuracy: **97.36%**
- Strong recall and precision for both classes

---

### Logistic Regression
- Linear classification model
- Scaled features used for fair comparison

**Final Performance:**
- Accuracy: **98.25%**
- Precision, Recall, and F1-score ≈ **0.98** for both classes

---

## Model Comparison Summary

| Model | Accuracy |
|------|----------|
| KNN | 97.36% |
| Logistic Regression | **98.25%** |

**Final Model Selection:**  
**Logistic Regression**, due to higher accuracy, better generalization, interpretability, and computational efficiency.

---

## Key Insights
- Tumor size and shape-related features are the strongest predictors of malignancy.
- Feature scaling plays a critical role in distance-based algorithms.
- Logistic Regression performs exceptionally well on this dataset with minimal complexity.

---

##  Limitations
- KNN does not scale well to very large datasets.
- Logistic Regression assumes linear decision boundaries.
- Model performance is evaluated on a single dataset; external validation is recommended.

---

## Future Improvements
- Apply dimensionality reduction (PCA)
- Experiment with ensemble models (Random Forest, XGBoost)
- Perform cross-dataset validation
- Deploy as a web application for real-time predictions

---

## Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📁 Project Structure

# 🏦 Loan Prediction Project

Welcome to the **Loan Prediction Project**! This project is a comprehensive Data Mining pipeline designed to predict whether a customer will get their loan approved based on their application details. The project is split into two main phases: Data Preprocessing and Modelling & Predictions.

## 📁 Repository Structure

```text
├── Datasets/
│   ├── Train data.csv        # Historical dataset used for training and testing
│   └── New Customer.csv      # Unseen data to make final loan predictions
├── phase1_preprocessing.ipynb # Jupyter notebook for Phase 1 (Preprocessing)
├── phase2_modelling.ipynb     # Jupyter notebook for Phase 2 (Modelling)
└── README.md                 # This file
```

## 🛠️ Phases Overview

### Phase 1: Data Preprocessing (`phase1_preprocessing.ipynb`)
In this phase, the raw loan records from `Train data.csv` are explored and refined to prepare them for machine learning models. The pipeline includes:
- **Exploratory Data Analysis (EDA):** Visualizing distributions and relationships between features.
- **Missing Value Handling:** Imputing missing data appropriately.
- **Feature Engineering:** Creating new meaningful features to help the models learn better patterns.
- **Categorical Encoding:** Converting non-numeric categories into machine-readable numeric formats (using `LabelEncoder` and `OneHotEncoder`).
- **Feature Scaling:** Standardizing features using `StandardScaler` to ensure all features contribute equally to the models.

*Output:* A clean, preprocessed dataset ready for modeling.

### Phase 2: Modelling & Predictions (`phase2_modelling.ipynb`)
This phase focuses on training various classification algorithms on the preprocessed data and handling class imbalances. The pipeline covers:
- **Data Loading:** Splitting the preprocessed data into training and testing sets.
- **Class Imbalance Handling:** Using techniques like SMOTE, ADASYN, and SMOTETomek to balance the "Approved" vs "Rejected" classes.
- **Model Training & Evaluation:** Training multiple classifiers, including:
  - Decision Trees
  - K-Nearest Neighbors (KNN)
  - Naive Bayes (Gaussian, Multinomial, Bernoulli)
  - XGBoost
- **Performance Comparison:** Evaluating models using metrics like Accuracy, Classification Report, Confusion Matrix, and ROC-AUC.
- **Final Predictions:** Using the best-performing model to predict loan approvals for the `New Customer.csv` dataset.

## 🚀 Getting Started

### Prerequisites
To run the notebooks successfully, you will need **Python 3.x** and the following libraries installed:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `imbalanced-learn` (`imblearn`)
- `xgboost`
- `joblib`

You can install all required dependencies by running:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost joblib
```

### Usage
1. Open the workspace in your preferred Jupyter Notebook environment or VS Code.
2. Run **`phase1_preprocessing.ipynb`** top-to-bottom to generate the preprocessed dataset.
3. Run **`phase2_modelling.ipynb`** top-to-bottom to train the models, review evaluation metrics, and make predictions on the new customer dataset.

## 📝 Conclusion
This project showcases an end-to-end data mining workflow, highlighting the importance of thorough data cleaning, handling imbalanced datasets, and comparing multiple machine learning models to solve a real-world financial problem.

# 🚀 Spaceship Titanic: Binary Classification

This project is my solution for the [Kaggle Spaceship Titanic competition](https://www.kaggle.com/c/spaceship-titanic). The goal is to predict which passengers were transported to an alternate dimension during the Spaceship Titanic's collision with a spacetime anomaly, using personal records. This is a binary classification problem.

## 📈 Achievements
* **Current Best Score (Accuracy on Kaggle):** 0.79822 (~79.8%)
* **Key Improvements:** 
    * Successfully resolved severe overfitting, reducing the gap between training and validation accuracy from ~20% to ~5%.
    * Balanced the model to have a minimal bias towards either class (analyzed via Confusion Matrix).

## 📊 Core Metrics (Local Validation)
* **Training Accuracy:** 84.53%
* **Testing Accuracy:** 79.18%
* **Confusion Matrix Insights (v2 Model):**
    * Correct Predictions: 1373 (696 Stayed, 677 Transported)
    * Incorrect Predictions: 366 (201 False Negatives, 165 False Positives)

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib
* **Environment:** Jupyter Notebook

## 📈 Methodology & Features

### 1. Data Preprocessing & EDA
* **Handling Missing Values:** Strategy depended on the feature type (e.g., zero-filling for monetary spending columns).
* **Exploratory Data Analysis (EDA):** Performed extensive analysis to understand correlations, leading to crucial feature engineering steps.

### 2. Feature Engineering
* **Feature Extraction (Cabin):** Decoded the `Cabin` feature into `Deck`, `Room_No`, and `Side` (Port/Starboard) to capture spatial location impact.
* **Feature Extraction (Group):** Extracted group information from `PassengerId` to understand social dynamics during evacuation.
* **Categorical Encoding:** Utilized `OneHotEncoder` and `pd.get_dummies` to prepare categorical features for machine learning.

### 3. Machine Learning Models
* **Random Forest Classifier (v1 - Base):** Initial model which suffered from severe overfitting (99% Train Acc).
* **Random Forest Classifier (v2 - Regularized):** This is the current best model. Optimized using regularization techniques such as restricting `max_depth` to 10 and setting `min_samples_leaf` to 5, resulting in excellent generalization.

## 📂 Project Structure
```text
├── data/                   # Dataset files (train.csv, test.csv)
├── notebooks/              # Jupyter Notebooks with step-by-step analysis & model building
├── output/                 # Generated prediction files (submission.csv)
└── README.md               # Project documentation
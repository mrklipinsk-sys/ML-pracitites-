# Digit Classification (MNIST) using Machine Learning

This project demonstrates the complete process of building a classifier to recognize handwritten digits (0-9) using two fundamental machine learning algorithms: **Decision Trees** and **Random Forests**. The implementation is based on the popular MNIST dataset (Kaggle version).

## 🚀 Key Achievements

*   Implemented image data cleaning and normalization.
*   Optimized a single Decision Tree, increasing accuracy from an initial ~68% to **85.4%**.
*   Deployed a **Random Forest** model, drastically improving performance to **96.36%** accuracy on the test set.
*   Conducted a detailed error analysis using Confusion Matrices.

## 📊 Dataset and Preprocessing

The dataset (from a CSV file) contains grayscale images (28x28 pixels) flattened into 784 columns (features).
1.  **Analysis:** Checked for missing values (none detected).
2.  **Splitting:** The Kaggle dataset (42,000 rows) was separated into features (`X`) and labels (`y`).
3.  **Normalization:** Pixel values (0-255) were scaled to the **[0, 1]** range by dividing by 255.0 to stabilize the training process.
4.  **Train/Test Split:** The data was split into training (80%) and test (20%) sets using a fixed seed (`random_state=42`) for reproducibility.

## 🛠 Models and Methodology

### 1. Single Decision Tree (DecisionTreeClassifier)
A baseline model was trained in the first step.
*   **Initial Result (max_depth=5):** ~68% (underfitting).
*   **Optimization:** Increasing `max_depth` to **20** raised the test accuracy to **85.4%** (Train: 90.9%).
*   **Insights:** The model captured general shapes well but struggled with details, often confusing digits with similar features (e.g., `4` with `9`, `3` with `5`), as shown by the confusion matrix.

### 2. Random Forest (RandomForestClassifier)
An ensemble algorithm was used to address the limitations of the single tree.
*   **Configuration:** Built a forest consisting of **100 trees** (`n_estimators=100`).
*   **Result:** Drastic improvement in accuracy to **96.36%** on the test set (Train: 100%).
*   **Advantage:** Thanks to the "majority voting" of the army of trees, the model became significantly more robust against specific differences in handwriting styles, eliminating most of the baseline model's critical errors.

## 📈 Results Analysis

Below is a comparison of the accuracy of both models on the test set:

| Model | Accuracy (Test Set) |
| :--- | :--- |
| Single Decision Tree (depth=20) | **85.40%** |
| **Random Forest (100 trees)** | **96.36%** ✅ |

## 📦 Libraries Used

*   Pandas (data manipulation)
*   Numpy (numerical computation)
*   Matplotlib / Seaborn (data visualization, confusion matrices)
*   Scikit-Learn (ML model implementation, metrics, preprocessing)
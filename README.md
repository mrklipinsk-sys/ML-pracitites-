🤖 ML-practices

A collection of machine learning projects focused on data preprocessing, exploratory data analysis (EDA), and predictive modeling. This repository serves as a journey from basic classification and computer vision to advanced regression and time series forecasting techniques.

📁 Projects

🏠 House Prices: Advanced Regression

Goal: Predict sales prices for residential homes in Ames, Iowa.

Key Techniques: Handling 79 explanatory variables, advanced feature engineering (e.g., TotalSF, HouseAge), log1p target transformation, and model stacking (planned).

Models: RandomForestRegressor, XGBRegressor (optimized).

Status: Done

    Current Best Score (RMSLE): 0.13866

    Key Improvements: Achieved a Mean Absolute Error (MAE) of ~$16,267 USD during local validation.

🚀 Spaceship Titanic: Classification

Goal: Predict which passengers were transported to an alternate dimension during a space collision.

Key Techniques:

    Advanced Data Preprocessing: Strategy depended on the feature type (e.g., zero-filling for monetary spending columns). Successfully synchronized train/test column differences using .reindex().

    Feature Engineering: Splitting complex strings into meaningful features: Cabin into Deck, Room_No, and Side; PassengerId into Group.

    Regularization & Overfitting Fix: Drastically reduced the gap between training and validation accuracy from ~20% to ~5% by optimizing model depth.

Models: RandomForestClassifier (Regularized). XGBoost (Planned).

Status: Done (Kaggle Submitted)

    Current Best Score (Accuracy): 0.79822 (~79.8%)

    Evaluation Insights (Local): Training Accuracy (84.53%), Testing Accuracy (79.18%). Confusion Matrix shows a balanced model with minimal bias.

📈 Store Sales: Time Series Forecasting

Goal: Predict daily grocery and retail sales for thousands of product families across store locations in Ecuador.

Key Techniques:

    Advanced Time Series Feature Engineering: Weekly-aligned cyclic lags (`lag_16`, `lag_21`, `lag_28`), rolling window statistics (7, 14, 30 days), and promotional activity aggregations.

    Target Encoding: Capturing store-category-day dynamics via mean sales aggregations per `(store_nbr, family, DayofWeek)` over recent windows.

    Data Cleaning & Noise Reduction: Filtered non-stationary historical noise by trimming training data prior to 2016.

    Domain-Specific Preprocessing & Post-Processing: Merged economic indicators (oil prices with ffill/bfill); enforced strict zero-sales predictions for historically inactive product-store pairs.

Models: LightGBM, XGBoost (Ensemble Blending).

Status: Done (Kaggle Submitted)

    Current Best Score (RMSLE): 0.42506

    Key Improvements: Improved RMSLE from initial baseline (~0.4670) down to 0.42506 by resolving calendar alignment issues, incorporating store metadata, and ensembling model predictions.

🔢 Digit Recognizer (MNIST): Computer Vision & Classification

Goal: Recognize handwritten digits (0–9) from 28x28 grayscale images flattened into 784 pixel features.

Key Techniques:

    Data Normalization: Scaled pixel values from [0, 255] to [0, 1] range to ensure stable and faster model convergence.

    Hyperparameter Optimization: Tuned single Decision Tree depth (`max_depth=20`) to prevent heavy underfitting.

    Error Analysis: Applied Confusion Matrices to analyze misclassifications between visually similar digits (e.g., 4 vs 9, 3 vs 5).

Models: DecisionTreeClassifier, RandomForestClassifier (100 trees).

Status: Done (Kaggle Submitted)

    Current Best Score (Accuracy): 0.96360 (~96.36%)

    Key Improvements: Boosted accuracy from initial baseline of ~68% (underfitted tree) to 85.4% via depth optimization, and ultimately reached 96.36% by deploying a Random Forest ensemble.

🛠️ Tech Stack

Language: Python

Libraries: Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn

Environment: Jupyter Notebooks / Google Colab

⚙️ Core Workflow Applied

Each project in this repository follows a standardized ML pipeline:

    Exploratory Data Analysis (EDA): Visualizing data to understand relationships and patterns.

    Feature Engineering: Creating new variables from raw data to improve model performance.

    Preprocessing: Handling missing values, encoding categorical data, and feature scaling.

    Model Selection & Training: Evaluating and fitting various machine learning models.

    Hyperparameter Tuning: Optimizing model settings for better generalization.

    Evaluation: Using relevant metrics (e.g., Accuracy, Confusion Matrix, RMSLE, MAE) to assess performance.
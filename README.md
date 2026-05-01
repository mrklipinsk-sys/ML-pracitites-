🤖 ML-practices

A collection of machine learning projects focused on data preprocessing, exploratory data analysis (EDA), and predictive modeling. This repository serves as a journey from basic classification to advanced regression techniques.

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

🛠️ Tech Stack

Language: Python

Libraries: Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn

Environment: Jupyter Notebooks / Google Colab

⚙️ Core Workflow Applied

Each project in this repository follows a standardized ML pipeline:

    Exploratory Data Analysis (EDA): Visualizing data to understand relationships and patterns.

    Feature Engineering: Creating new variables from raw data to improve model performance.

    Preprocessing: Handling missing values, encoding categorical data, and feature scaling.

    Model Selection & Training: Evaluating and fitting various machine learning models.

    Hyperparameter Tuning: Optimizing model settings for better generalization.

    Evaluation: Using relevant metrics (e.g., Accuracy, Confusion Matrix, RMSLE, MAE) to assess performance.
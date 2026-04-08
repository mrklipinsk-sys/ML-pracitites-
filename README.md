🤖 ML-practices

A collection of machine learning projects focused on data preprocessing, exploratory data analysis (EDA), and predictive modeling. This repository serves as a journey from basic classification to advanced regression techniques.
📁 Projects

🏠 House Prices: Advanced Regression

    Goal: Predict sales prices for residential homes in Ames, Iowa.

    Key Techniques: Handling 79 explanatory variables, advanced feature engineering, and handling skewed data.

    Models: RandomForestRegressor, Gradient Boosting (planned).

    Status: Done
        
        Current Best Score (RMSLE): 0.13866
        
        Key Improvements: Achieved a Mean Absolute Error (MAE) of ~$16,267 USD during local validation.

🚀 Spaceship Titanic: Classification (In Progress)

Goal: Predict which passengers were transported to an alternate dimension during a space collision.

Key Techniques: * Domain-Specific Imputation: Using passenger groups to infer home planets and luxury spending patterns to determine CryoSleep status.

    Feature Engineering: Splitting complex strings (Cabin, PassengerId) into meaningful features like Deck, Side, and Group.

Status: In Progress (Data Preprocessing Stage)

🛠️ Tech Stack

    Language: Python

    Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

    Environment: Jupyter Notebooks / Google Colab

⚙️ Core Workflow Applied

Each project in this repository follows a standardized ML pipeline:

    Data Loading: Importing datasets via Pandas.

    Feature Selection: Identifying relevant variables for the model.

    Missing Value Imputation: Using SimpleImputer for numerical and categorical gaps.

    Categorical Encoding: Transforming text into numbers via OneHotEncoder.

    Model Training: Splitting data into train/test sets and fitting the models.

    Evaluation: Analyzing performance through metrics like Accuracy (for classification) or RMSE (for regression).
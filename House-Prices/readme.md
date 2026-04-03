# House Prices: Advanced Regression Techniques

This project is my solution for the popular [Kaggle House Prices competition](https://www.kaggle.com/c/house-prices-advanced-regression-techniques). The goal is to predict the sales price of residential homes in Ames, Iowa, using 79 explanatory variables.

## 🚀 Achievements
* **Current Best Score (RMSLE):** 0.13866
* **Key Improvements:** Achieved a Mean Absolute Error (MAE) of ~$16,267 USD during local validation.

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, Seaborn, Matplotlib
* **Environment:** Jupyter Notebook 

## 📈 Methodology & Features

### 1. Data Preprocessing
* **Handling Missing Values:** Used `SimpleImputer` with `median` strategy for numerical data and `most_frequent` for categorical data.
* **Categorical Encoding:** Applied `OneHotEncoder` to transform text features into a machine-readable format.
* **Target Transformation:** Applied `log1p` transformation to the `SalePrice` to handle skewness and improve model stability.

### 2. Feature Engineering
* **TotalSF:** Created a combined feature of `1stFlrSF` + `2ndFlrSF` + `TotalBsmtSF` to capture the total living area.
* **HouseAge:** Calculated the age of the house at the time of sale (`YrSold` - `YearBuilt`).

### 3. Machine Learning Models
* **Random Forest Regressor:** Used as a robust baseline.
* **XGBoost Regressor:** Optimized with a learning rate of 0.05 and 1000 estimators, providing the best performance so far.

## 📂 Project Structure
```text
├── data/                   # Dataset files (train.csv, test.csv)
├── notebooks/              # Jupyter Notebooks with step-by-step analysis
├── output/                 # Submission files for Kaggle
└── README.md               # Project documentation


How to Run

    Clone this repository.

    Install dependencies: pip install -r requirements.txt.

    Open notebooks/House_Prices_Regression.ipynb and run all cells.

🔮 Future Work

    Implement outlier detection (e.g., removing houses with GrLivArea > 4000).

    Perform hyperparameter tuning using GridSearchCV.

    Explore model ensembling (stacking XGBoost and Random Forest).
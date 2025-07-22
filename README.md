# 🏠 House Price Prediction using Machine Learning

This project focuses on predicting house sale prices using advanced regression techniques and real-world housing data. It was completed as part of a machine learning practice initiative, and is now being showcased for my ML coordinator application.

## 📌 Problem Statement

The goal is to predict the final price of each home in the test dataset. The dataset includes 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa.

This is based on the **"House Prices: Advanced Regression Techniques"** Kaggle competition:  
https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/

## 🚀 Approach

The steps taken in the notebook include:

1. **Data Loading**  
   Reading the train and test datasets into Pandas DataFrames.

2. **Data Combination**  
   Merging the datasets for uniform preprocessing.

3. **Missing Value Treatment**  
   Imputing null values using domain knowledge and statistical techniques.

4. **Encoding Categorical Variables**  
   Using `pd.get_dummies()` for one-hot encoding of categorical features.

5. **Feature Transformation**  
   - Log transformation on skewed features  
   - Power transformation and robust scaling

6. **Model Selection**  
   Multiple regression models were experimented with, including:
   - Ridge Regression  
   - Lasso Regression  
   - XGBoost Regressor  
   - LightGBM Regressor

7. **Evaluation**  
   - Performance evaluated using RMSE (Root Mean Squared Error)  
   - Cross-validation for model robustness

8. **Prediction and Submission**  
   Final model predictions were saved and formatted for Kaggle submission.

## 🛠️ Technologies Used

- Python 3
- NumPy, Pandas
- Scikit-learn
- Matplotlib, Seaborn
- XGBoost
- LightGBM
- Kaggle Notebooks

## 📊 Sample Output

- Achieved competitive RMSE on local validation
- Final predictions successfully submitted on Kaggle

## 📌 Highlights

- Cleaned and engineered features from 70+ columns
- Built and compared multiple ensemble models
- Final result selected from the top 3 models

## 🧩 Challenges Faced & Solutions

1. **🔍 Missing & Incomplete Data**  
   - *Challenge:* Many features had missing values, including numerical and categorical ones like `LotFrontage`, `GarageType`, `Alley`, etc.  
   - *Solution:* I used contextual imputation — for example, filled `LotFrontage` using the median grouped by `Neighborhood`, and categorical nulls with `"None"` where it made sense.

2. **📉 Skewed Distributions**  
   - *Challenge:* Several numerical features (like `GrLivArea`, `TotalBsmtSF`) were highly skewed, affecting model performance.  
   - *Solution:* Applied log and power transformations (using `PowerTransformer`), which helped normalize distributions and reduce RMSE.

3. **📦 Feature Inconsistency Between Train/Test**  
   - *Challenge:* One-hot encoding created mismatched columns between train and test datasets.  
   - *Solution:* Merged the train and test datasets before encoding to ensure consistent feature space.

4. **⚖️ Outliers Impacting Model**  
   - *Challenge:* Extreme values in `SalePrice` and `GrLivArea` were distorting the model.  
   - *Solution:* Identified and removed outliers using domain knowledge and scatter plots to improve generalization.

5. **🔁 Model Selection Confusion**  
   - *Challenge:* It was hard to decide which model to trust — Ridge, Lasso, XGBoost, or LightGBM.  
   - *Solution:* Compared all using cross-validation RMSE and combined the top 3 for final prediction to improve robustness.

## 🧠 What I Learned

- Practical data preprocessing strategies
- Handling real-world messy data
- Model stacking and ensemble learning
- Using Kaggle environment for experiments

## 👤 Author

**K Madhava Reddy**  
Aspiring ML Engineer | Data Enthusiast  
[GitHub](https://github.com/MADHAVAREDDY-2005) • [Kaggle](https://www.kaggle.com/code/madhavareddy09/top-3-in-house-prediction/notebook)

---

📌 *This project demonstrates strong data preprocessing, model experimentation, and results presentation skills.*


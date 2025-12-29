# Medical Cost Prediction Project

This project aims to predict medical insurance costs based on various factors such as age, sex, BMI, children, smoking habits, and region.
The notebook explores the dataset through detailed explortory data analysis (EDA), feature engineering, and build machine learning models 
using optimized hyperparameter to accurately predict medical costs. The final model is selected based on performance metrics,
and the feature importance is examined using SHAP values.

## 📊 About the Dataset
The dataset used in this project contains medical insuracne cost data for individuals. It included the following features:

- **age**: Age of the individual
- **sex**: Gender of the individual
- **bmi**: Body Mass Index (BMI), a measure of body fat based on height and weight.
- **children**: Number of cylinder/dependents covered by the insurance plan.
- **smoker**: where the individual is a smoker or not.
- **region**: The individual's residential region in the Unites States.
- **charges**: The medical insurance cost charged to the individual (target variable). This dataset allows us to explore how various factors
  like age, BMI,smoking habits, and region contribute to medical insurance costs. It is particularly useful for regression tasks, as we aim
  to predict the charges based on the other features.

### 📄 Project Contents
**1. EDA (Exploratory Data Analysis)**
- A thorough examination of the dataset for understanding key insights and identifying patterns.

**2. Data Visualization:** Visualization of both univariate and bivariate relationships.
- Univariate Analysis
    - Categorical and numerical features.
- Bi-variate Analysis
    - Categorical vs. target
    - Numerical vs. target

**3. Feature Engineering**
- Handling missing values
- Outlier detection and treatment
- Extracting new features to enhance predictive performance.
- Encode categorical features and scaling numerical ones.

**4. Model Building**
- Optuna Hyperparameter Optimzation applied to key models such as LGBM, XGBoost, and CatBoost.
- Training various algorithms, inclusing GradientBoosting, RandomForest, DecisionTree, LinearRegression, and more.

**5. Model Evaluation**
- Models were evaluated using varioys metrics, such as:
  - Mean Square Error (MSE) and Root Mean Squared Error (RMSE) on both train and test sets.
  - R2 score to check how well the model fits the data.
  - Cross-validation to assess model stability. The evaluatuion revealed strong performance across all models, with the final models
    producing low error rates and high R2 scores.

**6. Model Performance Visualization**
-  A visual comparison of model performances using train and test mse, rmse, AND r2 scores was conducted. This helped in understanding
how well each model generalizes to unseen data.

**7. Final Model Selection**
- The **GradientBoostingRegressor** was selected as the final model due to its superior performance on test data. This model
provided the best trade-off between accuracy and interpretability, ensuring robust and explainable predictions.

**8. Final Model: SHAP Feature Importance**
- **Feature Importance using SHAP:** THE SHAP values were used to interpret the final model's predictions and to rank feature
importance, identifying the ket drivers behind medical cost predictions.
- **Save Final Model:** The final optimized model was saved for future use.

# 🔍 Key Insights
- The **GradientBoostingRegressor** performed the best among all models in terms of predictive accuracy, with the lowest RMSE and
highest R2 score.
- Features such as **smoking status, BMI, and age** significantly impacted medical cost predictions, as revealed by SHAP values.
- Optuna's hyperparameter optimization improved model performance for LGBM, XGBoost, and CatBoost, though
GradientBoostingRegressor was ultimately more stable.

# 📌 Summary
This project delves into predicting medical costs using various machine learning algorithms, with an emphasis on feature engineering and
model optimization. Several models were trained and evaluated, including GradientBoosting, RandomForest, and LinearRegression, with
GradientBoostingRegressor emerging as the best performer. Hyperparameter tuninng via Optuna imporved key models, and SHAP analysis
provided insights into feature importance, confirming that factors like smoking status, BMI, and age have significant predictive power. The
final model was saved for deployment, showcasing a complete workflow from exploratory data analysis to final model selection and evaluation.


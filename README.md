# rossmann-python-ml
Final project for Python for AI course at Iron Hack

Link to presentation:
https://docs.google.com/presentation/d/12dsWYqd2VBMzhT35Ltthgrm9O_onxduQ85vrVvw8QZM/edit?usp=sharing

### Read-Me: Model Evaluation and Hyperparameter Tuning for Store Sales Prediction

#### Introduction
This project focuses on exploratory data analysis and evaluating various regression models to predict store sales and optimizing model performance through hyperparameter tuning. We use a sample dataset that includes features such as store type, assortment, competition distance, promotional activities, and more. The target variable is the store sales.

#### Dataset
The dataset includes the following columns:
- **Store**: Unique identifier for each store
- **StoreType**: Type of store
- **Assortment**: Assortment type
- **CompetitionDistance**: Distance to the nearest competitor
- **CompetitionOpenSinceMonth**: Month when the nearest competitor opened
- **CompetitionOpenSinceYear**: Year when the nearest competitor opened
- **Promo2**: Indicates whether the store is participating in a continuous promotion
- **Promo2SinceWeek**: Week since the store started participating in Promo2
- **Promo2SinceYear**: Year since the store started participating in Promo2
- **PromoInterval**: Interval of Promo2
- **DayOfWeek**: Day of the week
- **Sales**: Store sales (target variable)
- **Customers**: Number of customers
- **Open**: Indicates whether the store was open
- **Promo**: Indicates whether a store is running a promotion
- **StateHoliday**: Indicates a state holiday
- **SchoolHoliday**: Indicates a school holiday
- **Year**: Year of the data point
- **Month**: Month of the data point

#### Objective
The objective is to compare different regression models and tune hyperparameters to improve the model's R² score, which measures the proportion of variance in the target variable that is predictable from the independent variables.

#### Models Evaluated
1. **Linear Regression**: A basic regression model with no hyperparameters to adjust.
2. **Random Forest Regressor**: An ensemble learning method that uses multiple decision trees.
3. **Gradient Boosting Regressor**: An ensemble technique that builds trees sequentially to reduce errors.
4. **Support Vector Regressor (SVR)**: Uses support vector machines for regression tasks.

#### Evaluation Metrics
- **Mean Squared Error (MSE)**: Measures the average squared difference between actual and predicted values.
- **Root Mean Squared Error (RMSE)**: The square root of MSE, providing error in the same units as the target variable.
- **Mean Absolute Error (MAE)**: Measures the average magnitude of errors without considering their direction.
- **R-squared (R²)**: Indicates the proportion of variance in the target variable that is predictable from the independent variables.
- **Time (s)**: Time taken to train the model and make predictions.

#### Hyperparameter Tuning
We use `GridSearchCV` to perform hyperparameter tuning for the `RandomForestRegressor` and XGBoost to find the best combination of parameters:
- **n_estimators**: Number of trees in the forest
- **max_depth**: Maximum depth of the trees
- **min_samples_split**: Minimum number of samples required to split an internal node
- **min_samples_leaf**: Minimum number of samples required to be at a leaf node

#### Script Overview
The script performs the following steps:
1. Import necessary libraries.
2. Load and preprocess the dataset.
3. Split the dataset into training and testing sets.
4. Define and evaluate each model, printing results as each model finishes.
5. Perform hyperparameter tuning using `GridSearchCV` for the `RandomForestRegressor`.
6. Evaluate the best model from the grid search.
7. Print and compare the results of all models.

#### Usage
To run the script, ensure you have the necessary libraries installed:
pandas, numpy, scikit-learn, tensorflow and all regressors


Then, execute the script in your Python environment. The script will print the results for each model as it finishes and display a summary of all results at the end.

### Conclusion
This project demonstrates how to evaluate multiple regression models and improve their performance through hyperparameter tuning, providing a comprehensive approach to model selection and optimization for store sales prediction.

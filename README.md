
# Bike Sharing Demand Prediction

This project involves building a regression model to predict bike sharing demand using the Bike Sharing Demand dataset. The project covers various steps in a typical machine learning workflow, including data cleaning, exploratory data analysis (EDA), feature engineering, model building, and hyperparameter tuning.

## Project Steps

1. **Data Loading and Preparation**: The dataset is loaded from an online source, and relevant features and target variables are selected for the analysis.
2. **Exploratory Data Analysis (EDA)**: Various visualizations and statistical analyses are performed to understand the data better:
   - **Correlation Matrix**: A heatmap to show correlations between features and the target variable.
   - **Target Distribution**: Histogram with KDE to visualize the distribution of the target variable (`cnt`).
   - **Scatter Plots**: Pairwise scatter plots to show relationships between features and the target variable.
3. **Data Preprocessing**:
   - **Numeric Features**: Missing values are imputed with the mean, and the features are scaled using `StandardScaler`.
   - **Categorical Features**: Missing values are imputed with the most frequent value, and the features are one-hot encoded.
4. **Pipeline Creation**: A pipeline is created using `ColumnTransformer` for preprocessing steps and `RandomForestRegressor` for the regression model.
5. **Model Training and Evaluation**:
   - The pipeline is fitted on the training data and evaluated on the test data.
   - Initial performance metrics: Mean Squared Error (MSE) and R-squared (R2) Score.
6. **Hyperparameter Tuning**:
   - **RandomizedSearchCV**: Initial hyperparameter tuning to narrow down the search space.
   - **GridSearchCV**: Further tuning using the best parameters from `RandomizedSearchCV` for finer adjustments.
   - Performance metrics after tuning are compared with the initial model.
7. **Model Persist
   - Saved the trained model using joblib for easy reuse without retraining, ensuring efficiency in deployment and scalability.


Insights and Predicted Results
Project Insights:

1- Data Exploration and Visualization:
   - Correlation Analysis: The heatmap showed strong correlations between some features like temp, atemp, and the target variable cnt, indicating their significance in predicting bike sharing demand.
   - Target Distribution: The target variable cnt (bike sharing count) has a right-skewed distribution, suggesting the need for potential transformation for better model performance.
   - Pairwise Scatter Plots: Visualized relationships between features and target, highlighting trends and potential non-linear relationships.

2- Preprocessing and Feature Engineering:
   - Numeric Features: Handled missing values using mean imputation and scaled using StandardScaler for normalization.
   - Categorical Features: Imputed missing values using the most frequent value and applied one-hot encoding for categorical variables.

3- Model Building and Evaluation:
   - Initial Model: Used a RandomForestRegressor within a pipeline. Achieved initial evaluation metrics:
      - Mean Squared Error (MSE): 1646.50
      - R-squared (R2) Score: 0.8945
   - Hyperparameter Tuning: Improved model performance using RandomizedSearchCV and GridSearchCV.
   - Best parameters from tuning improved the model.

4- Model Persistence:
   - Saved the trained model using joblib for easy reuse without retraining, ensuring efficiency in deployment and scalability.


** These results indicate that the tuned RandomForestRegressor model accurately predicts bike sharing demand, with a high R-squared value close to 0.90, suggesting a strong fit with the 
  data. The relatively low MSE further confirms the model's accuracy in predicting bike rental counts.**

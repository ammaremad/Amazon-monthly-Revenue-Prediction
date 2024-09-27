# Project Summary: Amazon Monthly Revenue Prediction

The project focuses on predicting Amazon's monthly revenue using a dataset containing 23,084 entries and 35 columns. The primary objective is to develop a machine learning model that accurately estimates monthly revenue based on various product features.

#### 1. **Data Understanding and Preparation**
- **Data Import**: The dataset was loaded using Pandas, and the structure was examined using `info()` and `head()` functions.
- **Target Label**: The target variable identified is `monthly_Revenue_Estimate`.
- **Data Cleaning**: Missing values were addressed by filling or dropping columns with high percentages of nulls. The `imageUrl` column was dropped as it did not contribute to the target variable. Categorical variables were converted to a categorical data type for better handling, and label encoding was applied to retain original text for visualization.

#### 2. **Exploratory Data Analysis (EDA)**
- **Statistical Overview**: Descriptive statistics were generated using the `describe()` function to understand the data distribution.
- **Correlation Analysis**: A correlation matrix was computed to evaluate relationships between features and the target variable. Features with weak or negative correlations were identified for potential removal.
- **Outlier Detection**: Boxplots were used to visualize outliers, which were handled using the interquartile range (IQR) method to replace extreme values with calculated fences.

#### 3. **Data Visualization**
- Various visualizations were created, including histograms, boxplots, scatter plots, and heatmaps, to identify patterns and trends in the data. A logarithmic transformation was applied to the `monthly_Revenue_Estimate` to improve its distribution.

#### 4. **Feature Engineering**
- Features were scaled using MinMaxScaler, and boolean columns (`is_Variation` and `out_Of_Stock_Now`) were converted to integers for better handling.

#### 5. **Modeling**
- The dataset was split into training and testing sets. Several regression models were evaluated:
  - **Linear Regression**: Achieved an R-squared value of 0.42, indicating low accuracy.
  - **XGBoost Regression**: Achieved an R-squared value of 0.98, demonstrating high accuracy.
  - **Random Forest Regression**: Achieved the highest accuracy with an R-squared value of 0.99.
  - **Decision Tree Regression**: Also performed well with an R-squared value of 0.98.

#### 6. **Model Evaluation**
- Each model's performance was assessed using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared values. The Random Forest model was selected as the best option for predicting monthly revenue due to its superior performance.

#### 7. **Conclusion**
- The project successfully developed a predictive model for Amazon's monthly revenue, with Random Forest Regression being the most effective. The analysis highlighted the importance of data cleaning, feature engineering, and model selection in achieving accurate predictions.

This comprehensive approach ensures that the model is robust and reliable for estimating monthly revenue, providing valuable insights for stakeholders.

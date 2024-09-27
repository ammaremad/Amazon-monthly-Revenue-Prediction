# Amazon Monthly Revenue Prediction

## Overview
This project aims to predict the monthly revenue of products listed on Amazon using a dataset containing various product features. The analysis employs several machine learning models to identify the most accurate method for revenue estimation.

## Table of Contents
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Data Understanding](#data-understanding)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Results](#results)
- [Conclusion](#conclusion)

## Dataset
The dataset consists of 23,084 entries and 35 columns, including features such as:
- `brandId`: Unique identifier for products
- `subcategoryId`: Unique identifier for each subcategory
- `monthlyRevenueEstimate`: Target variable for revenue prediction
- `monthlyUnitsSold`: Number of units sold per month
- `reviewCount`: Total number of reviews a product has received

## Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn
- XGBoost
- Imbalanced-learn

## Data Understanding
The data was imported and examined for its structure and types. The target label for prediction was identified as `monthlyRevenueEstimate`. The dataset contained various features related to product performance, sales, and reviews.

## Data Cleaning
Missing values were handled by:
- Dropping columns with a high percentage of nulls.
- Filling missing values in columns with a small percentage of nulls using appropriate methods (mean, mode).
- Converting categorical variables to a categorical data type for better handling.

## Exploratory Data Analysis (EDA)
EDA was conducted to visualize data distributions and relationships:
- Histograms and boxplots were used to identify distributions and outliers.
- A correlation matrix was created to evaluate relationships between features and the target variable.

## Feature Engineering
- Features were scaled using MinMaxScaler.
- Boolean columns (`isVariation` and `outOfStockNow`) were converted to integers for better handling.
- Label encoding was applied to categorical variables to retain original text for visualization.

## Modeling
The dataset was split into training and testing sets. Various regression models were evaluated:
1. **Linear Regression**: Achieved an R-squared value of 0.42.
2. **XGBoost Regression**: Achieved an R-squared value of 0.98.
3. **Random Forest Regression**: Achieved the highest accuracy with an R-squared value of 0.99.
4. **Decision Tree Regression**: Achieved an R-squared value of 0.98.

## Results
The Random Forest model was selected as the best option for predicting monthly revenue due to its superior performance. The model comparison showed:
- Random Forest Regression: 99% accuracy
- XGBoost Regression: 98% accuracy
- Linear Regression: 42% accuracy

## Conclusion
The project successfully developed a predictive model for Amazon's monthly revenue, with Random Forest Regression being the most effective. The analysis highlighted the importance of data cleaning, feature engineering, and model selection in achieving accurate predictions.

## How to Run the Project
1. Clone the repository.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Run the Jupyter Notebook `Amazon_Monthly_Revenue_Prediction.ipynb` to execute the analysis and modeling.


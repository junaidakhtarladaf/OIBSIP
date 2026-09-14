# House Price Prediction with Linear Regression

## Objective

Build a machine learning model to predict house prices using Linear Regression.

## Dataset

The Ames Housing dataset from the House Prices: Advanced Regression Techniques competition was used for this project.

The dataset contains residential property information and SalePrice as the target variable.

## Selected Features

- OverallQual
- GrLivArea
- GarageCars
- TotalBsmtSF
- YearBuilt
- Neighborhood

These features represent house quality, living area, garage capacity, basement area, property age, and location, which are likely to influence house prices.

## Workflow

1. Data loading and exploration
2. Missing value analysis
3. Descriptive statistics
4. SalePrice distribution analysis
5. Feature selection
6. Missing value handling
7. One-Hot Encoding
8. Correlation analysis
9. 80/20 train-test split
10. Linear Regression
11. Model evaluation
12. Actual vs Predicted analysis
13. Residual analysis
14. Coefficient analysis
15. Ridge Regression comparison

## Model Performance

### Linear Regression

- MSE: 1.329312 × 10⁹
- RMSE: 36,459.74
- R² Score: 0.8267

### Ridge Regression

- MSE: 1.559369 × 10⁹
- RMSE: 39,488.84
- R² Score: 0.7967

Linear Regression performed better than Ridge Regression on the selected test data.

## Key Findings

OverallQual showed the strongest correlation with SalePrice at 0.79, followed by GrLivArea at 0.71.

The actual vs predicted plot showed that most predictions were close to the diagonal line, while some higher-priced houses were underpredicted.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## Conclusion

The Linear Regression model performed well on the test data with an R² score of 0.8267 and an RMSE of 36,459.74. OverallQual and GrLivArea showed the strongest relationships with SalePrice.

The Actual vs Predicted plot showed that most predictions were close to the expected values, while some expensive houses were underpredicted. Ridge Regression was also tested, but Linear Regression achieved better performance on the selected test data.

## Project Structure

```text
DataAnalytics-L2-HousePricePrediction/
├── Data/
│   └── Raw/
│       └── train.csv
├── Notebook/
│   └── House_Price_Prediction.ipynb
├── Screenshots/
│   ├── SalePrice_Distribution.png
│   ├── Correlation_Heatmap.png
│   ├── Model_Evaluation.png
│   ├── Actual_vs_Predicted.png
│   ├── Residual_Plot.png
│   └── Ridge_Comparison.png
└── README.md
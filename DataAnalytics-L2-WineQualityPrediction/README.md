# Wine Quality Prediction

## Objective

The objective of this project is to train and compare multiple classification models to predict wine quality based on its physicochemical properties.

The project uses the Wine Quality dataset and compares Random Forest, Stochastic Gradient Descent (SGD), and Support Vector Classifier (SVC).

---

## Dataset

The project uses the Wine Quality Red Wine dataset.

Dataset source: UCI Machine Learning Repository

The dataset contains physicochemical measurements such as acidity, density, sulphates, alcohol, and other chemical properties along with wine quality scores.

For this project, the red wine dataset was used.

---

## Technologies Used

- Python
- pandas
- numpy
- scikit-learn
- seaborn
- matplotlib
- Jupyter Notebook

---

## Project Workflow

1. Load the Wine Quality dataset
2. Inspect the dataset structure
3. Check missing values and duplicate records
4. Analyze the distribution of wine quality scores
5. Perform exploratory data analysis
6. Analyze correlations between chemical features
7. Discuss class imbalance
8. Convert quality scores into Low, Medium, and High categories
9. Perform a stratified train-test split
10. Train Random Forest, SGD, and SVC classifiers
11. Evaluate model performance using accuracy and classification reports
12. Analyze confusion matrices
13. Analyze Random Forest feature importance
14. Compare all three models
15. Select the most suitable model for deployment

---

## Data Preparation

The dataset initially contained 1,599 records and 11 physicochemical features along with the quality score.

A total of 240 duplicate rows were identified and removed before modelling.

After removing duplicates, the dataset contained 1,359 records.

---

## Exploratory Data Analysis

### Quality Score Distribution

The quality scores are unevenly distributed. Quality scores 5 and 6 contain the majority of observations, while scores 3, 4, and 8 are underrepresented.

### Chemical Feature Distributions

Distribution plots were created for all physicochemical features to understand their spread and frequency.

### Correlation Analysis

A correlation heatmap was created to examine relationships between the chemical properties and wine quality.

Alcohol showed the strongest positive correlation with quality among the features, while volatile acidity showed a notable negative relationship.

---

## Class Imbalance

The quality scores are highly imbalanced, with Medium-quality wines representing the majority of observations.

This imbalance can cause classification models to favor the majority class and perform poorly on minority classes.

Therefore, macro F1-score was considered along with accuracy when comparing the models.

---

## Feature Engineering

The original quality scores were converted into three categories:

- Low: quality scores 3 and 4
- Medium: quality scores 5 and 6
- High: quality scores 7 and 8

A three-class approach was selected instead of binary classification because it preserves more information from the original quality scores. It distinguishes low-quality, medium-quality, and high-quality wines while simplifying the prediction problem into manageable categories.

---

## Train-Test Split

The dataset was divided into:

- 80% training data
- 20% testing data

Stratification was used to preserve the class proportions of Low, Medium, and High quality wines in both datasets.

Training samples: 1,087

Testing samples: 272

---

## Machine Learning Models

### 1. Random Forest

Random Forest was used as an ensemble classification algorithm capable of capturing nonlinear relationships between physicochemical properties and wine quality.

### 2. Stochastic Gradient Descent

SGD was used as a fast linear classification algorithm for comparison with the other models.

### 3. Support Vector Classifier

SVC was used to identify decision boundaries between the three wine quality categories.

---

## Model Performance

| Model | Accuracy | Macro F1-Score |
|---|---:|---:|
| Random Forest | 0.8199 | 0.5065 |
| SGD | 0.8162 | 0.2996 |
| SVC | 0.8162 | 0.2996 |

Random Forest achieved the highest accuracy and the highest macro F1-score among the three models.

---

## Random Forest Feature Importance

The most important features identified by the Random Forest model were:

| Chemical Feature | Importance |
|---|---:|
| Alcohol | 0.1517 |
| Volatile Acidity | 0.1174 |
| Sulphates | 0.1132 |
| Density | 0.0910 |
| Total Sulfur Dioxide | 0.0892 |
| Citric Acid | 0.0821 |
| Fixed Acidity | 0.0790 |
| Residual Sugar | 0.0765 |
| Chlorides | 0.0697 |
| pH | 0.0684 |
| Free Sulfur Dioxide | 0.0617 |

Alcohol was the most influential feature in the Random Forest model.

---

## Model Evaluation

Classification reports and confusion matrices were used to evaluate the performance of each classifier.

Random Forest was better at identifying the minority Low and High classes compared with SGD and SVC.

SGD and SVC achieved similar accuracy but showed difficulty identifying the minority classes.

---

## Conclusion

Random Forest is the most suitable model for deployment among the three tested classifiers.

It achieved an accuracy of 81.99% and the highest macro F1-score of 0.5065. It also performed better than SGD and SVC at identifying the minority quality classes.

However, class imbalance remains an important limitation. Further improvements such as class balancing, feature engineering, and hyperparameter tuning could improve minority-class performance before production deployment.

---

## Project Structure

```text
DataAnalytics-L2-WineQualityPrediction/
│
├── Data/
│   └── Raw/
│       ├── winequality-red.csv
│       └── winequality.names
│
├── Notebook/
│   └── Wine_Quality_Prediction.ipynb
│
├── Screenshots/
│   ├── 01_quality_distribution.png
│   ├── 02_chemical_features_distribution.png
│   ├── 03_correlation_heatmap.png
│   ├── 04_confusion_matrices.png
│   ├── 05_random_forest_feature_importance.png
│   └── 06_model_comparison.png
│
└── README.md
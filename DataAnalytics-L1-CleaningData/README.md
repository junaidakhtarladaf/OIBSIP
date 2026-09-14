# Data Cleaning - Dirty Cafe Sales Dataset

## Project Overview

This project focuses on cleaning and preparing a messy cafe sales dataset for further analysis. The dataset contains missing values, invalid placeholder values, inconsistent categorical formatting, incorrect data types, and potential outliers.

## Objectives

- Identify missing values and data quality issues
- Standardise invalid placeholder values
- Handle missing values using appropriate strategies
- Remove duplicate records
- Standardise categorical values
- Correct data types
- Detect value range anomalies
- Detect outliers using the IQR method
- Compare the dataset before and after cleaning
- Save the cleaned dataset as a new CSV file

## Dataset

The dataset used in this project is the Dirty Cafe Sales Dataset.

It contains 10,000 transaction records and 8 columns:

- Transaction ID
- Item
- Quantity
- Price Per Unit
- Total Spent
- Payment Method
- Location
- Transaction Date

## Data Cleaning Process

### 1. Data Quality Assessment

The dataset was inspected for missing values, data types, unique values, and potential data quality issues.

### 2. Standardising Invalid Values

Placeholder values such as `ERROR` and `UNKNOWN` were converted into missing values.

### 3. Handling Missing Values

- Numerical columns were handled using median imputation.
- Categorical columns were handled using mode imputation.
- Missing transaction dates were filled using the most frequent valid date.

### 4. Data Type Correction

- Transaction ID was kept as string.
- Quantity was converted to integer.
- Price Per Unit was converted to float.
- Total Spent was converted to float.
- Transaction Date was converted to datetime.

### 5. Categorical Standardisation

Categorical values were cleaned by removing unnecessary spaces and applying consistent capitalization.

### 6. Duplicate Removal

Duplicate rows were identified and removed.

### 7. Value Range Validation

Quantity, Price Per Unit, and Total Spent were checked for negative and zero values.

### 8. Outlier Detection

The IQR method was used to identify potential outliers. Potential outliers in Total Spent were retained because they may represent legitimate transactions.

## Before vs After Cleaning

| Metric | Before Cleaning | After Cleaning |
|---|---:|---:|
| Total Rows | 10,000 | 10,000 |
| Missing Values | 6,826 | 0 |
| Duplicate Rows | 0 | 0 |
| Data Type Accuracy | 4/8 | 8/8 |

## Tools Used

- Python
- Pandas
- NumPy
- Jupyter Notebook

## Conclusion

The dataset was successfully cleaned and transformed into a consistent format suitable for further analysis. Missing values, invalid placeholders, categorical inconsistencies, data type issues, duplicate records, range anomalies, and potential outliers were addressed using appropriate data cleaning techniques.

## Project Structure

```text
DataAnalytics-L1-CleaningData/
├── Data/
│   ├── Raw/
│   │   └── dirtycafe sales.csv
│   └── Cleaned/
│       └── cleaned_cafe_sales.csv
├── Notebook/
│   └── Data_Cleaning.ipynb
└── README.md
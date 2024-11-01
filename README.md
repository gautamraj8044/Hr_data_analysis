
---

# Employee Retention Prediction

This project uses a logistic regression model to predict employee turnover based on various features such as satisfaction level, average monthly hours, promotion status, and salary. The model aims to analyze factors contributing to employee attrition and help organizations improve retention strategies.

## Project Overview

The dataset used in this project contains data on employee performance, satisfaction, and retention. The analysis involves feature engineering, data visualization, and building a predictive model to understand the impact of these factors on employee turnover.

## Dataset

The dataset (`HR_comma_sep.csv`) includes the following columns:
- `satisfaction_level`: Employee satisfaction level
- `last_evaluation`: Last performance evaluation score
- `number_project`: Number of projects completed
- `average_montly_hours`: Average monthly hours worked
- `time_spend_company`: Years spent in the company
- `Work_accident`: Whether the employee has had a work accident (0 = No, 1 = Yes)
- `left`: Target variable, indicating if the employee left the company (0 = No, 1 = Yes)
- `promotion_last_5years`: Whether the employee was promoted in the last five years (0 = No, 1 = Yes)
- `Department`: Employee’s department
- `salary`: Employee’s salary level (low, medium, high)

## Data Preprocessing

1. **Categorical Encoding**: Transformed the `salary` column into dummy variables for model compatibility.
2. **Feature Selection**: Selected relevant columns for model training (`satisfaction_level`, `average_montly_hours`, `promotion_last_5years`, and `salary` dummy variables).

## Exploratory Data Analysis (EDA)

- **Group by Retention**: Calculated average values of the features for employees who stayed vs. those who left.
- **Visualization**:
    - Bar plots showing the relationship between `salary` and `left`.
    - Bar plots showing the relationship between `Department` and `left`.

## Model Building

Used logistic regression to predict whether an employee would leave the company based on selected features.

### Steps:

1. **Data Splitting**: Split the data into training and testing sets with a 30% training size.
2. **Model Training**: Trained a logistic regression model on the training data.
3. **Prediction and Accuracy**: Made predictions on the test data and calculated model accuracy.

### Model Performance

The accuracy of the model on the test data is calculated with the `model.score(X_test, y_test)` function.

## Requirements

To run this project, you’ll need the following libraries:

- `pandas`: For data manipulation
- `matplotlib`: For data visualization
- `scikit-learn`: For machine learning model

Install these libraries with:

```bash
pip install pandas matplotlib scikit-learn
```

## Usage

1. Clone the repository and load the dataset.
2. Run the Jupyter notebook or script to preprocess data, visualize insights, and train the logistic regression model.
3. Evaluate the model accuracy.

---

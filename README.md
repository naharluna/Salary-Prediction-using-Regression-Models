# Salary Prediction Using Regression Models

This project involves building a robust machine learning pipeline to predict employee salaries based on various demographic, educational, and professional attributes. The dataset used contains features like age, gender, degree, job title, and experience in years, alongside the target variable—salary.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Features](#features)
- [Preprocessing](#preprocessing)
- [Models](#models)
- [Evaluation](#evaluation)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [License](#license)

---

## Introduction
Salary prediction is a critical task in workforce management, helping organizations set competitive salaries and aiding professionals in career planning. This project explores various regression models and techniques to predict salaries with high accuracy.

## Dataset
The dataset is stored in the following path: `/content/drive/MyDrive/Dataset/Salary_Data.csv`. It includes the following columns:
- **Age**: Age of the employee.
- **Gender**: Gender of the employee.
- **Degree**: Educational qualification.
- **Job_title**: Job title of the employee.
- **Experience_Year**: Years of professional experience.
- **Salary**: Employee's salary (target variable).

## Features
### Numerical:
- `Age`
- `Experience_Year`
- `Salary` (target variable)

### Categorical:
- `Gender`
- `Degree`
- `Job_title`

## Preprocessing
1. **Outlier Removal**: Using the Interquartile Range (IQR) method.
2. **Label Encoding**: Converting categorical data into numerical format.
3. **Log Transformation**: To normalize the skewed salary data.
4. **Scaling**: Using `StandardScaler` and `MinMaxScaler` for numerical features.
5. **Polynomial Features**: Capturing interactions between features.

## Models
The following regression models were implemented and compared:
1. **Ridge Regression**
2. **Lasso Regression**
3. **Random Forest Regressor**
4. **Gradient Boosting Regressor**
5. **Stacking Regressor** (Ensemble Model)

## Evaluation
The models were evaluated using the following metrics:
- **R² Score**
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/naharluna/Salary-Prediction-using-Regression-Models.git
   ```
2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Load the dataset into the specified path (`/content/drive/MyDrive/Dataset/Salary_Data.csv`).
2. Run the notebook step-by-step to preprocess the data, train models, and evaluate performance.
3. Modify hyperparameters as needed to experiment with different configurations.

## Results
### Final Evaluation of Stacking Regressor
- **R² Score**: 0.87
- **Root Mean Squared Error (RMSE)**: 5500.35 (example)
- **Mean Absolute Error (MAE)**: 3100.20 (example)

The `Stacking Regressor` achieved the highest performance by combining predictions from individual models.

### Feature Importance
Permutation feature importance revealed that `Experience_Year` and `Job_title` were the most influential features for predicting salaries.

### Visualizations
- Salary distributions before and after transformations.
- Actual vs. Predicted salary scatter plots.
- Permutation feature importance bar plots.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Contributions are welcome! For any questions or suggestions, feel free to reach out or open an issue. 😊

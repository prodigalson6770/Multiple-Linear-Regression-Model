# Car Fuel Efficiency Prediction

## Project Overview
This project builds a **Multiple Linear Regression Model** to predict **Fuel Information.Highway mpg** (highway miles per gallon) using selected numerical features from the `cars.csv` dataset. The model is developed in **Python (Colab)** with necessary preprocessing, outlier removal, feature selection, and performance evaluation.

## Dataset: `cars.csv`
The dataset consists of various car specifications such as engine type, fuel efficiency, and dimensions. The target variable is:
- **Fuel Information.Highway mpg** (Highway fuel efficiency)

### Selected Features
Feature selection was performed based on **correlation analysis** and **VIF Scores**, and the final selected features are:
1. **Fuel Information.City mpg** (0.865 correlation) – Strongest predictor of highway MPG.
2. **Engine Information.Engine Statistics.Torque** (0.618 correlation) – Impacts acceleration and fuel efficiency.
3. **Dimensions.Height** (0.245 correlation) – Influences aerodynamics and fuel consumption.
4. **Dimensions.Width** (0.181 correlation) – Affects air resistance and overall efficiency.

## Model Development
The project follows these key steps:
1. **Data Preprocessing**
   - Handling missing values, duplicates, and categorical variables.
   - Removing outliers using the **IQR method**.
   - Removed duplicates
2. **Feature Selection**
   - Selecting features based on correlation analysis and VIF scores.
3. **Model Training & Evaluation**
   - Linear Regression is applied on:
   - **Selected features** (after feature selection and outlier removal)
   - Performance metrics include **Mean Squared Error (MSE)** and **R-squared (R²)**.
4. **Comparison & Results**
   - Analyzing the impact of feature selection and outlier removal on model performance.

## Performance Results
| Model Version               | Mean Squared Error (MSE) | R-squared (R²) |
|-----------------------------|-------------------------|----------------|
| Selected Features (Pre-Outlier Removal) | 2.83                   | 0.919          |
| Selected Features (Post-Outlier Removal) | 2.44                   | 0.926           |

Feature selection and outlier removal **improved the model’s generalization**, leading to a **more interpretable and efficient model**.

## Files Included
- **`cars.csv`** – The dataset containing car specifications.
- **`PA_Project.ipynb`** – Jupyter Notebook with full preprocessing, feature selection, model training, and evaluation.
- **`README.md`** – This file containing the project documentation.



## Conclusion
This project demonstrates how **feature selection and outlier removal** significantly impact model performance. The final model provides a more **accurate and interpretable** prediction of fuel efficiency based on relevant car characteristics.




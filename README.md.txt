# 💎 Diamond Price Prediction using Machine Learning

## 📌 Project Overview

This project analyzes diamond characteristics and develops machine learning regression models to predict diamond prices.

The project covers the complete machine learning workflow, including:

* Data loading and data quality checks
* Duplicate and missing-value analysis
* Exploratory Data Analysis (EDA)
* Feature preprocessing
* Ordinal encoding of categorical variables
* Train-test splitting
* Feature scaling
* Regression model development
* Model comparison
* Hyperparameter tuning
* Actual vs. predicted analysis
* Feature importance analysis

---

## 🎯 Objectives

The main objectives of this project are:

* Understand the characteristics of the diamond dataset.
* Explore relationships between diamond attributes and price.
* Identify important factors associated with diamond prices.
* Prepare numerical and categorical features for machine learning.
* Compare different regression algorithms.
* Tune the Random Forest model using cross-validation.
* Identify the most important features used for price prediction.

---

## 📊 Dataset

The dataset contains information about diamonds and their characteristics.

### Features

| Feature   | Description                                             |
| --------- | ------------------------------------------------------- |
| `carat`   | Weight of the diamond                                   |
| `cut`     | Quality of the diamond cut                              |
| `color`   | Diamond color grade                                     |
| `clarity` | Diamond clarity grade                                   |
| `depth`   | Total depth percentage                                  |
| `table`   | Width of the diamond's top relative to its widest point |
| `price`   | Diamond price — target variable                         |
| `x`       | Length in mm                                            |
| `y`       | Width in mm                                             |
| `z`       | Depth in mm                                             |

The `price` column is used as the target variable for the regression models.

---

## 🔍 Exploratory Data Analysis

The project performs exploratory analysis to understand the dataset and relationships between diamond characteristics and price.

The analysis includes:

* Numerical feature distributions
* Categorical feature distributions
* Price vs. carat
* Price vs. depth
* Price vs. table
* Price vs. diamond dimensions
* Average price by cut
* Average price by color
* Average price by clarity
* Correlation matrix

The analysis helps identify patterns and relationships that can support the machine learning stage.

---

## 🧹 Data Preprocessing

The following preprocessing steps are performed:

1. Removed the unnecessary `Index` column.
2. Checked data types and unique categorical values.
3. Checked duplicate records.
4. Checked missing values.
5. Separated features and target variable.
6. Applied ordinal encoding to categorical features.
7. Split the data into training and testing sets.
8. Applied `StandardScaler` using only the training data.

### Ordinal Encoding

The categorical variables `cut`, `color`, and `clarity` have meaningful domain-specific orderings, so ordinal encoding is used rather than arbitrary label encoding.

---

## 🤖 Machine Learning Models

Four regression algorithms are compared:

1. **Linear Regression**
2. **K-Nearest Neighbors (KNN) Regression**
3. **Decision Tree Regression**
4. **Random Forest Regression**

The models are evaluated using:

* **MAE (Mean Absolute Error)**
* **RMSE (Root Mean Squared Error)**
* **R² Score**

Since this is a regression problem, classification accuracy is not used as the evaluation metric.

---

## ⚙️ Hyperparameter Tuning

Random Forest is further optimized using `RandomizedSearchCV`.

The tuning process evaluates different combinations of:

* Number of estimators
* Maximum tree depth
* Minimum samples required for splitting
* Minimum samples per leaf
* Maximum features

Cross-validation is used to identify a better-performing Random Forest configuration.

---

## 📈 Model Evaluation

The project compares the regression models using RMSE and R² visualizations.

It also evaluates the tuned Random Forest model using:

* Actual vs. predicted price visualization
* RMSE
* MAE
* R² Score

Points closer to the diagonal line in the Actual vs. Predicted plot represent predictions closer to the actual diamond prices.

---

## 🔎 Feature Importance

Random Forest feature importance is used to identify which diamond characteristics contribute most to the model's predictions.

This provides additional interpretability and helps understand which variables are most useful for predicting diamond prices.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

---

## 📁 Project Structure

```text
Diamond-Price-Prediction/
│
├── Diamond_Price_Prediction.ipynb
├── diamonds.csv
├── README.md
└── requirements.txt
```

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/Diamond-Price-Prediction.git
```

### 2. Navigate to the project folder

```bash
cd Diamond-Price-Prediction
```

### 3. Install required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

```bash
jupyter notebook
```

Open:

```text
Diamond_Price_Prediction.ipynb
```

Make sure `diamonds.csv` is available in the expected location before running the notebook.

---

## 📌 Key Takeaways

* Exploratory Data Analysis helps identify relationships between diamond characteristics and price.
* `cut`, `color`, and `clarity` are encoded using domain-specific ordinal mappings.
* Scaling is performed after the train-test split to avoid data leakage.
* Multiple regression models are compared using MAE, RMSE, and R².
* Random Forest is further optimized using RandomizedSearchCV.
* Feature importance provides insight into the variables contributing to model predictions.

---

## 🏁 Conclusion

This project demonstrates an end-to-end machine learning approach for diamond price prediction, from data quality checks and exploratory analysis to model development, evaluation, hyperparameter tuning, and feature interpretation.

The final model should be selected based on the actual test-set **RMSE, MAE, and R²** results rather than assuming one algorithm is always superior. The tuned Random Forest provides an additional optimized model, while feature importance helps explain the variables that contribute most strongly to its predictions.

---

## 👨‍💻 Author

**Pratik Manjare**

**Skills demonstrated:**
Python • Pandas • NumPy • Data Visualization • Exploratory Data Analysis • Scikit-learn • Machine Learning • Regression • Model Evaluation • Hyperparameter Tuning

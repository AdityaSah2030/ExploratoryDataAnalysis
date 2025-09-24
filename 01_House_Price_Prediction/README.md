# House Price Prediction Pipeline 🏡

This project implements a complete machine learning pipeline to predict house prices based on the Ames Housing dataset from Kaggle. The entire workflow is divided into three main stages, each contained in its own Jupyter notebook:

1.  **Exploratory Data Analysis (EDA)**
2.  **Feature Engineering**
3.  **Feature Selection**

## 🎯 Project Purpose

The primary goal of this project is to build a robust regression model to predict the final sale price of houses. More importantly, it serves as a practical guide to structuring a data science project, demonstrating key steps like data cleaning, transformation, and feature selection that are crucial for building effective machine learning models.

---

## 📂 Project Structure

The project is organized into three sequential notebooks:

### 1. `Exploratory Data Analysis Part 1.ipynb`

**Purpose**: To understand the dataset, identify patterns, and uncover insights that will guide the feature engineering process.

**Key Activities**:
* **Loading and Inspecting Data**: Initial look at the data's shape, columns, and data types.
* **Missing Value Analysis**: Identified features with missing data and analyzed their relationship with the `SalePrice`.
* **Variable Analysis**: Differentiated between numerical (continuous/discrete) and categorical variables.
* **Visualization**: Used histograms, bar charts, and scatter plots to understand variable distributions and their relationships with the target variable (`SalePrice`).

### 2. `Feature Engineering.ipynb`

**Purpose**: To clean, transform, and create new features from the raw data to prepare it for modeling.

**Key Activities**:
* **Handling Missing Values**: Imputed missing values for both numerical (using the median) and categorical (using a "Missing" category) features.
* **Temporal Variable Engineering**: Transformed year-related features into "age" features (e.g., `HouseAge = YrSold - YearBuilt`).
* **Logarithmic Transformation**: Applied a log transform to skewed numerical features to make their distributions more normal.
* **Handling Rare Categories**: Grouped infrequent categories in categorical variables into a single "Rare" category.
* **Encoding & Scaling**: Converted categorical variables into numerical format using `LabelEncoder` and scaled all features to a common range (0 to 1) using `MinMaxScaler`.

### 3. `Feature Selection.ipynb`

**Purpose**: To select the most relevant features to build a simpler and more effective model.

**Key Activities**:
* **Lasso Regression (L1 Regularization)**: Used Lasso regression to shrink the coefficients of less important features to zero.
* **Selecting Features**: Extracted the features whose coefficients were not shrunk to zero. This significantly reduced the dimensionality of the dataset.
* **Creating the Final Dataset**: Saved a new `X_train.csv` containing only the most impactful features, which is now ready for model training.

---

## 🚀 How to Use

To run this project, follow the notebooks in their numerical order:
1.  Start with **Exploratory Data Analysis** to understand the data.
2.  Proceed to **Feature Engineering** to process the data.
3.  Finish with **Feature Selection** to create the final, model-ready dataset.

This structured approach ensures that each step builds upon the previous one, leading to a clean, well-prepared dataset ready for the final stage: model building.
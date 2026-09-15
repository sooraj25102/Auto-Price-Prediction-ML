# 🚗 Auto Price Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-Machine%20Learning-orange?logo=scikitlearn)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-blue?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-blue?logo=numpy)
![License](https://img.shields.io/badge/License-MIT-green)

## 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Business Problem](#-business-problem)
- [Objectives](#-objectives)
- [Dataset](#-dataset)
- [Technologies Used](#-technologies-used)
- [Project Workflow](#-project-workflow)
- [Exploratory Data Analysis](#-exploratory-data-analysis)
- [Data Preprocessing](#-data-preprocessing)
- [Machine Learning Models](#-machine-learning-models)
- [Model Evaluation](#-model-evaluation)
- [Results](#-results)
- [Feature Importance](#-feature-importance)
- [Project Visualizations](#-project-visualizations)
- [How to Run the Project](#-how-to-run-the-project)
- [Future Improvements](#-future-improvements)
- [Author](#-author)
- [License](#-license)

---

## 📌 Project Overview

This project develops machine learning models to predict automobile prices from vehicle characteristics such as engine size, horsepower, fuel type, body style, fuel efficiency, and vehicle dimensions.

The project demonstrates an end-to-end machine learning workflow, including:

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Feature and target preparation
- Machine learning model development
- Model evaluation and comparison
- Feature importance analysis
- Automobile price prediction

---

## 🎯 Business Problem

Determining an appropriate automobile price can be challenging because vehicle value depends on multiple characteristics, including engine specifications, dimensions, fuel efficiency, and other vehicle attributes.

An inaccurate estimate can contribute to financial loss for sellers, overpayment by buyers, or inefficient inventory pricing for dealerships. Machine learning provides a data-driven way to model relationships between vehicle characteristics and prices.

---

## 🎯 Objectives

- Clean and preprocess the automobile dataset.
- Perform Exploratory Data Analysis (EDA).
- Prepare numerical and categorical features for machine learning.
- Train and compare regression models.
- Evaluate model performance using appropriate regression metrics.
- Identify influential features in the Random Forest model.
- Select a model based on the evaluation results.

---

## 📂 Dataset

| Attribute | Details |
|---|---|
| Dataset | Automobile Imports Dataset |
| Type | Structured CSV |
| Target variable | `price` |
| Features | Vehicle specifications including engine size, horsepower, dimensions, fuel type, body style, and other attributes |

The dataset includes missing values in some feature columns. These are handled in the preprocessing pipeline rather than by modifying the original DataFrame.

---

## 🛠️ Technologies Used

- Python 3.11
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## 📊 Project Workflow

```text
Dataset
   ↓
Data Cleaning
   ↓
Data Type Correction
   ↓
Exploratory Data Analysis
   ↓
Feature and Target Separation
   ↓
Train-Test Split
   ↓
Preprocessing Pipeline
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Model Comparison
   ↓
Feature Importance Analysis
   ↓
Final Model Selection
```

---

## 📈 Exploratory Data Analysis

The dataset was explored to understand its structure, distributions, relationships, and data quality.

Key activities included:

- Missing-value analysis
- Distribution analysis
- Correlation analysis
- Feature relationship analysis
- Data type inspection
- Identification of potentially influential vehicle attributes

---

## ⚙️ Data Preprocessing

A pipeline-based preprocessing approach was used to prepare the features for machine learning.

### Numerical Features

Missing numerical values are handled using median imputation.

### Categorical Features

Missing categorical values are handled using most-frequent imputation. Categorical variables are transformed using one-hot encoding.

```python
OneHotEncoder(
    handle_unknown="ignore",
    drop="first"
)
```

`handle_unknown="ignore"` allows transformation to continue if a category appears in the test data that was not present in the training data. It does not learn new categories from the test data.

### Train-Test Split

The dataset was divided into training and testing subsets using an 80/20 split.

Preprocessing is incorporated into the model pipelines so imputation and encoding are fitted using training data, helping reduce the risk of data leakage.

---

## 🤖 Machine Learning Models

Two regression models were developed and evaluated.

### 1. Linear Regression

Linear Regression was used as a baseline model to establish a reference level of predictive performance.

### 2. Random Forest Regression

Random Forest Regression was used to model potentially nonlinear relationships between automobile characteristics and prices.

---

## 📊 Model Evaluation

The models were evaluated using three standard regression metrics.

### Mean Absolute Error (MAE)

MAE measures the average absolute difference between actual and predicted automobile prices. Lower values indicate smaller average errors.

### Root Mean Squared Error (RMSE)

RMSE is the square root of the average squared prediction error and gives greater weight to larger errors. Lower values indicate better performance.

### R² Score

R² measures how well the model explains variation in the target values. A higher value generally indicates a better fit on the evaluated dataset.

---

## 🏆 Results

Use the metrics generated by the latest successful execution of the notebook. The values below reflect the latest outputs available during this README update; if you change the data, split, or model configuration, rerun the notebook and update this table.

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 2028.65 | 3295.57 | 0.9112 |
| **Random Forest Regression** | **1899.16** | **2946.08** | **0.9291** |

### Best Model: Random Forest Regression

In the current evaluation, Random Forest Regression performed better than Linear Regression across the three reported metrics, with lower MAE and RMSE and a higher R² score. It was selected as the final model for this experiment.

---

## 🔍 Feature Importance

The Random Forest feature-importance analysis identified the following top features in the latest notebook output:

| Rank | Feature | Importance |
|---:|---|---:|
| 1 | Curb Weight | 0.434808 |
| 2 | Engine Size | 0.307027 |
| 3 | Highway MPG | 0.054771 |
| 4 | Horsepower | 0.053670 |
| 5 | City MPG | 0.039999 |
| 6 | Width | 0.030210 |
| 7 | Wheel Base | 0.011881 |
| 8 | Make — BMW | 0.009707 |
| 9 | Peak RPM | 0.007236 |
| 10 | Normalized Losses | 0.006987 |

Curb Weight and Engine Size were the two most influential features in this model's feature-importance output. Feature importance describes the model's use of features and should not be interpreted as proof of causation.

If a future notebook run produces different importance values, update this table using the newly generated output.

---

## 📷 Project Visualizations

The notebook includes visualizations for model evaluation and interpretation:

- **Actual vs. Predicted Prices:** compares predicted prices with actual prices for both models.
- **Model Comparison:** presents the prediction results of Linear Regression and Random Forest for comparison.
- **Residual Analysis:** examines prediction errors relative to the zero reference line.
- **Feature Importance:** displays the top features used by the Random Forest model.

If you export images from the notebook, save them in an `images/` folder and link them here. Do not add image links until the corresponding files exist in the repository.

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/sooraj25102/Auto-Price-Prediction-ML.git
```

### 2. Navigate to the Project Directory

```bash
cd Auto-Price-Prediction-ML
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open the project notebook and run the cells sequentially.

---

## 🔮 Future Improvements

Potential future improvements include:

- Hyperparameter tuning
- Cross-validation
- Evaluation of additional regression algorithms
- XGBoost implementation
- A Streamlit web application
- Flask or FastAPI deployment
- Docker containerization

---

## 👨‍💻 Author

**Sooraj R**

- GitHub: [sooraj25102](https://github.com/sooraj25102/Auto-Price-Prediction-ML)
- LinkedIn: [Sooraj R](https://www.linkedin.com/in/sooraj-r-869a49248)

---

## 📜 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

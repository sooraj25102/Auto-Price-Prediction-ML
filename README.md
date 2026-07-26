
# 🚗 Auto Price Prediction using Machine Learning

![Python](https://img.shields.io/badge/Python-3.13-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikitlearn)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-blue?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Scientific%20Computing-blue?logo=numpy)
![License](https://img.shields.io/badge/License-MIT-green)

## 📑 Table of Contents

- Project Overview
- Business Problem
- Objectives
- Dataset
- Technologies Used
- Project Workflow
- Exploratory Data Analysis
- Feature Engineering
- Machine Learning Models
- Model Evaluation
- Results
- Visualizations
- Future Improvements
- Installation
- Author

---


## 📌 Project Overview

This project develops a machine learning model to predict automobile prices based on various vehicle characteristics such as engine size, horsepower, fuel type, body style, and dimensions.

The project demonstrates a complete end-to-end data science workflow, including:

- Data Cleaning and Preprocessing
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Regression Model Development
- Model Evaluation and Comparison
- Price Prediction
---
## 🎯 Business Problem

Determining the appropriate selling price of a used automobile is a complex task because vehicle value depends on multiple technical and market-related factors.

An inaccurate price can result in:

- Financial loss for sellers
- Overpayment by buyers
- Inefficient inventory pricing for dealerships

Machine Learning provides a data-driven solution by learning relationships between vehicle attributes and market prices to generate reliable price estimates.


---
## 🎯 Objectives

- Clean and preprocess the dataset.
- Perform Exploratory Data Analysis (EDA).
- Engineer features for better model performance.
- Train multiple regression models.
- Evaluate and compare model performance.
- Predict automobile prices accurately.

---

## 📂 Dataset

| Attribute | Details |
|------------|----------|
| Dataset | Automobile Imports Dataset |
| Type | Structured CSV |
| Target Variable | Price |
| Features | Engine Size, Horsepower, Fuel Type, Body Style, etc. |

---

## 🛠️ Technologies Used

- Python
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
Exploratory Data Analysis
   ↓
Feature Engineering
   ↓
Train-Test Split
   ↓
Model Training
   ↓
Model Evaluation
   ↓
Price Prediction
```

---

## 📈 Exploratory Data Analysis

Key activities:

- Missing value analysis
- Outlier detection
- Correlation analysis
- Distribution analysis
- Feature relationships

---

## 🤖 Machine Learning Models

- Linear Regression
- Random Forest Regressor

---

## 📊 Model Performance

| Model | MAE | RMSE | R² Score |
|------|------:|------:|------:|
| Linear Regression |3174.5091612245647 |4924.882365960312 |0.8017563871328728 |
| Random Forest |1904.5325406504069 |3061.5947719977466 |0.9233869246262107 |

*(Replace these with your actual results.)*

---

## 📷 Project Visualizations

Add screenshots here after uploading them to the `images` folder.

Example:

```markdown
### Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

### Feature Importance

![Feature Importance](images/feature_importance.png)

### Actual vs Predicted

![Actual vs Predicted](images/actual_vs_predicted.png)
```

---

## 🚀 How to Run the Project

```bash
git clone https://github.com/sooraj25102/Auto-Price-Prediction-ML.git

cd Auto-Price-Prediction-ML

pip install -r requirements.txt

jupyter notebook
```

---

## 🔮 Future Improvements

- Hyperparameter tuning
- XGBoost implementation
- Streamlit web application
- Flask API deployment
- Docker containerization

---

## 👨‍💻 Author

**Sooraj R**

- GitHub: https://github.com/sooraj25102
- LinkedIn:https://www.linkedin.com/in/sooraj-r-869a49248

---

## 📜 License

This project is licensed under the MIT License.

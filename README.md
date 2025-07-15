# California Housing Price Prediction  
**Summer Training Project | Lovely Professional University**  
**Guided by: Ms. Sandeep Kaur & Mr. Jaffar Amin Chacket**

---

## 📌 Project Overview

This project was developed as part of the summer training program at Lovely Professional University. The goal was to predict median housing prices across various districts in California using supervised machine learning algorithms and visualize meaningful insights using Power BI. 

The dataset, sourced from `sklearn.datasets`, contains detailed information on housing blocks, including features such as median income, average number of rooms, housing age, and geographic coordinates. These attributes serve as predictive variables for estimating house prices.

The final deliverables include:
- A machine learning pipeline for data analysis, modeling, and evaluation
- An interactive Power BI dashboard that presents geographic, demographic, and economic insights
- A structured report documenting methodology, results, and findings

---

## 🎯 Project Objectives

- Load and explore the California Housing dataset
- Clean the data and handle outliers
- Engineer new features to enhance prediction accuracy
- Perform comprehensive exploratory data analysis (EDA)
- Train and evaluate multiple regression models
- Build an interactive Power BI dashboard to visualize the insights

---

## 🔍 Dataset Description

The dataset was accessed using `fetch_california_housing()` from `sklearn.datasets` and includes the following features:

| Feature         | Description                                   |
|-----------------|-----------------------------------------------|
| MedInc          | Median income in block group                  |
| HouseAge        | Median house age                              |
| AveRooms        | Average number of rooms per household         |
| AveBedrms       | Average number of bedrooms per household      |
| Population      | Total population in block group               |
| AveOccup        | Average number of household members           |
| Latitude        | Geographical coordinate (north-south)         |
| Longitude       | Geographical coordinate (east-west)           |
| MedHouseVal     | Median house value (target variable)          |

Additional engineered features include:
- `RoomsPerHousehold` = AveRooms / HouseAge
- `BedroomsPerRoom` = AveBedrms / AveRooms
- `PopulationPerHousehold` = Population / HouseAge

---

## 🧠 Exploratory Data Analysis (EDA)

EDA was performed using **matplotlib** and **seaborn** to understand data distribution and feature relationships:

- Correlation heatmap to identify feature relevance
- Distribution of target variable (`MedHouseVal`)
- Scatter plots: `MedInc` vs `MedHouseVal`, `Latitude` vs `MedHouseVal`
- Box plots for house age ranges
- KDE plots and pair plots to study interactions
- Output images stored in `/eda_outputs/`

---

## 🧪 Machine Learning Models

Three regression algorithms were trained and compared:

1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**

The dataset was split (80/20) using `train_test_split`. Metrics used for evaluation:
- **R² Score**: Coefficient of determination
- **RMSE**: Root Mean Squared Error
- **MAE**: Mean Absolute Error

### 📈 Model Performance Summary

| Model                 | R² Score | RMSE   | MAE   |
|----------------------|----------|--------|-------|
| Linear Regression     | 0.5786   | 0.6356 | 0.4742|
| Decision Tree         | 0.5410   | 0.6633 | 0.4391|
| **Random Forest**     | **0.7724** | **0.4672** | **0.3139**|

---

## 📊 Power BI Dashboard

The Power BI dashboard provides rich, interactive visualizations:

- **Map View**: Price hotspots across California using Latitude & Longitude
- **KPI Cards**: Avg Income, Avg House Price
- **Scatter Chart**: Median Income vs House Value
- **Bar Chart**: Model-wise performance comparison
- **Pie Chart**: House Age Distribution
- **Slicers**: Filter insights by income range, location, or housing age

Dashboard File: `dashboard/power_bi_dashboard.pbix`

---

## 🗂 Folder Structure

```
├── data/
│   └── california_housing_cleaned.csv
├── eda_outputs/
│   └── heatmaps, scatter plots, pair plots, etc.
├── model/
│   └── model_evaluation_results.csv
├── notebooks/
│   └── california_housing_model.ipynb
├── dashboard/
│   └── power_bi_dashboard.pbix
└── README.md
```

---

## 🧾 Skills Demonstrated

- Data preprocessing & outlier detection
- Feature engineering & transformation
- Statistical & visual data analysis
- Supervised regression modeling
- Performance evaluation using sklearn metrics
- Power BI dashboard creation for business insights

---

## 🙏 Acknowledgements

This project was completed as part of the Summer Training Program at **Lovely Professional University**, under the mentorship of:

- **Ms. Sandeep Kaur**
- **Mr. Jaffar Amin Chacket**

Special thanks to the creators of open-source tools and the data science community whose documentation and forums greatly aided this project.

---

## 📎 License

This repository is for academic and educational purposes only. All rights reserved by the author.

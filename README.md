# adult-income-analysis
Exploratory Data Analysis (EDA) of the UCI Adult Income dataset using Pandas, NumPy, and Matplotlib.

**Course:** CS 5 - Introduction to Machine Learning  
**Project:** Week 4 Jupyter Notebook Analysis  
**Team:** Azin Shahrokhi, Ione Axelrod, David Chang

## 📋 Project Overview
This project involves a comprehensive exploratory data analysis (EDA) of the **Adult Income dataset** from the UCI Machine Learning Repository. The goal was to perform data quality checks, handle formatting inconsistencies, and use statistical methods to understand the relationship between demographic features and income levels.

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** - **Pandas:** Data manipulation and cleaning.
  - **NumPy:** Statistical operations (Mean, Std Dev, Min/Max).
  - **Matplotlib:** Data visualization (Bar charts, Scatter plots).

## 🧪 Key Data Engineering Tasks

### 1. Data Cleaning (The "Strip" Fix)
During the analysis, I identified a common real-world data issue: **formatting inconsistencies**. Categorical strings in the "income" column contained leading spaces (e.g., `" <=50K"` instead of `"<=50K"`). 
- **Solution:** I implemented `.str.strip()` to clean the strings before mapping them to numeric values (`0` and `1`) for visualization.

### 2. NumPy Statistical Profiling
I converted the `hours_per_week` feature into a NumPy array to calculate the "Workforce Profile":
- **Average Work Week:** ~40.4 hours.
- **Standard Deviation:** ~12.3 hours (indicating significant variation in work schedules).
- **Range:** 1 to 99 hours per week.

## 📈 Visualizations & Insights

### Income Distribution
The analysis revealed a significant **class imbalance**, with the `<=50K` category being substantially larger than the `>50K` category. This is a critical observation for future Machine Learning model training.

### Hours Worked vs. Income
Using a scatter plot with transparency (`alpha=0.3`), I analyzed the overlap between work hours and income. The results suggest that "hours worked" alone is not a definitive predictor of income, as both classes show heavy density around the 40-hour mark.

## 💡 Reflection & Learning
- **Dataset Choice:** Selected the UCI Adult Income dataset for its balance of numeric and categorical data.
- **Tools:** Utilized `df.isna().sum()` to verify data integrity and `df.info()` to manage memory and data types.
- **Next Steps:** To build a predictive model, I would next implement **One-Hot Encoding** for categorical variables like `education` and `marital_status`.

---

### 📂 Repository Contents
- `Week4_Jupyter_Group1.ipynb`: The complete analysis and visualization notebook.
- `adult.data`: The source dataset from UCI.

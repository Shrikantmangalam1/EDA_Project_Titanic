# EDA_Project_Titanic

# 🚢 Titanic Dataset – Exploratory Data Analysis (EDA)
### *A Visual & Statistical Journey into the Most Famous Shipwreck*

<p align="center">
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Notebook-Google%20Colab-orange?style=for-the-badge&logo=googlecolab" />
  <img src="https://img.shields.io/badge/Visualization-Matplotlib-yellow?style=for-the-badge&logo=graphite" />
  <img src="https://img.shields.io/badge/Category-Data%20Analysis-purple?style=for-the-badge" />
</p>

---

## 🌟 Project Summary

This repository contains a **comprehensive Exploratory Data Analysis (EDA)** of the Titanic dataset.  
The goal is to deeply understand **survival patterns, passenger demographics, class differences, and hidden relationships** through high-quality visualizations, feature engineering, and statistical insight.

---

## 📌 Key Features

✔ Merging train & test datasets  
✔ Handling missing values  
✔ Univariate, Bivariate & Multivariate Analysis  
✔ Crosstab visualizations  
✔ Feature Engineering: **Child, Family Size**  
✔ Insightful visual charts  
✔ Clean, structured notebook  
✔ Final conclusions with real patterns  

---

## 📂 Repository Structure

├── EDA_Titanic.ipynb
├── README.md
├── train.csv
└── test.csv

---

## 🚀 Tech Stack

| Tool          | Purpose                      |
|---------------|------------------------------|
| Python        | Data manipulation & analysis |
| Pandas        | Data handling                |
| NumPy         | Numerical operations         |
| Matplotlib    | Visualizations               |
| Google Colab  | Notebook execution           |

---

# 📊 Analysis Overview

## 🔹 Univariate Analysis
- Age distribution  
- Gender ratio  
- Passenger class distribution  
- Survived vs Not Survived  

## 🔹 Bivariate Analysis
- Survival by Gender  
- Survival by Class (Pclass)  
- Embarked vs Class  
- Child survival comparison  
- Family size vs Survival  

## 🔹 Multivariate Analysis
- Gender + Class + Survival  
- Family Size + Gender + Survival  

---

# 🎨 Visual Outputs

A range of charts created using Matplotlib:

📌 Histograms  
📌 Boxplots  
📌 Pie Charts  
📌 Bar & Stacked Bar Graphs  
📌 Crosstab percentage plots  

Each chart helps uncover patterns not immediately visible in raw numbers.

---

# 🛠 Feature Engineering

### ✨ Created new columns:

| Feature       | Description         |
|---------------|----------------------|
| Child         | True if Age < 18     |
| Family_size   | SibSp + Parch + 1    |

These additional features reveal deeper insights such as **family survival patterns**.

---

# 🧠 Major Insights

### 🔥 Key Takeaways from the EDA

- **Females had a significantly higher survival rate** than males  
- **1st Class passengers survived the most**, 3rd Class the least  
- **Girl children survived more than boy children**  
- **Large families had extremely low survival rates**  
- Majority of those who died were **male + 3rd class**  
- Passengers from **Southampton (S)** were mostly 3rd class and had lower survival  

---

# 🖥 How to Run This Project

### 1️⃣ Clone the repository  
```bash
git clone https://github.com/Shrikantmangalam1/EDA_Project_Titanic/tree/Shrikantmangalam1-EDA-project
2️⃣ Open the notebook

Use Google Colab or Jupyter Notebook

3️⃣ Ensure datasets are present

Ensure train.csv and test.csv are in the same directory

4️⃣ Run all cells sequentially
5️⃣ Enjoy the insights 🔍
📘 Future Improvements

🔸 Add Seaborn visualizations
🔸 Apply ML models for prediction
🔸 Deploy a dashboard using Power BI / Tableau
🔸 Create an interactive web app

❤️ Connect With Me

If you find this project useful, feel free to ⭐ star the repo!

📧 Email:
shrikantmangalam2002@gmail.com

💼 LinkedIn:
www.linkedin.com/in/shrikant-mangalam-75148126a


# 🚢 Titanic – Exploratory Data Analysis (EDA)

A complete exploratory data analysis on the Titanic dataset covering univariate, bivariate, multivariate analysis and feature engineering — with visualisations and key insights.

---

## 📁 Project Structure

```
titanic-eda/
├── EDA_Titanic.ipynb   # Main notebook
├── train.csv           # Training data (891 passengers)
├── test.csv            # Test data (418 passengers)
├── plots/              # All generated visualisations
└── README.md
```

---

## 📦 Dataset

- **Source**: [Kaggle Titanic Competition](https://www.kaggle.com/c/titanic)
- **Train**: 891 rows × 12 columns
- **Test**: 418 rows × 11 columns
- **Merged for EDA**: 1,309 rows × 12 columns

---

## 🛠️ Setup & Run

```bash
pip install pandas numpy matplotlib
jupyter notebook EDA_Titanic.ipynb
```

---

## 📊 Analysis

---

### 1. Univariate Analysis — Age

#### Box Plot – Age (Merged Dataset)
![Age Boxplot Merged](plots/01_age_boxplot_merged.png)

#### Box Plot – Age (Train Dataset)
![Age Boxplot Train]((https://raw.github.com/Shrikantmangalam1/EDA_Project_Titanic/main/Graphs/box_plot_train.png))

#### Age Distribution Histogram
![Age Histogram](plots/03_age_histogram.png)

> **Insight:** The age distribution is right-skewed. The most common age group was **20–24 years** (160 passengers). Median age was ~28 years. There were **263 missing values** in the Age column.

---

### 2. Univariate Analysis — Survived

#### Survival Distribution
![Survival Pie Chart](plots/04_survival_distribution_pie.png)

> **Insight:** Among passengers with known outcomes, **342 survived** and **549 died**, giving a survival rate of **38.38%**. 418 passengers (test set) had missing survival data (grey slice).

---

### 3. Univariate Analysis — Passenger Class (Pclass)

#### Pclass Histogram
![Pclass Histogram](plots/05_pclass_histogram.png)

#### Pclass Distribution Pie Chart
![Pclass Pie](plots/06_pclass_pie.png)

> **Insight:** More than half the passengers (**54.2%**) travelled in 3rd class. 1st class accounted for 24.7% and 2nd class for 21.2%. No missing values in this column.

---

### 4. Univariate Analysis — Sex

#### Sex Ratio
![Sex Ratio Pie](plots/07_sex_ratio_pie.png)

> **Insight:** The passenger manifest was heavily male-dominated — **64.4% male** vs **35.6% female**. No missing values.

---

### 5. Bivariate Analysis — Survived vs Pclass

#### Which class had the most deaths/survivors? (Row-normalised)
![Survival % per Class Row](plots/08_survival_pct_per_class_row.png)

> Among all who **died**: 67.76% were from Class 3, 17.67% from Class 2, only 14.57% from Class 1.
> Among all who **survived**: 39.77% were from Class 1, 34.80% from Class 3, 25.44% from Class 2.

#### What was the survival rate within each class? (Column-normalised)
![Survival % per Class Col](plots/09_survival_pct_per_class_col.png)

> **Insight:** Survival rates within each class:
> - Class 1: **62.96% survived**
> - Class 2: **47.28% survived**
> - Class 3: only **24.24% survived**

---

### 6. Bivariate Analysis — Survived vs Sex

#### Survival Count by Gender
![Survival by Gender](plots/10_survival_count_by_gender.png)

> **Insight:** Gender was one of the strongest predictors of survival.
> - **74.2% of females survived**
> - Only **18.9% of males survived**

---

### 7. Bivariate Analysis — Pclass vs Sex

#### Gender Diversity in Each Class
![Gender Diversity in Class](plots/11_gender_diversity_in_class.png)

> **Insight:** Class 1 had the highest female proportion (44.6%), while Class 3 was most male-heavy (69.5%).

---

### 💡 Insight 01

> **The majority of survivors were Class 1 females**, while **the majority of deaths were Class 3 males**. Passenger class and gender together were the primary determinants of survival.

---

### 8. Children Survival Analysis

#### Were girl children more likely to survive than boy children?
![Children Survival](plots/12_children_survival.png)

| Sex | Died | Survived |
|-----|------|----------|
| Female | 17 | 38 |
| Male | 35 | 23 |

> **💡 Insight 02:** Girl children had a significantly better survival rate — **38 survived vs 23 boy children**, despite more boys being present overall.

---

### 9. Bivariate Analysis — Embarked vs Pclass

#### Passenger Diversity over Embarkment Port
![Embarkment vs Pclass](plots/13_passengers_diversity_embarkment.png)

| Port | Class 1 | Class 2 | Class 3 |
|------|---------|---------|---------|
| C (Cherbourg) | 52.2% | 10.4% | 37.4% |
| Q (Queenstown) | 2.4% | 5.7% | **91.9%** |
| S (Southampton) | 19.4% | 26.5% | 54.2% |

> **Insight:** Queenstown was almost exclusively Class 3 (91.9%). Cherbourg had the most Class 1 passengers (52.2%).

---

### 10. Feature Engineering — Family Size

`Family_size = SibSp + Parch + 1`

| Family Size | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 11 |
|------------|---|---|---|---|---|---|---|---|----|
| Survived % | 30.4 | 55.3 | 57.8 | **72.4** | 20.0 | 13.6 | 33.3 | 0 | 0 |

> **💡 Insight 03:** The sweet spot for survival was a **family of 2–4 members**. Very large families (8 or 11 members — all from the Sage family in Class 3) had a **0% survival rate**.

---

### 11. Multivariate Analysis — Sex + Pclass + Survived

#### Survival % by Gender and Class
![Survival by Gender and Class](plots/14_survival_pct_by_gender_class.png)

| Sex | Class | Survived % |
|-----|-------|------------|
| Female | 1 | **96.8%** |
| Female | 2 | **92.1%** |
| Female | 3 | 50.0% |
| Male | 1 | 36.9% |
| Male | 2 | 15.7% |
| Male | 3 | 13.5% |

> **Insight:** First-class females had a **96.8% survival rate**. Third-class males had only **13.5%**. Being female in any class gave better odds than being male in Class 1.

---

### 12. Multivariate Analysis — Family Size + Sex + Survived

#### Family Survival Rate by Gender
![Family Survival by Gender](plots/15_family_survival_by_gender.png)

> **Insight:** Across almost all family sizes, females consistently had a higher survival rate than males. The gender advantage was most pronounced in smaller family groups (sizes 1–3).

---

## 🔑 Summary of Key Insights

| # | Insight |
|---|---------|
| 1 | **Class + Gender = survival priority** — Class 1 females had ~97% survival; Class 3 males only ~14% |
| 2 | **Girl children survived more** than boy children — consistent with "women and children first" |
| 3 | **Optimal family size** for survival was 2–4; large families (8–11) had 0% survival |
| 4 | **Queenstown** passengers were almost entirely Class 3, the most at-risk group |
| 5 | **38.38% overall survival rate** — skewed by the large proportion of Class 3 male passengers |

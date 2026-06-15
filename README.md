
---# Sleep Health & Lifestyle Analysis

## 📌 Project Overview

The primary objective of this project is to analyze, explore, and model how an individual's daily lifestyle habits influence the quality and duration of their sleep using data science and machine learning techniques.

Through this data-driven analysis, we aim to uncover how minor adjustments in daily routines can pave the way for significantly better rest and overall well-being.

---

## 🎯 Project Objectives

* **Data Exploration:** Investigate and identify core correlations between daily behavioral habits and physiological metrics.
* **Predictive Modeling:** Build a machine learning model (initiated in the `mark_linear.ipynb` notebook) to predict an individual's sleep quality score or sleep duration based on their specific lifestyle factors.
* **Insight Generation:** Deliver practical, data-backed recommendations and actionable tips to help individuals optimize their daily routines for superior sleep health.

---

## 🧠 Model Technical Description: Linear Regression

The core predictive mechanism utilized within the `mark_linear.ipynb` notebook is a **Linear Regression** model.

### 1. Working Principle

Linear Regression is a foundational **Supervised Machine Learning** algorithm. In this project, we treat lifestyle habits as **Independent Variables ($X$)** and the sleep quality score as the **Dependent Target Variable ($Y$)**.

The algorithm works by establishing a mathematically optimal **Best-Fit Straight Line** through the data points. The relationship is represented by the following equation:

$$Y = \beta_0 + \beta_1X_1 + \beta_2X_2 + \dots + \beta_nX_n + \epsilon$$

* **$Y$**: The Target Variable (The predicted *Sleep Quality* score).
* **$X_1, X_2, \dots, X_n$**: Input Features (e.g., *Physical Activity, Stress Level, Heart Rate*).
* **$\beta_0$**: The Intercept (The baseline sleep quality score if all lifestyle inputs were mathematically zero).
* **$\beta_1, \beta_2, \dots, \beta_n$**: Coefficients/Weights (Indicates the direction and strength of the impact each individual lifestyle factor has on sleep).
* **$\epsilon$**: The Error Term (Accounts for random variations not explained by the model).

---

### 2. Model Pipeline (Step-by-Step Process)

The development lifecycle of the model follows a structured pipeline:

1. **Data Preprocessing:** Transforming categorical variables (such as *Gender* or *Occupation*) into numerical formats using encoding techniques and resolving any missing values.
2. **Feature Selection:** Identifying and selecting highly correlated variables (such as isolating *Stress Level* against *Sleep Quality*) to ensure maximum predictive power.
3. **Train/Test Split:** Partitioning the dataset into an **80% Training set** (for the model to learn patterns) and a **20% Testing set** (to evaluate real-world performance).
4. **Model Training:** Initializing and fitting the `LinearRegression()` algorithm from the `scikit-learn` library onto the prepared training data.

---

### 3. Model Evaluation Metrics

To accurately evaluate how precisely the model predicts sleep metrics, the following evaluation standards are deployed:

* **Mean Absolute Error (MAE):** Measures the average absolute difference between the actual sleep scores and the scores predicted by the model.
* **$R^2$ Score (Coefficient of Determination):** Quantifies the proportion of variance in sleep quality that can be predicted from the lifestyle factors. It scales from $0$ to $1$, where values closer to $1$ signify an excellent model fit.

---

### 4. Key Business & Health Insights

By decoding the model's coefficients ($\beta$ values), we can extract valuable, real-world conclusions:

* 📉 **Negative Correlation:** A negative coefficient for *Stress Level* confirms that as daily stress thresholds escalate, overall sleep quality predictably degrades.
* 📈 **Positive Correlation:** A positive coefficient for *Physical Activity* establishes that increasing daily exercise levels directly boosts the structural quality of rest.

---

## 🛠️ Tech Stack & Tools

* **Language:** Python
* **Environment:** Jupyter Notebooks (`.ipynb`)
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn



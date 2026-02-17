# 🚢 Titanic Survival Prediction  
### End-to-End Machine Learning Project  
*Kaggle Competition: [Titanic - Machine Learning from Disaster](https://www.kaggle.com/competitions/titanic)*

---

## 🎯 Project Objective

Develop predictive models to estimate passenger survival probability using demographic and socio-economic features.

This project was structured as a **multi-stage experimental pipeline**, designed to evaluate the impact of:

- 📊 Data preprocessing
- 🧠 Feature engineering
- 🤖 Model selection
- ⚙️ Algorithmic complexity
- 📉 Overfitting risk

---

# 🔬 Methodology

The project was divided into four progressive development stages.

---

## 🧱 Stage 1 — Baseline Model

Established a performance benchmark with minimal preprocessing.

### ✔ Key Actions

- Exploratory Data Analysis using *ydata-profiling*
- Removal of high-cardinality features
- Missing value imputation:
  - Mean (numerical)
  - Mode (categorical)
- Removal of text-based features
- Models trained:
  - Decision Tree
  - K-Nearest Neighbors
  - Logistic Regression
- Evaluation metrics:
  - Accuracy
  - Confusion Matrix

**Public Kaggle Score:** `0.66746`

---

## 🧩 Stage 2 — Categorical Feature Engineering

Integrated categorical variables properly into the modeling pipeline.

### ✔ Improvements

- Custom transformations using `lambda`
- Encoding via *OneHotEncoder*
- Same algorithms maintained for controlled comparison

**Public Kaggle Score:** `0.76555`

📈 Significant performance gain after proper categorical encoding.

---

## 🧠 Stage 3 — Advanced Feature Engineering & Optimization

Focused on domain understanding and feature enhancement.

### ✔ Enhancements

**Feature Scaling**
- Standardization of `Age` and `Fare`

**New Engineered Features**
- `FamilySize` = SibSp + Parch + 1
- `IsAlone` = Binary indicator

**Correlation Analysis**
- Selection of statistically relevant variables

Models maintained:
- Decision Tree
- KNN
- Logistic Regression

**Public Kaggle Score:** `0.77033` ⭐

📈 Incremental improvement driven by feature engineering.

---

## 🤖 Stage 4 — Advanced Algorithms

Tested more complex models while keeping all engineered features.

### ✔ Models Evaluated

- Logistic Regression
- Random Forest
- MLPClassifier (Neural Network)

Although the MLP achieved the highest validation accuracy, it underperformed in the Kaggle submission — indicating probable **overfitting**.

**Public Kaggle Score:** `0.69856`

⚠ Clear evidence of reduced generalization.

---

# 📊 Performance Evolution

| Stage | Strategy | Public Score |
|-------|----------|-------------|
| 1 | Baseline | 0.66746 |
| 2 | Categorical Encoding | 0.76555 |
| 3 | Feature Engineering | **0.77033** |
| 4 | Complex Models | 0.69856 |

---

# 🧠 Key Takeaways

- Feature engineering had greater impact than model complexity.
- More complex models do not guarantee better generalization.
- Validation performance must be interpreted cautiously.
- Structured experimentation improves model development clarity.

---

# 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- ydata-profiling

---

# 📌 Next Steps

- Implement robust cross-validation strategy
- Apply GridSearch / RandomSearch
- Experiment with Gradient Boosting (XGBoost, LightGBM)
- Improve feature selection pipeline

---

📬 Feel free to connect or reach out for collaboration.

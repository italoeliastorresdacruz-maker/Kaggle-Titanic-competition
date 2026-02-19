# 🚢 Titanic Survival Prediction  
### Kaggle Competition – Machine Learning from Disaster

This project aims to predict passenger survival on the Titanic using Machine Learning techniques. The development was structured in progressive stages to evaluate how different data treatments and modeling strategies impacted performance.

---

## 🎯 Objective

To build predictive models capable of estimating survival probability based on demographic and socio-economic features, while analyzing how each improvement influenced the final results.

---

## 🔬 Project Development

The project was divided into **five progressive stages**, each focused on specific improvements in the modeling pipeline.

---

## 🧱 Stage 1 – Baseline Model

In this initial stage, only basic preprocessing was applied in order to establish a performance baseline.

### ✔ Actions performed:

- Exploratory Data Analysis using **ydata-profiling**
- Removal of high-cardinality features
- Missing value treatment:
  - Mean for numerical variables
  - Mode for categorical variables
- Removal of text-based features
- Models trained:
  - **Decision Tree**
  - **K-Nearest Neighbors (KNN)**
  - **Logistic Regression**
- Evaluation metrics:
  - **Accuracy**
  - **Confusion Matrix**

**Public Kaggle Score:** `0.66746`

This stage served as a benchmark for subsequent improvements.

---

## 🧩 Stage 2 – Categorical Feature Treatment

The focus of this stage was properly incorporating categorical variables into the modeling process instead of discarding them.

### ✔ Improvements implemented:

- Custom transformations using `lambda`
- Encoding using **OneHotEncoder**
- Same algorithms maintained for controlled comparison

**Public Kaggle Score:** `0.76555`

📈 A significant performance gain was observed after properly handling categorical variables.

---

## 🧠 Stage 3 – Feature Engineering

In this phase, the objective was to better understand the dataset and extract more meaningful features.

### ✔ Adjustments made:

- Standardization of `Age` and `Fare`
- Creation of new features:
  - `FamilySize = SibSp + Parch + 1`
  - `IsAlone` (binary indicator)
- Correlation analysis to select the most relevant variables

The same models were maintained to ensure fair comparison.

**Public Kaggle Score:** `0.77033`

---

## 🤖 Stage 4 – More Complex Models

All engineered features were maintained, and more complex algorithms were tested.

### ✔ Algorithms evaluated:

- **Logistic Regression**
- **Random Forest**
- **MLPClassifier (Neural Network)**

The **MLPClassifier** achieved the highest validation accuracy. However, its performance decreased in the Kaggle submission.

**Public Kaggle Score:** `0.69856`

⚠ This behavior suggests probable **overfitting**, where the model fit the training data well but failed to generalize properly.

---

## ⚙️ Stage 5 – Hyperparameter Optimization with GridSearchCV

In the final stage, **GridSearchCV** was applied to optimize the hyperparameters of the models tested previously.

After optimization:

- The best-performing model was **Random Forest**
- Performance improved compared to Stage 4 and surpassed Stage 3

**Public Kaggle Score:** `0.78229`

---

## 📊 Performance Evolution

| Stage | Strategy | Public Score |
|-------|----------|--------------|
| 1 | Baseline Model | 0.66746 |
| 2 | Categorical Encoding | 0.76555 |
| 3 | Feature Engineering | 0.77033 |
| 4 | Complex Models | 0.69856 |
| 5 | GridSearch Optimization | **0.78229** |

---

## 🧠 Key Takeaways

- Proper handling of categorical variables significantly improved performance.
- Feature engineering had a greater impact than increasing model complexity.
- More complex models do not necessarily guarantee better generalization.
- Hyperparameter tuning can substantially enhance model performance.
- Structured experimentation improves clarity and model development efficiency.

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- ydata-profiling

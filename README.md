# Employee Attrition Prediction

This project aims to predict employee attrition using machine learning techniques. The focus is on building a clear, interpretable, and well-structured step-by-step workflow rather than relying on complex or black-box models.

## Approach

### 1. Exploratory Data Analysis (EDA)

* Checked data structure, distributions, and summary statistics
* Visualized numerical and categorical features
* Identified class imbalance in the target variable

### 2. Data Preprocessing

* Removed non-informative features
* One-hot encoding for categorical variables
* Verified absence of missing values

### 3. Feature Engineering

* Created **IncomePerYear** from MonthlyIncome
* Combined satisfaction-related variables into **TotalSatisfaction**

### 4. Handling Class Imbalance

* Applied **random oversampling** to balance the minority class

### 5. Feature Selection

* Used Sequential Feature Selector (forward selection)
* Optimized using F1-score

### 6. Model

* Logistic Regression (no advanced models used)
#### Rationale: Focus on interpretability, simplicity, and understanding feature effects.

### 7. Threshold Optimization

* Tuned classification threshold to maximize F1-score

### 8. Evaluation

* Accuracy, Precision, Recall, F1-score
* Confusion Matrix
* ROC-AUC Score

## Key Insights
* Distance from home strongly increases attrition risk
* Higher income reduces likelihood of leaving
* Work-life balance plays a significant role in retention
* Overtime is associated with higher attrition

# Employee Attrition Prediction
This project aims to predict employee attrition using machine learning techniques. The focus is on building a clear, interpretable, and well-structured workflow using statistical reasoning and model transparency rather than complex black-box models.

## Approach
### 1. Exploratory Data Analysis (EDA)

- Examined dataset structure and summary statistics  
- Visualized distributions of numerical and categorical variables  
- Identified **severe class imbalance** in the target variable (Attrition)  
- Observed weak correlations between predictors  

### 2. Data Preprocessing

- Removed non-informative feature (**EmployeeID**)  
- Applied **one-hot encoding** to categorical variables  
- Aligned train and test datasets to ensure consistent features  
- Confirmed absence of missing values  

### 3. Feature Engineering

- Created **IncomePerYear** from MonthlyIncome  
- Constructed **TotalSatisfaction** by combining:
  - Job Satisfaction  
  - Environment Satisfaction  
  - Relationship Satisfaction  
- Dropped redundant variables to reduce multicollinearity  

### 4. Handling Class Imbalance

- Used **class_weight = 'balanced'** in Logistic Regression  
- This assigns higher importance to the minority class based on inverse frequency  

### 5. Feature Selection

- Applied **Sequential Feature Selector (Forward Selection)**  
- Selected **top 10 features**  
- Optimized using **F1-score with 5-fold cross-validation**  

### 6. Model

- **Logistic Regression (no regularization)**  

**Rationale:**  
Focus on interpretability, simplicity, and understanding the impact of predictors on attrition.

### 7. Threshold Optimization

- Tuned classification threshold (0.3 – 0.7 range)  
- Selected optimal threshold based on **maximum F1-score**  

### 8. Evaluation

- Accuracy, Precision, Recall, F1-score  
- Confusion Matrix  
- ROC-AUC Score  

**Key Results:**
- Accuracy: **90%** (misleading due to imbalance)  
- F1-score (minority class): **0.15**  
- ROC-AUC: **0.737** → reasonable discrimination ability  

## Model Interpretation
- Converted coefficients to **odds ratios** for interpretability  
- Identified key drivers of attrition  

## Key Insights
- **Distance from home** significantly increases attrition risk  
- **Overtime** strongly increases likelihood of leaving  
- **Work-life balance** reduces attrition probability  
- **Training frequency** improves employee retention  
- Some job roles show higher turnover patterns  

## Output
Final predictions are saved as: 

## Author
Fazra Farook  
BSc (Hons) in Applied Statistics - University of Colombo

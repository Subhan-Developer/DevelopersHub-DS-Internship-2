# Task 1: Term Deposit Subscription Prediction

## Objective
Predict whether a bank customer will subscribe to a term deposit based on marketing campaign data.

## Dataset
- **Source**: Bank Marketing Dataset (UCI)
- **Samples**: 5,000 customers
- **Features**: Age, job, marital status, education, balance, housing loan, contact method, campaign details, etc.
- **Target**: deposit (1 = subscribed, 0 = not subscribed)

## Approach

### 1. Data Preprocessing
- Handled missing values
- Encoded categorical variables using LabelEncoder
- Scaled numerical features using StandardScaler

### 2. Exploratory Data Analysis
Created visualizations to understand:
- Age, balance, and job impact on subscription
- Monthly trends in subscription rates
- Correlation between features

### 3. Models Trained
| Model | Accuracy | F1-Score | AUC-ROC |
|-------|----------|----------|---------|
| Logistic Regression | ~80% | ~0.75 | ~0.85 |
| Random Forest | ~82% | ~0.78 | ~0.87 |

### 4. Model Evaluation
- Confusion Matrix
- ROC Curves
- Cross-validation (5-fold)

### 5. Explainable AI (SHAP)
Used SHAP to explain 5 individual predictions, showing:
- Which features increased deposit likelihood
- Which features decreased deposit likelihood

## Key Findings

1. **Age matters**: Younger customers (25-35) are more likely to subscribe
2. **Balance is crucial**: Higher account balance correlates with subscription
3. **Previous campaigns**: Success in previous campaigns increases likelihood
4. **Call duration**: Longer calls indicate higher engagement and subscription
5. **Job type**: Management and technician roles show higher rates

## Business Recommendations

- ✅ Target younger demographics with personalized offers
- ✅ Focus on customers with high account balances
- ✅ Follow up on previous successful campaign contacts
- ✅ Train sales team for longer, quality conversations
- ✅ Prioritize marketing budget on high-potential segments

## Technologies Used
- Python 3.13
- pandas, numpy (data manipulation)
- matplotlib, seaborn (visualization)
- scikit-learn (models, metrics)
- SHAP (model explainability)

## Files in This Task
- `Task1_Bank_Marketing.ipynb` - Complete analysis and modeling
- `README.md` - This documentation

## How to Run
```bash
# Install requirements
pip install pandas numpy matplotlib seaborn scikit-learn shap

# Run Jupyter notebook
jupyter notebook Task1_Bank_Marketing.ipynb
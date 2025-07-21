# Personal Loan Acceptance Prediction

## Objective

The objective of this project is to **predict which customers are likely to accept a personal loan offer** based on their demographic and financial information. The analysis aims to support marketing strategies by identifying key customer segments more likely to respond positively to promotional campaigns.

---

## Dataset

- **Source:** Bank Marketing Dataset from the UCI Machine Learning Repository.
- **Format:** CSV file named `bank.csv`.
- **Target Variable:** `deposit` — indicates whether the customer has subscribed to a term deposit (`yes` or `no`).

---

## Key Features Explored

During initial exploration, we focused on the following features:

- `age`: Customer’s age
- `job`: Type of job (e.g., admin., technician, services)
- `marital`: Marital status (e.g., married, single, divorced)

Other relevant features used during training:

- `education`, `balance`, `housing`, `loan`, `contact`, `duration`, `campaign`, `pdays`, `previous`, `poutcome`

---

## Data Preprocessing

- The `deposit` column was **encoded into binary format**:
  - `yes` → 1
  - `no` → 0

- **Categorical features** like `job`, `marital`, and `age` were encoded using **Label Encoding**.

- **Age Grouping**:
  - Age was grouped into custom bins such as:
    - `Under_25`, `26-35`, `36-45`, `46-55`, `56-65`, `Above_65`

---

## Exploratory Data Analysis (EDA)

### Univariate Analysis

- Value counts and distributions of categorical features (`job`, `marital`, `age`) were explored to understand dataset balance.

### Bivariate Analysis with Target

- Bar plots were created to analyze the acceptance rate (`deposit`) based on:
  - **Job Type**
  - **Marital Status**
  - **Age Groups**

These visualizations helped identify patterns among customer types.

---

## Model Training

### Logistic Regression

- A **Logistic Regression classifier** was trained on the processed dataset to predict customer loan acceptance.

---

### Decision Tree (Extension)

- A Decision Tree model was also trained on the same data for comparison with logistic regression.

---

## Model Evaluation

Evaluation was done using the following metrics:

- **Accuracy Score**: Percentage of correct predictions
- **Confusion Matrix**: Displays true positives, true negatives, false positives, and false negatives

---

## Visual Analysis

Several visualizations were produced to understand customer group trends:

- **Job Type**:
  - Higher acceptance rates were observed among:
    - Students
    - Retired individuals
    - Unemployed

- **Marital Status**:
  - Single customers were more likely to accept the loan offer compared to married or divorced individuals

- **Age Group**:
  - Customers in the age range **60+** had the highest acceptance rates

These visual patterns supported and explained the behavior captured by the predictive models.

---

## Conclusion

The project successfully predicted which customer groups are more likely to accept a personal loan offer, providing clear actionable insights for marketing teams.

---

## Key Insights

- **Age**: Customers aged **60+** are the most receptive
- **Job**: Students, retired individuals, and unemployed are more likely to accept
- **Marital Status**: Single individuals show a slightly higher tendency to accept offers

These patterns can help businesses tailor their marketing strategies and target the right audience more effectively.

---

## Future Improvements

- Implement and compare advanced models:
  - **Random Forest**
  - **XGBoost**
- Apply balancing techniques (e.g., **SMOTE**) if class imbalance exists
- Use **hyperparameter tuning** (e.g., GridSearchCV) to enhance model performance
- Include **feature importance plots** to interpret model decisions better

---



# Customer Churn Analysis for a Telecommunications Company  

## Project Overview  

This project involves an in-depth analysis of customer churn for a telecommunications company. The primary objective is to identify the factors contributing to customer churn and develop predictive models to forecast which customers are at risk of leaving.  

### Goals of the Analysis:  
- **Perform Exploratory Data Analysis (EDA)**: Identify patterns, correlations, and trends in the data.  
- **Data Preprocessing**: Clean the dataset by handling missing values, encoding categorical variables, and detecting outliers.  
- **Predictive Modeling**: Build models using Logistic Regression, Random Forest, and XGBoost to predict customer churn.  
- **Model Evaluation**: Assess the performance of models using metrics like accuracy, precision, recall, and F1-score.  
- **Derive Insights**: Provide actionable insights for improving customer retention strategies.  

---

## Dataset  

The dataset used in this analysis is publicly available and includes customer demographics, account details, services used, and churn status.  

### Key Features:  
- **customerID**: Unique customer identifier  
- **gender**: Gender of the customer  
- **SeniorCitizen**: Indicates if the customer is a senior citizen (1 or 0)  
- **Partner**: Whether the customer has a partner (Yes/No)  
- **Dependents**: Indicates if the customer has dependents (Yes/No)  
- **tenure**: Duration (in months) of the customer with the company  
- **PhoneService**: Whether the customer has phone service (Yes/No)  
- **MultipleLines**: Indicates if the customer has multiple lines (Yes/No/No phone service)  
- **InternetService**: Type of internet service (DSL/Fiber optic/No)  
- **OnlineSecurity**: Whether online security services are active (Yes/No/No internet service)  
- **Churn**: Target variable indicating if the customer churned (Yes/No)  

---

## Analysis Process  

### 1. **Data Cleaning and Preprocessing**  
- Missing values in the `TotalCharges` column were replaced with `0`, as they correspond to customers with a tenure of 0 months.  
- Binary categorical features (e.g., `gender`, `Partner`) were label-encoded.  
- Multiclass categorical feature (e.g., `PaymentMethod`) was one-hot encoded.   

### 2. **Exploratory Data Analysis (EDA)**  
- Generated visualizations to identify trends and patterns:  
  - **Churn Rate Analysis**: Compared churn rates across categories like `gender` and `PaymentMethod`.  
  - **Correlation Heatmap**: Highlighted relationships between numerical features and the `Churn` target variable.  
- Derived insights such as the impact of contract type and tenure on churn rates.  

### 3. **Modeling and Evaluation**  
- Built predictive models using:  
  - **Logistic Regression**  
  - **Random Forest Classifier**  
  - **XGBoost Classifier**
  - **Naive Bayes** 
- Evaluated models using metrics such as:  
  - Accuracy  
  - Precision  
  - Recall  
  - F1-Score  

### 4. **Insights and Recommendations**  
- Customers with longer tenures and contract types like two-year plans are less likely to churn.  
- Senior citizens and customers without dependents show higher churn rates, suggesting the need for targeted retention strategies.  

---

## Results  

After hyperparameter tuning, the performance metrics for the models were as follows:
- **Random Forest Classifier** performed well after hyperparameter tuning, achieving the following metrics:  
  - **Accuracy**: 75%  
  - **Precision (0)**: 88%  
  - **Recall (0)**: 77%  
  - **F1-Score (0)**: 82%  
  - **Precision (1)**: 52%  
  - **Recall (1)**: 72%  
  - **F1-Score (1)**: 61%  
  - **ROC AUC**: 83%  

- **XGBoost Classifier** also showed strong performance after hyperparameter tuning with the following results:  
  - **Accuracy**: 71%  
  - **Precision (0)**: 91%  
  - **Recall (0)**: 67%  
  - **F1-Score (0)**: 77%  
  - **Precision (1)**: 47%  
  - **Recall (1)**: 81%  
  - **F1-Score (1)**: 59%  
  - **ROC AUC**: 82%  
- The **ROC AUC** scores for all models were consistently high, indicating reliable discrimination between churned and non-churned customers.

---

## Limitations  

- The dataset does not account for external factors such as market competition or economic conditions.    
- Further feature engineering may improve model performance.  

---

## Future Work  

- Incorporate additional external datasets to provide a holistic analysis.  
- Develop a more robust feature engineering pipeline to capture non-linear relationships.  
- Explore advanced machine learning models, such as neural networks, for improved churn prediction.  

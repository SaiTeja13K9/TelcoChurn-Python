# Customer Churn Prediction for Telco

## 📌 Project Overview
This project focuses on analyzing and predicting customer churn for a telecommunications company using the **Telco Customer Churn dataset**. The goal is to **identify key factors that contribute to customer churn** and build predictive models to **assist in targeted customer retention strategies**.

## 🔥 Motivation
Customer churn significantly affects business profitability. Identifying the most influential factors behind churn and accurately predicting customer attrition can help businesses develop proactive retention strategies. This project aims to answer:
- **What factors influence customer churn the most?**
- **How accurately can we predict customer churn using available data?**

## 📊 Dataset Description
The **Telco Customer Churn dataset** consists of **7,043 rows** and **21 columns**, including:
- **Demographic Variables**: Gender, SeniorCitizen, Partner, Dependents.
- **Subscription Details**: InternetService, Contract Type, PaymentMethod.
- **Financial Metrics**: MonthlyCharges, TotalCharges.
- **Target Variable**: Churn (Yes/No).

## 🔧 Data Preparation Steps
To ensure data consistency and improve model performance, the following preprocessing steps were performed:
- **Handling Missing Values**: Filled missing values in the `TotalCharges` column with mean values.
- **Standardizing Values**: Replaced inconsistent values (e.g., "No Internet Service") with a standard format.
- **Feature Engineering**:
  - Created `tenure_group` (grouping customers based on tenure periods).
  - Generated `TotalServices` (total number of services subscribed).
  - Converted `SeniorCitizen` and other features into appropriate numerical or categorical types.
- **Feature Scaling**: Applied standard scaling to numerical variables (`MonthlyCharges`, `TotalCharges`) for model consistency.

## 📊 Exploratory Data Analysis (EDA)
Key insights from the EDA:
- **Churn Rate**: ~26% of customers in the dataset had churned.
- **Tenure & Churn**: Customers with shorter tenures (~18 months) are more likely to churn.
- **Contract Type & Churn**: Month-to-month contracts have the highest churn rate.
- **Financial Factors**: Higher monthly charges correlate with higher churn rates.
- **Service Bundling**: Customers subscribing to bundled services are less likely to churn.

## 🔍 Machine Learning Models
The following models were built and evaluated:

### 1️⃣ **Logistic Regression**
- **AUC-ROC Score**: 0.84
- **Key Findings**:
  - Good separation between churned and non-churned customers.
  - Higher precision for non-churn cases but lower recall for churn cases.

### 2️⃣ **Random Forest Classifier**
- **AUC-ROC Score**: 0.82
- **Key Findings**:
  - Strong performance in identifying important features.
  - Slightly lower recall for churned customers compared to Logistic Regression.

## 🔑 Key Findings & Managerial Implications
- **High-risk churn customers** have **short tenures**, **high monthly charges**, and **month-to-month contracts**.
- **Contract-based retention strategies** (shifting customers to one-year or two-year contracts) can **reduce churn**.
- **Bundled services** encourage customer retention.
- **Predictive modeling** helps identify at-risk customers, allowing proactive engagement strategies.

## 🛠 Technologies Used
- **Programming Languages**: Python
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- **Machine Learning Models**: Logistic Regression, Random Forest
- **Visualization Tools**: Matplotlib, Seaborn

## 📂 Project Structure
```
📁 Customer-Churn-Prediction
│── 📄 README.md              # Project documentation
│── 📄 Final_Project_5110_Group_13.ipynb  # Jupyter Notebook with code
│── 📄 BCIS_5110_Final_Project_Report.pdf # Detailed project report
│── 📁 data                  # Folder containing datasets
│── 📁 images                # Visualizations and plots
```

## 📌 Next Steps
- **Improve feature engineering** by exploring additional customer interaction metrics.
- **Optimize machine learning models** by tuning hyperparameters.
- **Explore deep learning approaches** (e.g., Neural Networks) for improved churn prediction.
- **Deploy the model** as a web application or API for real-time customer churn predictions.

## 📜 References
- **Dataset**: [Telco Customer Churn - Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Machine Learning Techniques**: Scikit-learn documentation
- **Feature Engineering & EDA**: Python libraries Pandas, Seaborn

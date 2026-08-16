# Customer Churn Prediction Using Data Mining and Machine Learning

## Project Overview

Customer churn is a major challenge for telecom companies. When customers stop using a company's services and move to another provider, it is known as **customer churn**.

This project develops a **machine learning-based Customer Churn Prediction system** that analyzes telecom customer information and predicts whether a customer is likely to **churn (leave)** or **stay** with the company.

The project combines **Data Mining, Exploratory Data Analysis, Data Preprocessing, and Machine Learning Classification** techniques to identify patterns associated with customer churn.

The system also compares multiple machine learning algorithms and identifies the important customer characteristics that contribute to churn prediction.

---

## Project Objective

The main objectives of this project are:

* To analyze telecom customer behavior.
* To identify patterns associated with customer churn.
* To preprocess and transform customer data for machine learning.
* To build classification models for predicting customer churn.
* To compare different machine learning algorithms.
* To evaluate models using multiple performance metrics.
* To identify important features influencing churn predictions.
* To provide customer-level churn predictions.
* To provide useful business recommendations for customer retention.

---

## Dataset

The project uses the **Telco Customer Churn Dataset**.

The dataset contains information about approximately **7,043 telecom customers** and includes customer account, service, and demographic information.

### Important Features

| Feature           | Description                                             |
| ----------------- | ------------------------------------------------------- |
| `customerID`      | Unique customer identifier                              |
| `gender`          | Customer gender                                         |
| `SeniorCitizen`   | Indicates whether the customer is a senior citizen      |
| `Partner`         | Whether the customer has a partner                      |
| `Dependents`      | Whether the customer has dependents                     |
| `tenure`          | Number of months the customer has used the service      |
| `PhoneService`    | Whether the customer has phone service                  |
| `InternetService` | Type of internet service                                |
| `Contract`        | Type of customer contract                               |
| `PaymentMethod`   | Customer payment method                                 |
| `MonthlyCharges`  | Monthly amount charged to the customer                  |
| `TotalCharges`    | Total amount charged to the customer                    |
| `Churn`           | Target variable indicating whether the customer churned |

### Target Variable

The target variable is:

`Churn`

It is converted into:

* `0` → Customer stayed
* `1` → Customer churned

---

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Google Colab / Jupyter Notebook**
* **GitHub**

---

# Project Workflow

## 1. Data Collection

The Telco Customer Churn dataset is loaded into the Python environment using Pandas.

The dataset contains customer information that can be used to understand and predict churn behavior.

---

## 2. Data Understanding

The dataset is analyzed using:

* Dataset shape
* Column information
* Data types
* Statistical summary
* Unique values
* Missing-value analysis
* Duplicate-value analysis

This step helps understand the structure and quality of the dataset before applying machine learning.

---

## 3. Data Preprocessing

The following preprocessing steps are performed:

### Customer ID Removal

The `customerID` column is removed because it is only an identifier and does not provide meaningful information for predicting churn.

### Handling Missing Values

The `TotalCharges` column is converted into a numerical format.

Any missing values are handled using the median value.

### Target Encoding

The `Churn` column is converted into numerical values:

```text
No  → 0
Yes → 1
```

### Categorical Encoding

Categorical features are converted into numerical representations using **One-Hot Encoding** so that machine learning algorithms can process them.

---

## 4. Exploratory Data Analysis

Exploratory Data Analysis (EDA) is performed to understand customer behavior and identify patterns related to churn.

The project analyzes:

* Overall churn distribution
* Contract type vs churn
* Internet service vs churn
* Payment method vs churn
* Tenure vs churn
* Monthly charges vs churn
* Total charges vs churn
* Correlation between numerical features

Visualizations are created using **Matplotlib and Seaborn**.

---

## 5. Feature Selection

The dataset is divided into:

### Input Features (X)

Customer characteristics such as:

* Tenure
* Contract
* Internet Service
* Monthly Charges
* Total Charges
* Payment Method
* And other available customer attributes

### Target Variable (y)

```text
Churn
```

The objective is to predict the target variable using the available customer features.

---

## 6. Train-Test Split

The dataset is divided into:

* **80% Training Data**
* **20% Testing Data**

The training data is used to train the machine learning models, while the testing data is used to evaluate their performance on previously unseen customers.

Stratified splitting is used to maintain the proportion of churned and non-churned customers in the training and testing datasets.

---

# Machine Learning Models

Three classification algorithms are implemented and compared.

## 1. Logistic Regression

Logistic Regression is used as a baseline classification model.

It estimates the probability that a customer belongs to the churn or non-churn class.

---

## 2. Decision Tree Classifier

A Decision Tree creates a sequence of decision rules based on customer characteristics.

For example, the model may learn patterns involving:

```text
Contract
   ↓
Tenure
   ↓
Monthly Charges
   ↓
Churn Prediction
```

Decision Trees are also relatively easy to interpret.

---

## 3. Random Forest Classifier

Random Forest combines multiple Decision Trees to produce a more robust prediction.

Multiple trees make predictions independently, and their results are combined to produce the final classification.

Random Forest is also used to determine feature importance.

---

# Model Evaluation

The models are evaluated using multiple performance metrics.

## Accuracy

Measures the percentage of total predictions that are correct.

```text
Accuracy =
Correct Predictions / Total Predictions
```

---

## Precision

Precision measures how many customers predicted as churners actually churned.

---

## Recall

Recall measures how many of the customers who actually churned were correctly identified by the model.

Recall is particularly important in churn prediction because failing to identify a customer who is likely to leave may result in a lost customer.

---

## F1-Score

F1-score provides a balance between precision and recall.

It is useful when both false positives and false negatives need to be considered.

---

## ROC-AUC

ROC-AUC measures the model's ability to distinguish between churned and non-churned customers.

A higher ROC-AUC generally indicates better classification performance.

---

## Confusion Matrix

A confusion matrix is used to visualize:

* True Positives
* True Negatives
* False Positives
* False Negatives

This provides a detailed view of the model's correct and incorrect predictions.

---

# Model Comparison

The performance of the three models is compared using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

The model with the strongest overall performance based on the selected evaluation criteria is identified as the best-performing model.

The actual performance values are generated directly by the notebook and should be used when presenting the project.

---

# Feature Importance

Random Forest feature importance is used to identify which customer characteristics contribute most to the model's predictions.

Important predictive features may include variables related to:

* Contract type
* Tenure
* Monthly charges
* Total charges
* Internet service
* Payment method

Feature importance indicates which variables the model relies on most for prediction. It does not necessarily mean that a feature directly causes customer churn.

---

# Customer-Level Churn Prediction

The project also provides a customer-level prediction function.

A customer's information can be provided to the trained model, including:

* Tenure
* Monthly charges
* Total charges
* Contract type
* Internet service
* Payment method

The system then produces:

```text
Churn Prediction
+
Churn Probability
```

For example:

```text
Customer is likely to CHURN

Churn Probability: XX%
```

The exact probability is generated by the trained machine learning model.

---

# Business Insights

The analysis can help telecom companies understand customer churn behavior.

Potential observations include:

* Month-to-month customers may have higher churn rates than customers with longer contracts.
* Customers with shorter tenure may have a higher likelihood of churn.
* Monthly charges can be associated with differences in churn behavior.
* Internet service type can provide useful information for churn prediction.
* Payment method can also provide predictive information.

These patterns can help businesses identify customers who may require additional attention.

---

# Business Recommendations

Based on the analysis, telecom companies can:

1. Identify customers with high churn probability.
2. Provide personalized retention offers.
3. Encourage month-to-month customers to move to longer-term contracts.
4. Provide special offers to newer customers.
5. Improve customer support for high-risk customers.
6. Analyze pricing and service plans for customers with high churn probability.
7. Use machine learning predictions as part of a customer retention strategy.

---

# Project Architecture

```text
                 Telecom Customer Dataset
                           |
                           ↓
                  Data Preprocessing
                           |
                           ↓
                Exploratory Data Analysis
                           |
                           ↓
                    Feature Encoding
                           |
                           ↓
                    Train/Test Split
                           |
             ┌─────────────┼─────────────┐
             ↓             ↓             ↓
       Logistic        Decision       Random
       Regression        Tree          Forest
             ↓             ↓             ↓
             └─────────────┼─────────────┘
                           ↓
                    Model Evaluation
                           |
                           ↓
                   Model Comparison
                           |
                           ↓
                    Best Performing
                        Model
                           |
             ┌─────────────┴─────────────┐
             ↓                           ↓
       Churn Prediction           Feature Importance
             ↓
       Business Insights
             ↓
       Customer Retention
```

---

# Project Structure

```text
Customer-Churn-Prediction/
│
├── Customer_Churn_Prediction.ipynb
│
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
│
└── README.md
```

### File Description

**`Customer_Churn_Prediction.ipynb`**

Contains the complete Python implementation, including data preprocessing, visualization, model training, evaluation, and customer-level prediction.

**`WA_Fn-UseC_-Telco-Customer-Churn.csv`**

Contains the Telco Customer Churn dataset used for the project.

**`README.md`**

Contains project documentation, methodology, technologies, results, and business insights.

---

# How to Run the Project

## Option 1 — Google Colab

1. Open Google Colab.
2. Upload `Customer_Churn_Prediction.ipynb`.
3. Upload `WA_Fn-UseC_-Telco-Customer-Churn.csv` when requested by the notebook.
4. Run the notebook cells sequentially.
5. Review the visualizations and model evaluation results.

## Option 2 — Jupyter Notebook

1. Install Python.
2. Install the required libraries.
3. Place the notebook and CSV dataset in the same folder.
4. Open the notebook using Jupyter Notebook.
5. Run the cells sequentially.

---

# Key Learning Outcomes

Through this project, the following concepts were implemented:

* Data collection
* Data cleaning
* Missing-value handling
* Exploratory Data Analysis
* Data visualization
* Feature engineering
* Categorical encoding
* Train-test splitting
* Feature scaling
* Classification algorithms
* Logistic Regression
* Decision Trees
* Random Forest
* Model evaluation
* Confusion matrix
* ROC-AUC
* Feature importance
* Customer-level prediction
* Business interpretation of machine learning results

---

# Future Improvements

The project can be further improved by:

* Hyperparameter tuning using GridSearchCV or RandomizedSearchCV
* Implementing XGBoost
* Handling class imbalance using techniques such as SMOTE
* Developing a web application for real-time predictions
* Deploying the model using Flask or FastAPI
* Creating an interactive Power BI dashboard
* Integrating the prediction system with a telecom CRM system
* Monitoring model performance using new customer data

---

# Conclusion

This project demonstrates how **Data Mining and Machine Learning** can be used to analyze telecom customer behavior and predict customer churn.

By analyzing customer characteristics and comparing multiple classification algorithms, the system can identify customers who are more likely to leave the service.

The predictions can help telecom companies take proactive retention measures, improve customer satisfaction, and potentially reduce customer loss.

---

# Author

**Geetha**

**B.Tech – Computer Science and Engineering**

**Data Analytics and Visualization**

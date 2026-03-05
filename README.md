# Customer Churn Prediction using Data Mining

## Project Overview
Customer churn prediction is an important task for businesses to identify customers who are likely to stop using their services. In this project, a machine learning model is built to analyze telecom customer data and predict whether a customer will churn or not.

This project demonstrates the application of data mining techniques and machine learning algorithms for customer behavior analysis.

---

## Objective
The main objective of this project is to build a predictive model that can identify customers who are likely to leave the service based on their usage patterns and account information.

---

## Technologies Used
- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook / Google Colab

---

## Dataset
The dataset used is the **Telco Customer Churn Dataset**.

It contains information such as:
- Customer ID
- Gender
- Tenure
- Internet Service
- Monthly Charges
- Contract Type
- Payment Method
- Churn (Target Variable)

---

## Project Workflow

### 1. Data Collection
The telecom customer churn dataset is loaded using the Pandas library.

### 2. Data Preprocessing
- Removed unnecessary columns (CustomerID)
- Converted categorical data into numerical format using Label Encoding
- Checked for missing values

### 3. Feature Selection
Input features (X) and target variable (Y) were defined.

### 4. Data Splitting
The dataset was split into:
- Training Data (80%)
- Testing Data (20%)

### 5. Model Building
A **Decision Tree Classifier** was used to train the machine learning model.

### 6. Prediction
The trained model predicts whether customers will churn or stay.

### 7. Model Evaluation
The model performance was evaluated using:
- Accuracy Score
- Classification Report

### 8. Data Visualization
A bar chart was used to visualize churn distribution among customers.

---

## Results
The model successfully predicts customer churn with good accuracy and provides insights into customer behavior patterns.

---

## Project Structure
Customer-Churn-Prediction
│
├── churn_prediction.ipynb
├── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── README.md


---

## How to Run the Project

1. Download or clone the repository


git clone https://github.com/your-username/customer-churn-prediction.git


2. Open the notebook in Jupyter Notebook or Google Colab

3. Run all cells step by step

---

## Resume Description

Developed a Customer Churn Prediction model using Decision Tree algorithm to analyze telecom customer behavior and predict churn using Python, Pandas, and Scikit-learn.

---

## Future Improvements
- Apply advanced models like Random Forest and XGBoost
- Improve model accuracy using feature engineering
- Deploy the model using a web application

---

## Author
Geetha

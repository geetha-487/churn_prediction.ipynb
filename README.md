# 📡 Quantum-Enhanced Telecom Customer Churn Prediction

## 🚀 Project Overview

**Quantum-Enhanced Telecom Customer Churn Prediction** is an advanced machine learning project that predicts the probability of a telecom customer leaving a service provider (**customer churn**).

The project combines:

* 📊 Telecom customer data
* 🧹 Data preprocessing
* 🎯 Feature selection
* ⚛️ **4-Qubit Quantum Circuit**
* 🧠 **Variational Quantum Classifier (VQC)**
* ⚙️ **Classical Adam Optimizer**
* 📈 Churn probability prediction
* 🔍 **SHAP Explainable AI**

The main objective is to explore how **Quantum Machine Learning (QML)** can be integrated with classical machine-learning techniques to create an interpretable customer churn prediction system.

---

## 🔄 Project Workflow

```text
Telecom Data
     ↓
Preprocessing
     ↓
Feature Selection
     ↓
4 Selected Features
     ↓
4-Qubit Quantum Circuit
     ↓
Variational Quantum Classifier (VQC)
     ↓
Classical Adam Optimizer
     ↓
Churn Probability
     ↓
SHAP Explainable AI
```

---

## 💡 Why Quantum Machine Learning?

Traditional churn prediction systems generally rely on classical algorithms such as:

* Logistic Regression
* Decision Trees
* Random Forest
* Support Vector Machines
* Neural Networks

This project introduces a **Quantum Machine Learning approach** by encoding selected customer features into a **4-qubit quantum circuit** and using a **Variational Quantum Classifier (VQC)** for classification.

The quantum circuit provides an experimental framework for investigating the application of quantum computing techniques to telecom churn prediction.

> **Note:** The project explores the application of quantum machine learning; it does not assume that the quantum model will automatically outperform classical machine-learning models.

---

## 🧩 Methodology

### 1. 📡 Telecom Dataset

The system takes telecom customer information such as:

* Customer demographics
* Account information
* Service usage
* Contract details
* Payment information
* Monthly charges
* Tenure
* Churn status

The target variable represents whether a customer has churned.

---

### 2. 🧹 Data Preprocessing

The raw telecom data is prepared before being passed to the quantum model.

Preprocessing may include:

* Handling missing values
* Removing unnecessary columns
* Encoding categorical variables
* Converting target labels
* Feature scaling
* Preparing training and testing datasets

---

### 3. 🎯 Feature Selection

Relevant customer attributes are selected to reduce the dimensionality of the input.

The final pipeline uses:

```text
4 Selected Features
        ↓
4 Qubits
```

Each selected feature is mapped to a corresponding quantum qubit.

This creates a direct relationship between the classical input features and the quantum circuit.

---

## ⚛️ 4-Qubit Quantum Circuit

The selected four features are encoded into a **4-qubit quantum circuit**.

Conceptually:

```text
Feature 1 ──► Qubit 1 ──┐
Feature 2 ──► Qubit 2 ──┤
Feature 3 ──► Qubit 3 ──┤──► Variational Circuit ──► Measurement
Feature 4 ──► Qubit 4 ──┘
```

The circuit applies parameterized quantum operations to transform the encoded information before measurement.

---

## 🧠 Variational Quantum Classifier (VQC)

The project uses a **Variational Quantum Classifier (VQC)** for churn classification.

The VQC consists of:

* Feature encoding
* Parameterized quantum gates
* Variational layers
* Quantum measurements
* Classical optimization

The parameters of the quantum circuit are optimized during training to minimize the classification loss.

---

## ⚙️ Classical Adam Optimizer

The quantum circuit parameters are optimized using the **Adam optimizer**.

```text
Quantum Circuit
       ↓
Prediction
       ↓
Loss Calculation
       ↓
Adam Optimizer
       ↓
Updated Parameters
       ↓
Quantum Circuit
```

This hybrid structure combines:

**Quantum computation + Classical optimization**

---

## 📈 Churn Probability

Instead of only producing a binary churn label, the system generates a **churn probability**.

Example:

```text
Customer
   ↓
Quantum Model
   ↓
Churn Probability = 0.82
   ↓
82% estimated probability of churn
```

This probability can be used to identify customers who may require retention strategies.

---

## 🔍 SHAP Explainable AI

To make the model more interpretable, the project incorporates **SHAP (SHapley Additive exPlanations)**.

SHAP helps explain how individual input features contribute to a model's prediction.

Example:

```text
Customer Churn Probability
          ↓
       SHAP
          ↓
 ┌─────────────────────┐
 │ Feature 1    +0.31  │
 │ Feature 2    -0.12  │
 │ Feature 3    +0.24  │
 │ Feature 4    +0.08  │
 └─────────────────────┘
```

This allows users to understand **which selected customer characteristics contributed to the prediction**.

---

## 🏗️ System Architecture

```text
                ┌───────────────────┐
                │   Telecom Data    │
                └─────────┬─────────┘
                          ↓
                ┌───────────────────┐
                │  Preprocessing    │
                └─────────┬─────────┘
                          ↓
                ┌───────────────────┐
                │ Feature Selection │
                └─────────┬─────────┘
                          ↓
                ┌───────────────────┐
                │ 4 Selected        │
                │ Features          │
                └─────────┬─────────┘
                          ↓
                ┌───────────────────┐
                │ 4-Qubit Quantum   │
                │ Circuit            │
                └─────────┬─────────┘
                          ↓
                ┌───────────────────┐
                │       VQC         │
                └─────────┬─────────┘
                          ↓
                ┌───────────────────┐
                │ Adam Optimizer    │
                └─────────┬─────────┘
                          ↓
                ┌───────────────────┐
                │ Churn Probability │
                └─────────┬─────────┘
                          ↓
                ┌───────────────────┐
                │ SHAP Explainable  │
                │ AI                │
                └───────────────────┘
```

---

## 🛠️ Technologies Used

| Technology           | Purpose                                  |
| -------------------- | ---------------------------------------- |
| Python               | Core implementation                      |
| Pandas               | Data processing                          |
| NumPy                | Numerical computation                    |
| Scikit-learn         | Preprocessing and classical ML utilities |
| Quantum ML Framework | Quantum circuit and VQC implementation   |
| Adam Optimizer       | Parameter optimization                   |
| SHAP                 | Explainable AI                           |
| Matplotlib           | Visualization                            |
| Jupyter Notebook     | Development and experimentation          |
| Git & GitHub         | Version control                          |

---

## 📁 Project Structure

```text
quantum-telecom-churn/
│
├── data/
│   └── telecom_data.csv
│
├── notebooks/
│   └── quantum_churn_prediction.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── feature_selection.py
│   ├── quantum_model.py
│   ├── training.py
│   └── explainability.py
│
├── results/
│   ├── model_results/
│   └── shap_plots/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ▶️ Installation

Clone the repository:

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

Move into the project directory:

```bash
cd quantum-telecom-churn
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🚀 Running the Project

If the implementation is provided as a Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
notebooks/quantum_churn_prediction.ipynb
```

Run the notebook cells sequentially:

```text
Load Dataset
     ↓
Preprocess Data
     ↓
Select Features
     ↓
Encode Features
     ↓
Construct 4-Qubit Circuit
     ↓
Train VQC
     ↓
Optimize Parameters
     ↓
Predict Churn Probability
     ↓
Generate SHAP Explanations
```

---

## 📊 Expected Output

The system produces:

### Model Output

```text
Customer ID: XXXXX
Churn Probability: 0.82
Prediction: Churn
```

### Explainability Output

SHAP visualizations can be generated to show the contribution of each selected feature to the prediction.

---

## 🌟 Key Features

* ⚛️ **Quantum Machine Learning**
* 🔹 4-Qubit Quantum Circuit
* 🧠 Variational Quantum Classifier
* ⚙️ Adam-based optimization
* 📊 Telecom churn prediction
* 📈 Probability-based prediction
* 🔍 SHAP Explainable AI
* 🔄 Hybrid quantum-classical workflow
* 📉 Feature selection and dimensionality reduction

---

## 💡 Innovation

The project introduces a **hybrid quantum-classical architecture** for telecom customer churn prediction.

The key innovation is the integration of:

```text
Classical Telecom Data
        +
Feature Selection
        +
4-Qubit Quantum Circuit
        +
Variational Quantum Classifier
        +
Classical Optimization
        +
Explainable AI
```

Rather than using a conventional classification pipeline alone, the project investigates the use of a **variational quantum model** while retaining classical preprocessing, optimization, and explainability techniques.

---

## 🆕 Novelty

The project combines multiple techniques into a single churn-prediction pipeline:

1. **Dimensionality reduction to four relevant features**
2. **Four-feature-to-four-qubit mapping**
3. **Variational quantum classification**
4. **Classical Adam optimization of quantum parameters**
5. **Probability-based churn prediction**
6. **SHAP-based interpretation**

This creates a hybrid framework connecting **telecom analytics, quantum machine learning, and explainable AI**.

---

## 🎯 Applications

The proposed system can be explored for:

* Telecom customer retention
* Customer behavior analysis
* Churn-risk identification
* Personalized retention strategies
* Telecom business analytics
* Quantum machine-learning research
* Explainable predictive analytics

---

## 🔮 Future Scope

Future development can include:

* Increasing the number of qubits
* Testing different quantum feature maps
* Comparing multiple quantum classifiers
* Comparing quantum and classical models
* Testing quantum kernels
* Running experiments on real quantum hardware
* Hyperparameter optimization
* Real-time churn prediction
* Web-based prediction dashboard
* Automated customer retention recommendations
* Advanced explainability techniques

---

## 👥 Project Objective

The primary objective is to develop and evaluate a **quantum-enhanced telecom churn prediction pipeline** that combines quantum machine learning with classical optimization and explainable AI.

The project aims to investigate whether a compact quantum representation can be effectively integrated into a practical telecom analytics workflow.

---

## 📌 Disclaimer

This project is an academic/research implementation for exploring **Quantum Machine Learning (QML)** and **Explainable AI (XAI)** in telecom churn prediction. Model performance depends on the dataset, preprocessing, feature selection, quantum circuit design, optimizer settings, and evaluation methodology.

---

## 📜 License

This project is intended for academic and educational purposes.

---

## ⭐ Acknowledgements

This project combines concepts from:

* Machine Learning
* Quantum Computing
* Quantum Machine Learning
* Telecom Analytics
* Explainable Artificial Intelligence
* Hybrid Quantum-Classical Computing

**Built as an academic project exploring the intersection of Quantum Computing, Machine Learning, and Explainable AI.**


# Author

**Geetha**

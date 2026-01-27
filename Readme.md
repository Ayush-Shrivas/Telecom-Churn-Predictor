# 📉 Telecom Customer Churn Prediction Engine

[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![Scikit-Learn](https://img.shields.io/badge/ML-Scikit--Learn-orange.svg)](https://scikit-learn.org/)
[![Gradio](https://img.shields.io/badge/Interface-Gradio-hotpink.svg)](https://gradio.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-brightgreen.svg)](https://github.com/)

> **A robust Machine Learning pipeline designed to identify high-risk customers and reduce churn rates through proactive retention strategies.**

---

## 📖 Executive Summary
In the telecommunications sector, customer acquisition costs (CAC) are significantly higher than retention costs. This project deploys a **Random Forest Classifier** to analyze customer demographics, billing patterns, and service usage history. 

By predicting the probability of **Customer Churn** (attrition) in real-time, this tool empowers business stakeholders to intervene with targeted offers, thereby increasing Customer Lifetime Value (CLTV).

---

## 🚀 Key Features

* **🧠 Intelligent Predictive Model:** Utilizes an ensemble logic (Random Forest) to classify users with high precision, handling non-linear relationships between billing and tenure.
* **⚡ Synthetic Data Engine:** Features a built-in data simulator that generates realistic, statistically significant telecom datasets (N=1000) for instant reproducibility without external dependencies.
* **📊 Automated EDA Pipeline:** Performs immediate Exploratory Data Analysis, generating correlation heatmaps and distribution plots to identify key churn drivers.
* **🎛️ Interactive Inference Dashboard:** Integrates a **Gradio GUI** directly into the workflow, allowing non-technical teams to perform "What-If" analysis on single customer profiles.

---
## 📂 Project Directory Structure

```text
├── 📂 .gradio               # Gradio cache files
├── 📂 Demo Screenshots      # Images used in README
│   ├── dashboard UI.png
│   └── HEATMAP.png
├── 📂 Dataset
│   └──  data
├── 📄 Churn_Analysis.ipynb  # Main Project Notebook
└── 📄 README.md             # Project Documentation
```
---

## 🛠️ Technical Architecture

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Language** | Python | Core programming logic. |
| **Data Processing** | Pandas / NumPy | Data manipulation, cleaning, and vectorization. |
| **Visualization** | Seaborn / Matplotlib | Statistical graphics and feature importance plotting. |
| **Machine Learning** | Scikit-Learn | Model training (Random Forest), validation, and metrics. |
| **Frontend** | Gradio | Web-based interface for model interaction. |

---

## 📂 Data Dictionary
The model analyzes the following features to generate predictions:

| Feature | Type | Description |
| :--- | :--- | :--- |
| `Tenure_Months` | Numerical | Number of months the customer has stayed with the company. |
| `MonthlyCharges` | Numerical | Current monthly bill amount (USD). |
| `Contract` | Categorical | Type of contract: *Month-to-month, One year, Two year*. |
| `PaymentMethod` | Categorical | Billing method (e.g., *Electronic check, Credit card*). |
| `SeniorCitizen` | Binary | Whether the customer is a senior citizen (0/1). |
| `PaperlessBilling` | Binary | Whether the customer uses paperless billing (Yes/No). |

---

## ⚙️ Installation & Usage

### Prerequisites
* Python 3.7 or higher
* Jupyter Notebook or VS Code (Recommended)

### Step 1: Clone the Repository
```bash
git clone [https://github.com/yourusername/churn-prediction-engine.git](https://github.com/yourusername/churn-prediction-engine.git)
cd churn-prediction-engine
```
### Step 2: Install Dependencies
```bash 
pip install pandas numpy matplotlib seaborn scikit-learn gradio
```
### Step 3: Run the Analysis
Execute the main script or notebook:
```bash
# If using Jupyter Notebook
jupyter notebook Churn_Analysis.ipynb
```
Upon running, the script will train the model and launch the local web server for the GUI.

---
## 📊 Model Performance
The current Random Forest implementation achieves the following metrics on the synthetic validation set:

* Accuracy: ~85-90%

* Precision: High reliability in identifying "Safe" customers.

* Recall: Optimized to capture potential churners (minimizing False Negatives).

### Key Insights (Feature Importance)
The model identified the following as the top predictors of churn:

* Contract Type: Month-to-month contracts are the single strongest indicator of flight risk.

* Tenure: Risk decreases exponentially after the first 12 months.

* Monthly Charges: High billing amounts correlate positively with churn probability.
---
## 📸 Screenshots

### 1. The Interactive Dashboard
_The user-friendly interface allows support agents to input customer details and receive an instant risk assessment._

![Dashboard Interface](Demo%20Screenshots/dashboard%20UI.png)

### 2. Confusion Matrix & Heatmap
_Visual validation of the model's true positive vs. false positive rates._

![Confusion Matrix & Heatmap](Demo%20Screenshots/HEATMAP.png)
---

## 🔄 System Workflow

```text
[Raw Data] 
   │
   ▼
[Preprocessing] --> (Data Cleaning & One-Hot Encoding)
   │
   ▼
[Train/Test Split]
   │
   ├─> [Training Set] --> [Random Forest Model] 
   │          │
   └─> [Testing Set] ───────────┐
                                │
                              [Evaluation]
                                │
   ┌────────────────────────────┘
   ▼
[Gradio Interface] --> (User Inputs Data)
   │
   ▼
((Prediction: High Risk / Safe))
    
```
## 👥 Collaborators

**Ayush**
* **Role:** Lead Developer & Data Scientist
* **Contribution:** Model training, GUI implementation, and Documentation.
* **GitHub**: [Ayush-Shrivas](https://github.com/Ayush-Shrivas)
* **LinkedIn**: [Ayush Shrivas](https://www.linkedin.com/in/ayush-shrivas-190475299/)

**Laxmi Tiwari**
* **Role:** Project Collaborator
* **Contribution:** Research, Data Analysis, and Testing.
* **GitHub**: [Laxmi-Tiwari](https://github.com/laxmi911)
* * **LinkedIn**: [Laxmi Tiwari](https://www.linkedin.com/in/laxmi-tiwari-aba648322/)
---

# Telecom Customer Churn Prediction

## 📌 Project Overview

Customer churn is one of the biggest challenges for telecom companies. Losing existing customers leads to reduced revenue and increased acquisition costs.

This project develops an **end-to-end Machine Learning solution** to predict customer churn and provide actionable business insights that help telecom companies proactively retain customers.

The project covers the complete data science workflow—from data preprocessing and exploratory data analysis (EDA) to model training, deployment with FastAPI, and an interactive Streamlit application.

---

## 🎯 Business Problem

Telecom companies collect large amounts of customer data, but identifying customers who are likely to leave remains a challenge.

The goal of this project is to:

* Predict whether a customer is likely to churn.
* Identify the key drivers of churn.
* Generate actionable business recommendations.
* Deploy the trained model for real-time predictions.

---

## 📂 Dataset

The project uses the **Telecom Customer Churn Dataset** containing **3,333 customer records**.

Features include:

* State
* Account Length
* Area Code
* International Plan
* Voice Mail Plan
* Number of Voice Mail Messages
* Total Day, Evening, Night, and International Minutes
* Call Charges
* Customer Service Calls
* Churn (Target Variable)

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* FastAPI
* Streamlit

---

## 📈 Exploratory Data Analysis (EDA)

The analysis uncovered several important business insights.

### Key Findings

* Approximately **14.5%** of customers churned.
* Customers with an **International Plan** had a significantly higher churn rate.
* Customers making **4 or more customer service calls** were much more likely to churn.
* Heavy daytime users showed higher churn rates.
* States such as **New Jersey, California, Texas, and Maryland** recorded some of the highest churn rates.

---

## 🤖 Machine Learning Model

Several preprocessing steps were applied before training:

* Data Cleaning
* Label Encoding
* Feature Engineering
* Train/Test Split

### Model Used

* Random Forest Classifier

### Model Performance

| Metric   | Score     |
| -------- | --------- |
| Accuracy | **95.5%** |
| ROC-AUC  | **91.6%** |

The Random Forest model provided strong predictive performance while maintaining good generalization on unseen data.

---

## 💡 Business Recommendations

Based on the analysis, the following recommendations were identified:

* Proactively contact customers after their fourth customer service call.
* Review pricing and offerings for International Plan subscribers.
* Develop loyalty programs for high-value customers.
* Launch targeted retention campaigns in high-churn states.
* Introduce unlimited daytime calling plans for heavy users.

---

## 🚀 Deployment

The trained model was deployed using:

### FastAPI

* REST API for real-time churn prediction.
* Interactive Swagger documentation.
* Business recommendations included in prediction responses.

### Streamlit

Interactive dashboard allowing users to:

* Enter customer information.
* Predict customer churn.
* View churn probability.
* Receive business recommendations.

---

## 📁 Project Structure

```text
Telecom_Churn_Project/
│
├── app.py
├── streamlit_app.py
├── requirements.txt
├── README.md
│
├── models/
│   ├── telecom_churn_model.joblib
│   ├── state_encoder.joblib
│   ├── intl_encoder.joblib
│   └── voice_encoder.joblib
│
├── notebooks/
│   └── Telecom_Customer_Churn.ipynb
│
├── data/
│   ├── churn-bigml-80.csv
│   └── churn-bigml-20.csv
│
└── images/
```

---

## ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Telecom-Churn-Prediction.git
```

Navigate into the project folder

```bash
cd Telecom-Churn-Prediction
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Run the FastAPI Application

```bash
uvicorn app:app --reload
```

Open your browser:

```
http://127.0.0.1:8000/docs
```

---

## ▶️ Run the Streamlit Application

```bash
streamlit run streamlit_app.py
```

---

## 📊 Example Prediction Output

```json
{
  "Prediction": "Likely to Churn",
  "Churn Probability": 0.94,
  "Confidence": "94.0%",
  "Risk Level": "High",
  "Business Recommendation": [
    "Customer has many support calls. Escalate to retention team.",
    "Review international plan pricing."
  ]
}
```

---

## 📌 Future Improvements

* Deploy the application on Render or Railway.
* Containerize the project with Docker.
* Add SHAP explainability for model predictions.
* Build an automated retraining pipeline.
* Store prediction history in a database.
* Integrate cloud deployment (AWS/Azure/GCP).

---

## 👩‍💻 About Me

**Faith Onalu-Iwuchukwu**

I am an aspiring Data Scientist passionate about transforming data into actionable business insights through Machine Learning, Predictive Analytics, and AI solutions.

### Skills

* Python
* SQL
* Machine Learning
* Data Analysis
* FastAPI
* Streamlit
* Power BI
* Tableau
* Scikit-learn

---

## ⭐ If you found this project interesting, please consider giving it a star!

Feedback, suggestions, and contributions are always welcome.

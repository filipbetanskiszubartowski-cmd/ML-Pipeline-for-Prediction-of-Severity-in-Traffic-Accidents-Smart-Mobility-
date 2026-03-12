# 🚨 Smart Mobility: Traffic Accident Severity Prediction

## 📌 Project Overview
This project presents an end-to-end Machine Learning pipeline designed to predict the severity of road accidents (Slight, Serious, Fatal). The primary business goal is to enable emergency services to optimize resource allocation in real-time by predicting accident severity before first responders arrive at the scene.

## ⚙️ Methodology & Technical Stack
* **Language:** Python 
* **Libraries:** Pandas, NumPy, Scikit-Learn, Seaborn, Matplotlib
* **Modeling:** Logistic Regression, Random Forest Classifier (OVR)
* **Evaluation Metrics:** ROC-AUC, F1-Score (Macro), Confusion Matrix

## 🧠 Feature Engineering Highlights
Instead of using raw data, several domain-specific features were engineered to improve model accuracy:
* **Temporal Features:** Cyclical feature extraction (Month, Day of Year) to capture seasonal accident trends.
* **Domain-Specific Flags:** Creation of `Is_Night` and `Is_Rush_Hour` variables to correlate lighting and traffic density with accident severity.
* **High-Cardinality Handling:** Implemented Frequency Encoding for categorical variables like `Local_Authority_(District)` and `Police_Force` to prevent high dimensionality without losing geographical patterns.

## 📊 Results & Business Impact
* The Random Forest classifier outperformed baseline models, effectively managing the non-linear relationships between road conditions, time, and severity.
* **Business Value:** Implementing this model in a centralized emergency dispatch system could prioritize ambulance dispatching, potentially reducing response times for life-threatening incidents.

> **Note:** The complete preprocessing pipeline, exploratory data analysis (EDA), and model training can be found in the `Machine_Learning_Project.ipynb` notebook.

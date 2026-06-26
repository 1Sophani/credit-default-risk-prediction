# Credit Default Risk Prediction

<img width="2074" height="1164" alt="Financial Risk Dashboard" src="https://github.com/user-attachments/assets/c78b3140-3310-4981-8374-73c937b22c0b" />

<img width="2074" height="1174" alt="Machine Learning Performance Dashboard" src="https://github.com/user-attachments/assets/88ace7f1-58d6-47d8-8328-fd22402b5473" />

---

## 📌 Project Overview

Financial institutions face significant financial losses due to borrower loan defaults. This project develops machine learning models to predict loan default risk and uses an interactive Power BI dashboard to communicate the key business drivers influencing default.

The project combines insights from two separate datasets:

* **LendingClub Accepted Loans** – Real-world U.S. lending data used for model training and evaluation.
* **Kaggle Financial Risk Data – Large** – A large synthetic dataset used for additional modeling and business intelligence dashboard development.

By comparing multiple machine learning algorithms across two independent datasets, this project validates whether important financial risk factors remain consistent regardless of data source.

---

# 🎯 Business Objectives

This project was designed to answer the following business questions:

* Which borrower characteristics contribute most to loan default?
* Can machine learning accurately identify high-risk borrowers?
* Which classification algorithm provides the best predictive performance?
* How can interactive dashboards communicate loan risk to business stakeholders?

---

# 🛠️ Technology Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* TensorFlow / Keras
* Jupyter Notebook
* Power BI
* Git
* GitHub

---

# 🗂️ Repository Structure

Credit-Default-Risk-Prediction/
│
├── Credit Default Risk.ipynb
├── Credit Default Risk.pbix
├── README.md

---

# 🔧 Data Preprocessing & Feature Engineering

Because the two datasets contained different schemas and feature structures, each dataset was cleaned and processed independently.

### Data Preparation

* Removed missing values
* Cleaned inconsistent records
* Normalized numerical variables
* Encoded categorical variables
* Prepared datasets for machine learning

### Feature Engineering

Several new variables were created to improve model performance and business interpretation, including:

* Credit Score Bands
* Age Groups
* Debt-to-Income (DTI) Ranges
* Employment Categories
* Loan Purpose Groupings

These engineered features made the dashboard easier to interpret while improving model usability.

---

# 🤖 Machine Learning Modeling

Separate machine learning pipelines were developed for each dataset due to their differing structures.

## Algorithms Evaluated

| Model                 | Purpose                                             |
| --------------------- | --------------------------------------------------- |
| Logistic Regression   | Baseline classification model                       |
| Decision Tree         | Capture nonlinear decision boundaries               |
| Random Forest         | Improve generalization through ensemble learning    |
| Neural Network (FCNN) | Learn complex relationships among borrower features |

---

## Evaluation Metrics

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Area Under the ROC Curve (AUC)

Because identifying borrowers likely to default is especially important in lending, recall and AUC were considered key performance metrics in addition to overall accuracy.

---

# 📈 Model Results

## LendingClub Dataset

Among the evaluated models, the **Neural Network (FCNN)** achieved the strongest overall balance of predictive performance.

| Model                     | Highlights                                                                                |
| ------------------------- | ----------------------------------------------------------------------------------------- |
| Logistic Regression       | Baseline performance with moderate predictive ability                                     |
| Decision Tree             | Nearly perfect Recall (99.9%) but lower AUC, suggesting potential overfitting             |
| Random Forest             | Strong Recall (93%) with balanced performance                                             |
| **Neural Network (FCNN)** | **Best overall model** with Recall = **98.3%**, Accuracy = **74.7%**, and **AUC = 0.801** |

---

## Kaggle Financial Risk Dataset

A second machine learning pipeline was developed using the Kaggle Financial Risk dataset.

Despite differences between the datasets, similar patterns emerged:

* Credit score remained one of the strongest predictors of default.
* Higher debt-to-income ratios were consistently associated with increased risk.
* Employment status influenced repayment behavior.
* Loan purpose remained an important risk indicator.

The Neural Network again produced the strongest overall performance, reinforcing the consistency of these financial risk factors.

---

# 📊 Interactive Power BI Dashboard

The dashboard translates machine learning findings into business-friendly visualizations that allow stakeholders to explore default risk across multiple borrower characteristics.

## Dashboard Insights

### Debt-to-Income Ratio (DTI)

Borrowers with **DTI values greater than 0.40** experienced a significant increase in default rates, suggesting debt burden is one of the strongest indicators of financial risk.

### Credit Score

Loan approval rates increased substantially once borrower credit scores exceeded approximately **600**, while lower scores were associated with higher default rates.

### Age

Borrowers between **18–25 years old** and **56+ years old** demonstrated elevated default rates compared to middle-aged borrowers.

### Employment Status

Unemployed and self-employed borrowers showed greater financial risk than borrowers employed full-time.

### Loan Purpose

Education loans exhibited the highest default rates among the loan categories analyzed.

---

# 💼 Business Recommendations

Based on the analysis, financial institutions may consider:

* Performing additional underwriting for applicants with DTI values above 0.40.
* Increasing review requirements for borrowers with credit scores below 600.
* Monitoring education-related loans more closely due to their elevated default rates.
* Incorporating the Neural Network model into underwriting workflows as a decision-support tool for identifying high-risk applicants.

---

# 🚀 How to Run

1. Clone this repository.
2. Open **Credit Default Risk.ipynb** in Jupyter Notebook or Visual Studio Code.
3. Run all notebook cells to reproduce preprocessing, modeling, and evaluation.
4. Open **Credit Default Risk.pbix** using Power BI Desktop to explore the interactive dashboard.

---

# ⚠️ Limitations

* One of the datasets is synthetic and may not fully represent real-world lending behavior.
* Hyperparameter optimization was limited.
* Class imbalance techniques (such as SMOTE) were not explored.
* Models were evaluated on historical datasets and were not deployed in a production environment.

---

# 🔮 Future Improvements

Potential enhancements include:

* Implement XGBoost and LightGBM models
* Perform hyperparameter tuning
* Deploy the model as an interactive web application
* Integrate SHAP values for explainable AI
* Develop a real-time prediction API
* Explore class imbalance techniques for improved model performance

---

# 📚 Datasets

* **LendingClub Accepted Loans** (Real-world lending dataset)
* **Kaggle Financial Risk Data – Large** (Synthetic financial risk dataset)

---

# 💡 Skills Demonstrated

* Data Cleaning
* Feature Engineering
* Exploratory Data Analysis
* Machine Learning
* Classification Modeling
* Neural Networks
* Model Evaluation
* Python
* Pandas
* Scikit-learn
* TensorFlow / Keras
* Power BI
* Business Intelligence
* Data Visualization

---

# ✨ Key Takeaway

This project demonstrates an end-to-end machine learning workflow for credit default prediction, from data preprocessing and feature engineering to model development, evaluation, and business intelligence reporting.

Across two independent datasets, credit score, debt-to-income ratio, employment status, and loan purpose consistently emerged as the strongest predictors of borrower default. Among the evaluated algorithms, the Neural Network delivered the best balance of predictive performance and generalization, while the interactive Power BI dashboard transformed technical findings into actionable insights for lending stakeholders.
  

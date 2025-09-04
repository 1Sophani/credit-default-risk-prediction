# Credit Default Risk Prediction

This project predicts loan default risk using machine learning models (Python, Jupyter Notebook) and visualizes risk drivers with an interactive Power BI dashboard.  

It combines insights from two datasets:
- **LendingClub Accepted Loans** (real-world US lending data for model training/testing)  
- **Kaggle Financial Risk Data – Large** (synthetic but large-scale dataset, used for both modeling and dashboarding)  

---

## 📊 Project Overview
Lending institutions face significant risk from borrower defaults.  
This project explores borrower features (credit score, DTI, employment, loan purpose, etc.) and applies machine learning models to predict default risk.  
A Power BI dashboard highlights key drivers of default and presents insights in a business-friendly format.  

---

## 🗂️ Repository Structure


---

## 🔧 Data Preprocessing & Feature Engineering
- Cleaned and preprocessed **two datasets independently** since they had different schemas:
  - **LendingClub Accepted Loans**  
  - **Kaggle Financial Risk Data – Large**
- Handled missing values, normalized numeric fields, and encoded categorical variables  
- Created engineered features such as:
  - Credit score bands  
  - Age groups  
  - DTI ranges  
  - Employment categories  
  - Loan purpose groupings  

---

## 🤖 Modeling
Because the datasets had different structures, I trained **two separate models**, one for each dataset.  

### Algorithms Tested
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Neural Network (FCNN)  

### Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- AUC (Area Under ROC Curve)  

---

## 📈 Results

### LendingClub Model
- **Neural Network (FCNN)** achieved the best overall performance:  
  - Recall = **98.3%**  
  - AUC = **0.801**  
  - Accuracy = 74.7%  
- **Decision Tree** reached near-perfect Recall (99.9%) but lower AUC, suggesting possible overfitting.  
- **Random Forest** provided strong Recall (93%) but slightly weaker balance.  
- **Logistic Regression** served as a baseline with moderate performance.  

### Kaggle Model
- Similar trends were observed: credit score, DTI, employment status, and loan purpose were consistent drivers of risk.  
- Neural Network again performed best overall, confirming patterns across datasets.  

---

## 📊 Dashboard (Kaggle Dataset)
The **Power BI dashboard** built on the Kaggle dataset highlights:  
- **Default Rate by DTI** → sharp increase when DTI ≥ 0.4  
- **Default Rate by Age** → higher risk in younger (18–25) and older (56+) borrowers  
- **Employment Status** → unemployed and self-employed groups trend riskier  
- **Loan Purpose** → education loans show the highest default rate  
- **Credit Score** → approval rates increase sharply above ~600

  
<img width="2074" height="1164" alt="image" src="https://github.com/user-attachments/assets/c78b3140-3310-4981-8374-73c937b22c0b" />

<img width="2074" height="1174" alt="image" src="https://github.com/user-attachments/assets/88ace7f1-58d6-47d8-8328-fd22402b5473" />

---

## 🚀 How to Run
1. Open the Jupyter Notebook (`Credit Default Risk.ipynb`) in Jupyter or VS Code and run all cells.  
2. Open the Power BI file (`Credit Default Risk.pbix`) in Power BI Desktop to explore the dashboard.  

---

## 🔮 Future Work
- Test additional models (XGBoost, LightGBM)  
- Hyperparameter tuning for Neural Networks  
- Deploy as an interactive web app  
- Add explainability layer (e.g., SHAP values for feature importance)  

---

## 📚 Datasets
- [LendingClub Accepted Loans](https://www.lendingclub.com/info/download-data.action)  
- [Kaggle Financial Risk Data – Large](https://www.kaggle.com/)  

---

## ✨ Key Takeaway
By cleaning and modeling **two different datasets** independently, this project validates that key risk drivers (credit score, DTI, employment, loan purpose) remain consistent across sources.  
The **Neural Network** model delivered the strongest balance of recall and generalization, while the **Power BI dashboard** translates these findings into actionable insights for business users.  

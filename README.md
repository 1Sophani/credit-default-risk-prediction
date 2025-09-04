# credit-default-risk-prediction
Credit default risk prediction using machine learning models (Python) with business insights via Power BI dashboard

---

## 🔧 Methodology
### Data Preprocessing & Feature Engineering
- Cleaned LendingClub dataset (missing values, encoding, outlier handling)  
- Created features: credit score bands, age groups, DTI ranges, employment categories, loan purpose groupings  

### Modeling
Trained and compared 4 machine learning models:
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Neural Network (FCNN)  

### Evaluation Metrics
- Accuracy, Precision, Recall, F1 Score, AUC  

---

## 📈 Results
- **Neural Network (FCNN)** achieved the best overall performance:  
  - Recall = **98.3%**  
  - AUC = **0.801**  
  - Accuracy = 74.7%  
- **Decision Tree** achieved almost perfect recall (99.9%) but lower AUC (0.800), suggesting possible overfitting.  
- **Random Forest** offered a strong balance with 93% recall.  
- **Logistic Regression** served as a baseline.  

---

## 📊 Dashboard (Kaggle Dataset)
Power BI dashboard built on the Kaggle Financial Risk Data – Large dataset highlights:
- **Default Rate by DTI**: sharp increase when DTI ≥ 0.4  
- **Default Rate by Age**: higher risk in younger (18–25) and older (56+) borrowers  
- **Employment Status**: unemployed and self-employed groups trend riskier  
- **Loan Purpose**: education loans show the highest default rate  
- **Credit Score**: approval rates increase sharply above ~600  

![Dashboard Screenshot](images/dashboard.png)  

---

## 🚀 How to Run
1. Open the Jupyter Notebook (`Credit Default Risk.ipynb`) in Jupyter or VS Code and run all cells.  
2. Open the Power BI file (`Credit Default Risk.pbix`) in Power BI Desktop to explore the dashboard.  

---

## 🔮 Future Work
- Test XGBoost / LightGBM models  
- Deploy as an interactive web app  
- Add explainability layer (e.g., SHAP values)  

---

## 📚 Datasets
- [LendingClub Accepted Loans](https://www.lendingclub.com/info/download-data.action)  
- [Kaggle Financial Risk Data – Large](https://www.kaggle.com/)  

---

## ✨ Key Takeaway
Machine learning models (particularly Neural Networks) can significantly reduce missed defaults, while dashboards allow business stakeholders to identify risk drivers quickly and intuitively.

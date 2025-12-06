# Texas School Rating Prediction (2022–2023)

A machine learning and data visualization project analyzing Texas public school performance using 2022–2023 Accountability Ratings from the Texas Education Agency (TEA).

---

## 📌 Project Overview
This project predicts the **Overall Rating (A–F)** of Texas public schools using academic, demographic, and distinction-based features.  
We used Python-based machine learning models and a multi-page Power BI dashboard to uncover statewide patterns in school performance.

---

## 📂 Dataset
**Source:** Texas Open Data Portal (TEA)  
**Title:** School Year 2022–2023 Statewide Accountability Ratings  
Dataset Link:  
https://data.texas.gov/dataset/School-Year-2022-2023-Statewide-Accountability-Rat/nui6-x374

The dataset includes:
- School and district identifiers  
- School type & charter status  
- Region and county  
- Demographic indicators  
- Academic performance scores  
- TEA distinction designations  
- **Target:** Overall Rating (A–F)

---

## 🧹 Data Preprocessing
Key preprocessing steps:
- Removed columns with >80% missing values  
- Imputed missing numeric (mean) and categorical (mode) values  
- Checked for duplicates  
- Handled outliers (kept them as real performance variation)  
- Encoded categorical variables  
- Converted rating A–F → 4–0  
- Standardized numeric features  
- Train/test split: **80% / 20%**

---

## 🛠 Feature Engineering
Custom engineered features include:
- **Performance Gap Index** – difference between achievement and equity indicators  
- **Distinction Rate (0–1)** – proportion of TEA distinctions earned  
- **Achievement Efficiency Ratio** – performance adjusted for school size & disadvantage  

These features capture deeper patterns not directly visible in raw TEA data.

---

## 🔍 Exploratory Data Analysis (EDA)
We built an interactive **Power BI dashboard** to analyze:
- A–F rating distribution  
- School type vs. performance  
- Charter vs. non-charter comparison  
- Distinction achievements  
- Regional, county, and district-level performance  
- Geographic clusters of A-rated schools  

📊 Dashboard Link:  
https://app.powerbi.com/groups/me/reports/9e60b870-aeb8-4e5f-8300-9537faf1a9ae/b4f5805990120ceadc3b?ctid=5cdc5b43-d7be-4caa-8173-729e3b0a62d9&experience=power-bi&clientSideAuth=0&bookmarkGuid=3a8a485c-0811-4b34-860d-8e60ce788048

---

## 🤖 Models Used
We trained four supervised models:

- Logistic Regression  
- Linear Discriminant Analysis (LDA)  
- Random Forest  
- XGBoost  

**Evaluation Metrics:**
- Accuracy  
- F1-score  
- ROC–AUC  

---

## 📈 Model Performance

| Model                   | Accuracy | ROC–AUC | Notes                               |
|------------------------|----------|---------|--------------------------------------|
| Logistic Regression     | ~65%     | ~0.89   | Good baseline, linear limitations    |
| LDA                     | ~60%     | ~0.86   | Misclassifies middle categories      |
| Random Forest           | ~91%     | 0.993   | Strong nonlinear modeling            |
| **XGBoost**             | **~92%** | **~0.99** | **Best model overall**              |

**XGBoost** was the top-performing model, with excellent separation across all five rating categories.

---

## 🏁 Conclusion
Machine learning models—particularly ensemble methods—proved highly effective for predicting Texas school accountability ratings.  
The combination of engineered features, academic indicators, and geographic insights produced strong, interpretable results.

---

## 🚀 Future Work
Possible extensions:
- Add **tuition and funding data** for each campus  
- Incorporate detailed TEA distinction criteria  
- Include additional years of accountability data  
- Perform hyperparameter tuning  
- Use deep learning models  
- Add fairness analysis across student groups  
- Expand Power BI dashboard with more drill-through options  

---

## 👥 Team Members 
- Phuong Le Thien Trinh  
- Lingala Harini Sarma  
- Mohamed Ahmed  
- Sai Harshith Kondabathini  

---


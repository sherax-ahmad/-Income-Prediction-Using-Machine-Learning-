# Income Prediction Using Machine Learning

This repository contains an analysis of **income prediction** using the [UCI Adult Income Dataset](https://archive.ics.uci.edu/dataset/2/adult).  
The project explores **bias and fairness in machine learning models**, with a focus on how demographic factors (such as gender) influence predictions and perpetuate inequalities.

---

## 📌 Project Overview
- **Objective**: Build a machine learning model to predict whether an individual earns more than \$50,000 per year.  
- **Dataset**: UCI Adult Census dataset (48,842 records).  
- **Model**: Random Forest Classifier with fairness evaluation.  
- **Focus**: Identify and analyze **algorithmic bias** across gender groups using fairness criteria such as:
  - Accuracy
  - Demographic Parity
  - Equal Opportunity  

---

## 🔎 Key Findings
- Overall model accuracy: **86%**.  
- Model performs better at predicting low-income individuals (≤\$50K).  
- Gender bias is evident:
  - Men predicted as high earners **~3x more often** than women (26.4% vs 9.3%).  
  - Equal opportunity was somewhat satisfied (4.5% TPR disparity), but demographic parity was not.  
- Education, age, and weekly working hours are the strongest predictors of income.  

---

## ⚙️ Methodology
1. **Data Preprocessing**
   - Removal of missing values.
   - One-hot encoding of categorical features.
   - Standardization of numerical features.
   - Gender removed from training features to test indirect bias.  

2. **Model Development**
   - Random Forest Classifier.
   - Hyperparameter tuning via cross-validation.
   - Train-test split with stratification.  

3. **Evaluation**
   - Classification metrics (precision, recall, F1-score, accuracy).
   - Confusion matrix (raw & normalized).
   - Fairness analysis by gender groups.

---

## 📊 Results
| Metric | Low Income (≤50K) | High Income (>50K) |
|--------|------------------|--------------------|
| Precision | 0.89 | 0.74 |
| Recall    | 0.93 | 0.64 |
| F1-Score  | 0.91 | 0.68 |
| Accuracy  | **86%** | - |

- Bias analysis shows that **accuracy differences and demographic imbalances** exist even without explicitly using gender as a feature.  

---

## 📂 Repository Structure
├── data/ # Dataset (not included, must be downloaded)

├── notebooks/ # Jupyter notebooks for exploration & modeling

├── src/ # Python scripts for preprocessing & modeling

├── results/ # Figures, evaluation metrics, and fairness reports

├── README.md # Project documentation

└── requirements.txt # Python dependencies


---

## 🚀 How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/your-username/income-prediction-ml.git
   cd income-prediction-ml



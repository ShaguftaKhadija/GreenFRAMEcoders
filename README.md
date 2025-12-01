GreenFrame Coders — Depression Detection Using ML Models
---
IBMz Datathon 2025

Project overview
---
An end-to-end machine learning pipeline to detect depression from student 
survey data. The project covers data preprocessing, model selection, training & 
validation, evaluation, and explainability (XAI) for model decisions. The goal is 
a reliable, interpretable classifier that helps identify students at 
risk so that interventions can be planned.

What this repository contains
---
GreenFrame-Coders/
├── notebook.ipynb                      # Main notebook (modeling, EDA, XAI)
├── data/
│   ├── student_depression.csv          # Dataset used (cleaned / original)
├── models/
│   ├── final_model.pkl                  # Trained model (optional)
├── visuals/
│   ├── missing_values.png
│   ├── class_distribution.png
│   ├── feature_importance.png
├── README.md                              <-- You are editing this
├── project_report.pdf                      # Project write-up (attached)
└── requirements.txt                         # Python requirements

Key questions answered
---
1.What is in the dataset?

Overview of fields used: id, Gender, Age, City, Profession, Academic Pressure, Work Pressure,
CGPA, Study Satisfaction, Job Satisfaction, Sleep Duration, Dietary Habits, Degree, Have you ever
had suicidal thoughts?, Work/Study Hours, Financial Stress, Family History of Mental Illness, 
Depression.(See dataset file in data/.)

2.Can we predict depression from the available features?

We train classification models (logistic regression as baseline) and evaluate predictive performance
using accuracy, precision, recall, F1, and ROC-AUC.

3.Is the model robust and ready for preliminary screening?

We perform cross-validation, inspect class balance, and analyze failure modes. Results and recommendations
are in project_report.pdf. 

Dataset source & license
--
Dataset used (original source):https://www.kaggle.com/datasets/hopesb/student-depression-dataset?resource=download

License: Apache 2.0:Public Domain Dataset is publicly available for educational and analytical use.

Credit: “Data source:Kaggle-Shodolamu Opeyemi(Student Depression) 

Tools & methods
---
Languages / Tools: Python (pandas, scikit-learn, matplotlib), Jupyter Notebook

Data processing: missing value checks, median imputation (e.g., Sleep Duration), one-hot encoding for categorical 
variables, scaling where needed.

Modeling: logistic regression (baseline), other classifiers explored (e.g., Random Forest, XGBoost) — train/validate/test 
split and cross-validation.

Evaluation: accuracy, precision, recall, F1, confusion matrix, ROC-AUC. 

Version control / repo: Git & GitHub

How to reproduce (simple)
---
1.Clone this repository:
git clone https://github.com/ShaguftaKhadija/GreenFRAMEcoders.git
cd GreenFRAMEcoders

2.Install dependencies:
pip install -r requirements.txt

3.Open the notebook:
Launch Jupyter and open notebook.ipynb, or view project_report.pdf
for the summary.

4.Prepare the data:
•Place student_depression.csv in the data/ folder (or use the provided copy).
•Run the Data preprocessing section: check missing values, fill Sleep Duration with
median, one-hot encode categorical columns.

5.Train & evaluate:
•Run the Model training and evaluation cells. A logistic regression baseline is included;
other models and cross-validation are available in the notebook.

6.Save results:
•Trained model artifacts (if created) can be saved to models/.
•Visualizations will be saved in visuals/.

Files to check first
--
notebook.ipynb — step-by-step code (EDA → preprocessing → modeling → XAI).
project_report.pdf — short project write-up and high-level results. 

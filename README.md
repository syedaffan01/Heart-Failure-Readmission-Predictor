🧠 Heart Failure Readmission Predictor

💻 An AI-powered web app that predicts the likelihood of hospital readmission (or death event) in heart failure patients using machine learning.

🩺 Overview:

Heart failure is a major global health issue, leading to high readmission rates and mortality.
This project uses Machine Learning (XGBoost Classifier) to predict whether a patient with heart failure is likely to experience a readmission/death event within 30 days based on clinical features.

The model is deployed using Flask, allowing doctors or hospitals to easily enter patient details through a web interface and instantly get predictions.

🚀 Tech Stack:
Component	Technology
Programming Language-	Python
Framework-	Flask
Machine Learning-	Scikit-learn, XGBoost
Data Preprocessing-	NumPy, Pandas
Visualization-	Matplotlib, Seaborn
Model Persistence-	Pickle
Frontend-	HTML, CSS (via Flask Templates)

📂 Project Structure:

heart_failureapp/
│
├── app.py                       # Flask backend app
├── heart_failure_model.sav      # Trained ML model
├── scaler.sav                   # Scaler for preprocessing
├── requirements.txt             # Required dependencies
├── .gitignore                   # Git ignore file
├── templates/
│   └── index.html               # Frontend HTML page
└── README.md                    # Project documentation

📊 Dataset Information:

📁 Dataset Name: Heart Failure Clinical Records Dataset
📦 Source: UCI Machine Learning Repository

Feature	Description
age- Age of the patient
anaemia-	Decrease of red blood cells (1 = Yes, 0 = No)
creatinine_phosphokinase-	Enzyme level in the blood (mcg/L)
diabetes-	Diabetes status (1 = Yes, 0 = No)
ejection_fraction-	Percentage of blood leaving the heart per contraction
high_blood_pressure-	Hypertension (1 = Yes, 0 = No)
platelets-	Platelet count (kiloplatelets/mL)
serum_creatinine-	Level of kidney function (mg/dL)
serum_sodium-	Sodium level (mEq/L)
sex-	1 = Male, 0 = Female
smoking-	1 = Smoker, 0 = Non-smoker
time-	Follow-up period (days)
DEATH_EVENT	Target variable (1 = Died, 0 = Survived)

🧩 Machine Learning Pipeline:

Data Preprocessing

Scaled features using StandardScaler

Handled data normalization

Model Training

Algorithms tested: Logistic Regression, Random Forest, XGBoost

Best model: XGBoost Classifier

Model Evaluation

Accuracy: ~87–90%

AUC Score: ~0.91

Model Deployment

Model and scaler saved using pickle

Integrated with Flask for web prediction

🧠 Prediction Parameters (User Inputs):
Input Field	Example	Description
Age- 65	Patient age in years
Anaemia	0	1 = Yes, 0 = No
Creatinine Phosphokinase	250	mcg/L
Diabetes	1	1 = Yes, 0 = No
Ejection Fraction	35	% blood leaving heart per contraction
High Blood Pressure	1	1 = Yes, 0 = No
Platelets	250000	kiloplatelets/mL
Serum Creatinine	1.0	mg/dL
Serum Sodium	135	mEq/L
Sex	1	1 = Male, 0 = Female
Smoking	0	1 = Yes, 0 = No
Time	130	Days of follow-up


🧾 Results Displayed:

After clicking Predict, the app shows:

✅ Low Readmission Risk
or
⚠️ High Readmission Risk


⚙️ Installation & Setup:

1️⃣ Clone this repository:

git clone https://github.com/syedaffan01/Heart-Failure-Readmission_Predictor.git


2️⃣ Navigate into the project folder:

cd Heart-Failure-Readmission_Predictor


3️⃣ Create a virtual environment:

python -m venv venv


4️⃣ Activate it:

Windows: venv\Scripts\activate

Mac/Linux: source venv/bin/activate

5️⃣ Install dependencies:

pip install -r requirements.txt


6️⃣ Run the Flask app:

python app.py


7️⃣ Open in browser:

http://127.0.0.1:5000/

🧠 Concepts Used

Supervised Machine Learning

Classification Problem

Data Normalization (StandardScaler)

Model Persistence (Pickle)

Flask Web Deployment

Web Form Integration

🎨 UI Overview

A clean and minimal HTML interface built using Flask templates.

🖥️ Page: index.html

Input form for patient details

“Predict” button

Result displayed dynamically below the form

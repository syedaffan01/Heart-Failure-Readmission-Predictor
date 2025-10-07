# Heart Failure Readmission Predictor
🧠 An AI-powered web app that predicts the likelihood of hospital readmission (or death event) in heart failure patients using machine learning.

## 🩺 Overview
Heart failure is a major global health issue, leading to high readmission rates and mortality. This project uses Machine Learning (XGBoost Classifier) to predict whether a patient with heart failure is likely to experience a readmission/death event within 30 days based on clinical features. The model is deployed using Flask, allowing doctors or hospitals to easily enter patient details through a web interface and instantly get predictions.

## 🚀 Tech Stack
| Component           | Technology                     |
|---------------------|--------------------------------|
| Programming Language| Python                         |
| Framework           | Flask                          |
| Machine Learning    | Scikit-learn, XGBoost          |
| Data Preprocessing  | NumPy, Pandas                  |
| Visualization       | Matplotlib, Seaborn            |
| Model Persistence   | Pickle                         |
| Frontend            | HTML, CSS (via Flask Templates)|

## 📂 Project Structure
```
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
```

## 📊 Dataset Information
**Dataset Name**: Heart Failure Clinical Records Dataset  
**Source**: UCI Machine Learning Repository  

| Feature                  | Description                                      |
|--------------------------|--------------------------------------------------|
| age                      | Age of the patient                               |
| anaemia                  | Decrease of red blood cells (1 = Yes, 0 = No)     |
| creatinine_phosphokinase | Enzyme level in the blood (mcg/L)                |
| diabetes                 | Diabetes status (1 = Yes, 0 = No)                |
| ejection_fraction        | Percentage of blood leaving the heart per contraction |
| high_blood_pressure      | Hypertension (1 = Yes, 0 = No)                   |
| platelets                | Platelet count (kiloplatelets/mL)                |
| serum_creatinine         | Level of kidney function (mg/dL)                 |
| serum_sodium             | Sodium level (mEq/L)                             |
| sex                      | 1 = Male, 0 = Female                             |
| smoking                  | 1 = Smoker, 0 = Non-smoker                       |
| time                     | Follow-up period (days)                          |
| DEATH_EVENT              | Target variable (1 = Died, 0 = Survived)         |

## 🧩 Machine Learning Pipeline
1. **Data Preprocessing**  
   - Scaled features using StandardScaler  
   - Handled data normalization  

2. **Model Training**  
   - Algorithms tested: Logistic Regression, Random Forest, XGBoost  
   - Best model: XGBoost Classifier  

3. **Model Evaluation**  
   - Accuracy: ~87–90%  
   - AUC Score: ~0.91  

4. **Model Deployment**  
   - Model and scaler saved using pickle  
   - Integrated with Flask for web prediction  

## 🧠 Prediction Parameters (User Inputs)
| Input Field             | Example | Description                              |
|-------------------------|---------|------------------------------------------|
| Age                     | 65      | Patient age in years                     |
| Anaemia                 | 0       | 1 = Yes, 0 = No                          |
| Creatinine Phosphokinase| 250     | mcg/L                                    |
| Diabetes                | 1       | 1 = Yes, 0 = No                          |
| Ejection Fraction       | 35      | % blood leaving heart per contraction    |
| High Blood Pressure     | 1       | 1 = Yes, 0 = No                          |
| Platelets               | 250000  | kiloplatelets/mL                         |
| Serum Creatinine        | 1.0     | mg/dL                                    |
| Serum Sodium            | 135     | mEq/L                                    |
| Sex                     | 1       | 1 = Male, 0 = Female                     |
| Smoking                 | 0       | 1 = Yes, 0 = No                          |
| Time                    | 130     | Days of follow-up                        |

## 🧾 Results Displayed
After clicking Predict, the app shows:  
✅ **Low Readmission Risk**  
or  
⚠️ **High Readmission Risk**

## ⚙️ Installation & Setup
1. Clone this repository:  
   ```bash
   git clone https://github.com/syedaffan01/Heart-Failure-Readmission-Predictor.git
   ```

2. Navigate into the project folder:  
   ```bash
   cd Heart-Failure-Readmission-Predictor
   ```

3. Create a virtual environment:  
   ```bash
   python -m venv venv
   ```

4. Activate it:  
   - **Windows**: `venv\Scripts\activate`  
   - **Mac/Linux**: `source venv/bin/activate`

5. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

6. Run the Flask app:  
   ```bash
   python app.py
   ```

7. Open in browser:  
   ```
   http://127.0.0.1:5000/
   ```

## 🧠 Concepts Used
- Supervised Machine Learning  
- Classification Problem  
- Data

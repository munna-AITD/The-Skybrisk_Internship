# ✈️ Flight Delay Prediction System using Machine Learning

A complete Machine Learning project that predicts whether a flight will be delayed by more than 15 minutes using airline operational data from the Kaggle US Flight Delay Dataset.

---

# 📌 Project Overview

Flight delays significantly impact airline operations, airport scheduling, passenger satisfaction, and operational costs. This project develops a predictive analytics system using Machine Learning algorithms to classify flights as delayed or non-delayed.

The project includes:

* Data preprocessing
* Missing value handling
* Exploratory Data Analysis (EDA)
* Feature engineering
* Classification modeling
* Logistic Regression
* Random Forest Classifier
* Model evaluation
* ROC-AUC analysis
* Model saving using `.pkl`

---

# 📂 Dataset

Dataset Source:

[Kaggle US Flight Delay Dataset](https://www.kaggle.com/datasets/usdot/flight-delays?utm_source=chatgpt.com)

Dataset contains:

* Airline operational records
* Airport information
* Flight schedules
* Delay details

Sample size used in this project:

```python
100000 rows
```

---

# 🎯 Problem Statement

The objective is to predict whether a flight will be delayed by more than 15 minutes before departure using machine learning classification techniques.

Target Variable:

```python
DELAYED = ARRIVAL_DELAY > 15
```

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Joblib / Pickle
* Jupyter Notebook

---

# ⚙️ Data Preprocessing

The following preprocessing techniques were applied:

## ✅ Missing Value Handling

* Mean imputation for normal distributions
* Median imputation for skewed distributions

## ✅ Categorical Encoding

* Label Encoding

## ✅ Feature Scaling

* StandardScaler (for Logistic Regression)

## ✅ Data Leakage Removal

The following leakage columns were removed:

```python
ARRIVAL_TIME
WHEELS_ON
WHEELS_OFF
AIR_TIME
ELAPSED_TIME
TAXI_IN
TAXI_OUT
DEPARTURE_DELAY
```

These variables contain future operational information and would produce unrealistic model performance.

---

# 📊 Exploratory Data Analysis (EDA)

EDA included:

* Delay distribution analysis
* Airline-wise delay frequency
* Histogram plots
* Correlation heatmaps
* Missing value analysis
* Airport traffic analysis

Suggested visualizations:

* ROC Curve
* Confusion Matrix
* Feature Importance
* Delay Distribution

---

# 🤖 Machine Learning Models

## 1️⃣ Logistic Regression

### Features

* Linear classification model
* Used with:

```python
class_weight='balanced'
```

### Performance

| Metric   | Score |
| -------- | ----- |
| Accuracy | 71.6% |
| ROC-AUC  | 0.79  |
| Recall   | 0.71  |
| F1-score | 0.63  |

---

## 2️⃣ Random Forest Classifier

### Features

* Ensemble learning model
* Nonlinear relationship handling
* Better generalization capability

### Performance

| Metric   | Score  |
| -------- | ------ |
| Accuracy | 83.23% |
| ROC-AUC  | 0.89   |
| Recall   | 0.71   |
| F1-score | 0.74   |

---

# 📈 ROC Curve Analysis

The ROC-AUC score comparison demonstrated that Random Forest significantly outperformed Logistic Regression.

| Model               | ROC-AUC |
| ------------------- | ------- |
| Logistic Regression | 0.79    |
| Random Forest       | 0.89    |

Random Forest showed superior discrimination capability for delayed vs non-delayed flights.

---

# 📉 Confusion Matrix

## Random Forest

```python
[[11869 1400]
 [1953 4778]]
```

Interpretation:

* Correctly predicted most delayed flights
* Reduced false negatives
* Better operational usefulness

---

# 🧠 Key Findings

✅ Random Forest outperformed Logistic Regression
✅ Class balancing improved delayed flight detection
✅ Data leakage removal produced realistic evaluation
✅ ROC-AUC confirmed strong classification performance
✅ Recall is critical for airline operational systems

---

# 💼 Business Applications

This system can help airlines:

* Predict delays before departure
* Improve passenger communication
* Optimize airport operations
* Reduce operational costs
* Improve crew and gate management
* Enhance scheduling efficiency

---

# 🚀 Future Improvements

Future enhancements may include:

* XGBoost implementation
* LightGBM
* Weather data integration
* Real-time flight tracking
* Deep Learning models
* Streamlit deployment
* Flask API deployment
* Hyperparameter tuning

---

# 💾 Model Saving

Models were saved using Pickle / Joblib:

```python
import joblib

joblib.dump(rf_model, 'random_forest_model.pkl')
```

---

# ▶️ How to Run

## Install Dependencies

```bash
pip install pandas numpy matplotlib scikit-learn joblib kagglehub
```

## Run Notebook

```bash
jupyter notebook
```

---

# 📁 Project Structure

```bash
Flight-Delay-Prediction/
│
├── data/
├── notebooks/
├── models/
├── reports/
├── images/
├── README.md
├── requirements.txt
└── app.py
```

---

# 📌 Conclusion

This project successfully developed a Machine Learning-based Flight Delay Prediction System using airline operational data.

Among all models, Random Forest demonstrated the best overall performance with:

* Higher accuracy
* Better F1-score
* Strong ROC-AUC
* Better nonlinear learning capability

The system is suitable for real-world airline operational support and future deployment applications.

---

# 👨‍💻 Author

Munna Kumar

Machine Learning | Data Science | AI Projects

---


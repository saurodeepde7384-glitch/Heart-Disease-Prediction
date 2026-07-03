# Heart Disease Prediction using Logistic Regression

An approachable machine learning project that uses **Logistic Regression** to forecast the risk of heart disease. A whole machine learning workflow, including data exploration, preprocessing, model training, evaluation, and serialisation, is shown in this project.

> **Note:** This project was built as part of my machine learning learning journey and is intended for educational purposes.

---

## Project Overview

The objective of this project is to build a binary classification model that predicts whether a patient is likely to have heart disease based on various medical parameters.

The workflow covers:

* Data loading and inspection
* Exploratory Data Analysis (EDA)
* Data preprocessing
* Feature selection
* Model training using Logistic Regression
* Model evaluation
* Saving the trained model using Joblib

---

## Dataset Features

The dataset contains medical attributes such as:

* Age
* Gender
* Heart Rate
* Systolic Blood Pressure
* Diastolic Blood Pressure
* Blood Sugar
* CK-MB
* Troponin
* Result (Target Variable)

---

## Technologies Used

* Python
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib

---

## Project Structure

```
Heart-Disease-Prediction/
│
├── data/
│   └── Medicaldataset.csv
│
├── models/
│   └── logistic_model.pkl
│
├── notebooks/
│   └── Heart_Disease_Prediction.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Machine Learning Workflow

1. Import required libraries
2. Load the dataset
3. Perform exploratory data analysis
4. Encode categorical values
5. Split the dataset into training and testing sets
6. Train a Logistic Regression model
7. Evaluate the model using multiple classification metrics
8. Save the trained model for future use

---

## Evaluation Metrics

The model is evaluated using:

* Accuracy
* Confusion Matrix
* Precision
* Recall
* F1-Score
* Classification Report

These metrics provide a better understanding of the model's classification performance beyond overall accuracy.

---

## Model Saving

The trained model is saved using Joblib, allowing it to be loaded later without retraining.

```python
import joblib

model = joblib.load("models/logistic_model.pkl")
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/saurodeepde7384-glitch/Heart-Disease-Prediction.git
```

Move into the project directory:

```bash
cd Heart-Disease-Prediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## Future Improvements

Some improvements planned for future versions include:

* User input
* Feature scaling
* Hyperparameter tuning
* Cross-validation
* Trying additional classification algorithms
* Building a Streamlit or Flask web application
* Model comparison and performance visualization

---

## Saurodeep De



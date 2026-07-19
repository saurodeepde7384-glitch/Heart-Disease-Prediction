# Heart Attack Prediction using Machine Learning

A beginner-friendly Machine Learning project that predicts the likelihood of a heart attack using multiple classification algorithms. The project demonstrates an end-to-end machine learning workflow, including Exploratory Data Analysis (EDA), preprocessing with Scikit-learn Pipelines, model training, evaluation, comparison, and model serialization.

> **Note:** This project was built as part of my machine learning learning journey and is intended for educational purposes.

---

## Project Overview

The objective of this project is to build and compare multiple machine learning classification models that predict whether a patient is likely to experience a heart attack based on various medical parameters.

To maintain a clean workflow, the project is divided into two separate notebooks:

* **heartattack_eda.ipynb** – Data exploration, visualization, and insights.
* **heartattack_model_training.ipynb** – Data preprocessing, model training, evaluation, comparison, and model saving.

---

## Dataset Features

The dataset contains the following medical attributes:

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
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib

---

## Project Structure

```text
heartattackprediction/
│
├── data/
│   └── Medicaldataset.csv
│
├── models/
│   ├── decision_tree_model.pkl
│
├── notebooks/
│   ├── heartattack_eda.ipynb
│   └── heartattack_model_training.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Exploratory Data Analysis (EDA)

The EDA notebook focuses on understanding the dataset before model development. It includes:

* Dataset overview
* Missing value analysis
* Duplicate value checking
* Statistical summary
* Feature distribution analysis
* Correlation analysis
* Data visualization
* Key observations and insights

---

## Data Preprocessing

The training notebook uses Scikit-learn Pipelines to create a reusable preprocessing workflow.

### Numerical Pipeline

* Median Imputation (Used Median to tackle the outliers)
* Standard Scaling

### Categorical Pipeline

* Most Frequent Imputation
* One-Hot Encoding

Both pipelines are combined using **ColumnTransformer**, ensuring that each feature type receives the appropriate preprocessing automatically.

---

## Machine Learning Pipeline

The preprocessing workflow is integrated with the machine learning model using Scikit-learn's `Pipeline`.

This approach provides several advantages:

* Prevents data leakage
* Keeps preprocessing and model training together
* Simplifies prediction on new data
* Makes model deployment easier

---

## Models Trained

The following classification algorithms are trained and evaluated:

* Logistic Regression
* K-Nearest Neighbors (KNN)
* Support Vector Machine (SVM)
* Decision Tree Classifier
* Random Forest Classifier
* Gradient Boosting Classifier

Each model is trained using the same preprocessing pipeline to ensure a fair comparison.

---

## Model Evaluation

Each model is evaluated using multiple classification metrics:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Classification Report

A performance comparison is also conducted to identify the most effective model.

---

## Model Serialization

The trained models are saved using **Joblib**, allowing them to be loaded later without retraining.

```python
import joblib

model = joblib.load("models/decision_tree_model.pkl")
prediction = model.predict(new_data)
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/saurodeepde7384-glitch/Heart-Disease-Prediction.git
```

Navigate to the project directory:

```bash
cd heartattackprediction
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## Future Improvements

Some potential enhancements include:

* Hyperparameter tuning
* Cross-validation
* Feature engineering
* Model explainability using SHAP or LIME
* Streamlit web application
* REST API deployment with Flask or FastAPI
* Automated model selection and optimization

---

## Author

**Saurodeep De**

---

## License

> This Project Is Open-Source & Free To Use.
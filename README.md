# Heart Attack Prediction using Machine Learning

A beginner-friendly Machine Learning project that predicts the likelihood of a heart attack using multiple classification algorithms. The project demonstrates an end-to-end machine learning workflow, including Exploratory Data Analysis (EDA), preprocessing with Scikit-learn Pipelines, model training, evaluation, comparison, and model serialization.

An approachable machine learning project that uses **Logistic Regression** to forecast the risk of heart disease. A whole machine learning workflow, including data exploration, preprocessing, model training, evaluation, and serialisation, is shown in this project.


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
* Scikit-Learn
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

## Results

The performance of each classification model was evaluated using Accuracy, Precision, Recall, and F1-Score.

| Model                  |   Accuracy |  Precision |     Recall |   F1-Score |
| :--------------------- | ---------: | ---------: | ---------: | ---------: |
| Logistic Regression    |     78.03% |     81.56% |     82.57% |     82.06% |
| K-Nearest Neighbors    |     62.12% |     69.04% |     68.46% |     68.75% |
| Support Vector Machine |     70.71% |     74.13% |     79.67% |     76.80% |
| **Decision Tree**      | **98.23%** | **97.95%** | **98.56%** | **98.56%** |
| Random Forest          |     97.98% |     97.94% |     98.76% |     98.35% |
| Gradient Boosting      |     97.98% |     97.55% | **99.17%** | **98.35%** |

### Best Performing Model

Among all the evaluated models, the **Decision Tree Classifier** achieved the highest overall performance, with an accuracy of **98.23%** while maintaining excellent precision, recall, and F1-score. Random Forest and Gradient Boosting also delivered highly competitive results, making them strong alternatives for this classification task.


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
* Streamlit or Fast API web application
* REST API deployment with Flask or FastAPI
* Automated model selection and optimization

---

## Author

* SAURODEEP DE

---

## License

> This project is open-source and free to use (Only for Educational Purpose and is not trained on any real life data).

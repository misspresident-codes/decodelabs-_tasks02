<h1 align="center">💳 Credit Card Fraud Detection Using Machine Learning</h1>

<p align="center">
Detecting fraudulent transactions using Logistic Regression and Random Forest with SMOTE balancing.
</p>

---

## 📖 Overview

This project focuses on identifying fraudulent credit card transactions using Machine Learning techniques. Since fraud datasets are highly imbalanced, SMOTE (Synthetic Minority Oversampling Technique) was used to balance the classes before training the models.

Two classification models were implemented:

- Logistic Regression
- Random Forest Classifier

Their performances were compared using various evaluation metrics and ROC-AUC scores.

---

## 🚀 Features

- Data cleaning and preprocessing
- Feature engineering
- Handling missing values
- Label encoding categorical features
- Balancing classes using SMOTE
- Logistic Regression model
- Random Forest model
- Hyperparameter tuning using RandomizedSearchCV
- Performance evaluation
- ROC-AUC comparison

---

## 📂 Dataset

Dataset contains transaction information such as:

- Merchant
- Category
- Amount
- Gender
- City
- State
- Job
- Transaction Time
- Date of Birth
- Fraud Label (`is_fraud`)

Target variable:

```
is_fraud
```

- 0 → Legitimate transaction
- 1 → Fraudulent transaction

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Imbalanced-Learn
- Matplotlib
- Seaborn

---

## ⚙️ Workflow

### 1. Data Loading

```python
pd.read_csv()
```

---

### 2. Data Cleaning

Removed unnecessary columns:

- Unnamed: 0
- cc_num
- first
- last
- street
- trans_num

---

### 3. Feature Engineering

Extracted:

- Transaction hour
- Age of customer

Converted:

- Transaction date → datetime
- DOB → datetime

---

### 4. Encoding

Categorical columns encoded using LabelEncoder:

- merchant
- category
- gender
- city
- state
- job

---

### 5. Train-Test Split

80% Training

20% Testing

```python
train_test_split()
```

---

### 6. Handling Class Imbalance

Applied:

```python
SMOTE()
```

to generate synthetic minority samples.

---

### 7. Models Used

#### Logistic Regression

Pipeline:

```
StandardScaler
↓
SMOTE
↓
Logistic Regression
```

#### Random Forest

Pipeline:

```
SMOTE
↓
Random Forest Classifier
```

Hyperparameters optimized using:

```python
RandomizedSearchCV()
```

---

### 8. Evaluation Metrics

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Classification Report

---

## 📊 Model Comparison

| Model | Description |
|---------|------------|
| Logistic Regression | Baseline model |
| Random Forest | Ensemble model with hyperparameter tuning |

ROC-AUC score was used to select the better model.

---

## 📁 Project Structure

```
├── fraudTrain.csv
├── Project2.ipynb
├── README.md
└── requirements.txt
```

---

## 📦 Installation

Clone repository:

```bash
git clone https://github.com/yourusername/Credit-Card-Fraud-Detection.git
```

Move into directory:

```bash
cd Credit-Card-Fraud-Detection
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run:

```bash
jupyter notebook
```

Open:

```
Project2.ipynb
```

---

## 🎯 Future Improvements

- XGBoost implementation
- LightGBM model
- Feature importance visualization
- SHAP explainability
- Deployment using Streamlit
- Real-time fraud detection API

---

## 👩‍💻 Author

**Khyati Sahu**

- Python Developer
- Machine Learning Enthusiast
- Data Science Learner

---

⭐ If you found this project useful, consider giving it a star.

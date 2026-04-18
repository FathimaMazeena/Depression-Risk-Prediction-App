# 🧠 Depression Risk Prediction App

🔗 **Live App:**
https://depression-risk-prediction-app.streamlit.app/

---

## 📌 Overview

This project is a **machine learning-based web application** that predicts the likelihood of depression based on user-provided inputs related to lifestyle, academic/work stress, and personal background.

It provides a **real-time, user-friendly interface** for non-technical users to assess mental health risk using a trained predictive model.

---

## 🚀 Key Features

* 🔍 Real-time depression risk prediction
* 📊 End-to-end ML pipeline (data → model → deployment)
* 🤖 Ensemble model using stacking (higher accuracy)
* 🌐 Fully deployed interactive app using Streamlit
* ☁️ External model hosting using Hugging Face

---

## 🧠 Machine Learning Pipeline

### 🔹 Data Preprocessing

* Handled missing values using domain-based imputation
* Managed categorical and numerical inconsistencies
* Removed outliers and rare categories

### 🔹 Feature Engineering

* One-hot encoding for categorical variables
* Feature scaling using StandardScaler
* Structured feature alignment for prediction consistency

### 🔹 Modeling

Implemented and compared multiple models:

* Logistic Regression
* Random Forest
* XGBoost

### 🔹 Optimization

* Hyperparameter tuning using Grid Search CV
* Addressed class imbalance using weighting techniques

### 🔹 Ensemble Learning

* Combined models using **Stacking Classifier**
* Improved generalization and predictive performance

### 🔹 Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC

---

## 📂 Dataset

The model was trained using a dataset provided through a Kaggle machine learning competition on depression risk prediction. 

The dataset contains anonymized survey responses covering:

* Mental health indicators
* Lifestyle habits
* Academic/work stress factors
* Socio-demographic attributes

🔗 Kaggle Competition:
https://www.kaggle.com/competitions/playground-series-s4e11/overview

---

🏆 Kaggle Competition Submission

The trained stacking ensemble model was used to generate predictions for the Kaggle competition test dataset. These predictions were submitted to the leaderboard for evaluation.

This process demonstrated:

Model generalization on unseen data
Real-world ML evaluation workflow (train → validate → submit)
Practical deployment of a trained ML pipeline beyond local testing

---

## 🧪 Tech Stack

* **Frontend:** Streamlit
* **Backend:** Python
* **ML Libraries:** scikit-learn, XGBoost
* **Data Processing:** pandas, numpy
* **Model Storage:** joblib
* **Model Hosting:** Hugging Face

---

## ☁️ Model Hosting (Hugging Face)

Due to large file size limitations on GitHub, the trained model and preprocessing files are hosted on Hugging Face.

### 📦 Files hosted:

* `depression_prediction_stack.pkl` (final model)
* `scaler.pkl`
* `encoder.pkl`

### 🔗 Hugging Face Repo:

```
https://huggingface.co/mazeena/depression-prediction-model
```

---

## ⚙️ How the App Loads the Model

The app dynamically downloads model files using:

```python
from huggingface_hub import hf_hub_download

model_path = hf_hub_download(repo_id="mazeena/depression-prediction-model", filename="depression_prediction_stack.pkl")
```

This avoids pushing large files to GitHub and ensures smooth deployment.

---

## 🛠️ Installation (Run Locally)

### 1️⃣ Clone the repository

```bash
git clone https://github.com/FathimaMazeena/Depression-Risk-Prediction-App/
cd Depression-Risk-Prediction-App
```

---

### 2️⃣ Create virtual environment

```bash
python -m venv myenv
myenv\Scripts\activate   # Windows
```

---

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Run the app

```bash
streamlit run app.py
```

---

## 📁 Project Structure

```
├── app.py
├── MentalHealthAnalysis.py
├── requirements.txt
├── runtime.txt
├── README.md
├── .gitignore
├── .gitattributes
```

---

## ⚠️ Deployment Notes

### 🔹 Why Hugging Face is used

* GitHub limits large files (~100MB)
* ML models exceed this limit
* Hugging Face allows easy hosting + API download

---

### 🔹 Important Configuration

**runtime.txt**

```
python-3.12
```

👉 Ensures compatibility with the trained model

---

### 🔹 requirements.txt (minimal setup)

```
streamlit
pandas
numpy
scikit-learn
joblib
huggingface_hub
xgboost
```

---

## 📊 How It Works

1. User inputs personal and lifestyle data
2. Data is cleaned using `TestDataCleaner`
3. Features are encoded and scaled
4. Model predicts depression risk
5. Result is displayed instantly

---

## 🎯 Use Case

This tool can be used for:

* Early mental health awareness
* Educational demonstrations of ML in healthcare
* Research prototypes

⚠️ **Disclaimer:** This is not a medical diagnosis tool.

---

## 💡 Future Improvements

* Add probability score instead of binary output
* Improve UI/UX design
* Add user history tracking

---

## 📅 Project Details
Type: Academic Project 

Duration: Feb 2025 - Mar 2025

Affiliation: Cardiff Metropolitan University

---
## 👩‍💻 Author

**Mazeena Cader**

Software Engineering Graduate | MERN Stack Developer | ML Enthusiast

---

## 📄 License
This project is for educational purposes.

---

## ⭐ If you found this useful

Give this project a ⭐ on GitHub!

---




# 🚗 Car Price Prediction Machine Learning Web Application

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikit-learn)
![Streamlit](https://img.shields.io/badge/Streamlit-Deployed-red?logo=streamlit)
![GitHub](https://img.shields.io/badge/GitHub-Repository-black?logo=github)
![Status](https://img.shields.io/badge/Status-Live-brightgreen)

## 📌 Project Overview

The **Car Price Prediction Machine Learning Web Application** is an end-to-end machine learning project designed to estimate the selling price of used cars based on various vehicle characteristics.

Users can enter vehicle information such as brand, manufacturing year, fuel type, transmission type, mileage, engine capacity, and other specifications to receive an estimated car price instantly.

🌐 **Live App:** [Click Here to Try the App](https://car-price-prediction-machine-learning-model-knc3vjxogru7hvvuen.streamlit.app/)

---

## 🎯 Objectives

- Build a machine learning model capable of predicting used car prices
- Develop an interactive web interface for real-time predictions
- Deploy the application online for public access
- Gain practical experience in the complete machine learning lifecycle

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Language | Python |
| Data Processing | Pandas, NumPy |
| Machine Learning | Scikit-Learn, Linear Regression |
| Model Saving | Pickle |
| Web Application | Streamlit |
| Version Control | Git, GitHub |
| Deployment | Streamlit Community Cloud |

---

## 📊 Dataset

- **Dataset:** Used Car Dataset (`Cardetails.csv`)
- **Target Variable:** Selling Price

### Features Used

| Feature | Type |
|---------|------|
| Car Brand | Categorical |
| Manufacturing Year | Numerical |
| Kilometers Driven | Numerical |
| Fuel Type | Categorical |
| Seller Type | Categorical |
| Transmission Type | Categorical |
| Ownership Status | Categorical |
| Mileage | Numerical |
| Engine Capacity (CC) | Numerical |
| Maximum Power | Numerical |
| Number of Seats | Numerical |

---

## 🔄 Data Preprocessing

### Steps Performed

- Removed unnecessary data and handled missing values
- Checked for duplicate records
- Extracted vehicle brand names from car titles
- Selected relevant features for training

### Categorical Encoding

| Feature | Encoding |
|---------|----------|
| Fuel Type | Diesel → 1, Petrol → 2, LPG → 3, CNG → 4 |
| Transmission | Manual → 1, Automatic → 2 |
| Seller Type | Individual → 1, Dealer → 2, Trustmark Dealer → 3 |
| Owner | First → 1, Second → 2, Third → 3, Fourth+ → 4, Test Drive → 5 |

---

## 🤖 Machine Learning Model

**Algorithm:** Linear Regression (Scikit-Learn)

### Training Pipeline

```
Dataset Loading → Preprocessing → Feature Encoding → Train-Test Split → Model Training → Evaluation → Pickle Save
```

### Model Saving

```python
import pickle
pickle.dump(model, open("model.pkl", "wb"))
```

---

## 🌐 Web Application Features

- ✅ Interactive UI with dropdowns and sliders
- ✅ Real-time car price prediction
- ✅ Supports 30+ car brands
- ✅ User-friendly and responsive design

### How to Use

1. Select your **Car Brand**
2. Set **Manufacturing Year** and **KMs Driven**
3. Choose **Fuel Type**, **Transmission**, **Seller Type**, **Owner Type**
4. Adjust **Mileage**, **Engine CC**, **Max Power**, **Seats**
5. Click **Predict** to get the estimated price instantly!

---

## 🚀 Deployment

**Platform:** Streamlit Community Cloud

### Steps

1. Push all project files to GitHub
2. Connect GitHub repo to Streamlit Cloud
3. Configure deployment settings
4. Deploy and get a public URL

### Files Required for Deployment

```
app.py
model.pkl
Cardetails.csv
requirements.txt
Car_Price_Prediction.ipynb
```

### requirements.txt

```
streamlit
pandas
numpy
scikit-learn
```

---

## ⚠️ Challenges & Solutions

### 1. Model Loading Issue

| | Detail |
|-|--------|
| **Problem** | `FileNotFoundError` — Streamlit Cloud could not locate `model.pkl` |
| **Solution** | Used `pathlib` for correct cross-platform file path handling |

### 2. Missing Dependencies

| | Detail |
|-|--------|
| **Problem** | `ModuleNotFoundError: No module named 'sklearn'` |
| **Solution** | Added `scikit-learn` to `requirements.txt` |

### 3. Prediction Data Type Error

| | Detail |
|-|--------|
| **Problem** | `ValueError` during `model.predict()` due to string inputs |
| **Solution** | Converted all inputs to numeric: `input_data_model.apply(pd.to_numeric)` |

---

## 💡 Key Learning Outcomes

- Building end-to-end machine learning pipelines
- Developing interactive web apps with Streamlit
- Deploying ML models to cloud platforms
- Debugging real-world production issues
- Managing project dependencies for deployment

---

## 📁 Project Structure

```
Car-Price-Prediction/
│
├── app.py                        # Streamlit web application
├── Car_Price_Prediction.ipynb    # Jupyter Notebook (EDA + Model Training)
├── Cardetails.csv                # Dataset
├── model.pkl                     # Trained ML model
└── requirements.txt              # Dependencies
```

---

## ▶️ Run Locally

```bash
# Clone the repository
git clone https://github.com/tanvir-50198/Car-Price-Prediction-Machine-Learning-Model.git

# Navigate to project folder
cd Car-Price-Prediction-Machine-Learning-Model

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```

---

## 👨‍💻 Author

**Tanvir Rahman**
- 🌐 [Live App](https://car-price-prediction-machine-learning-model-knc3vjxogru7hvvuen.streamlit.app/)
- 💻 [GitHub](https://github.com/tanvir-50198)
- 💼 [LinkedIn](https://www.linkedin.com/in/tanvir-50198)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

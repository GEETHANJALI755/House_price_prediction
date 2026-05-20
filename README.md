# 🏠 House Price Prediction Using Machine Learning

## 📌 Project Overview
This project predicts house prices using Machine Learning techniques based on various house features such as bedrooms, bathrooms, living area, lot size, location, house age, and renovation status.

The project includes:
- Data preprocessing and feature engineering
- Training multiple machine learning models
- Model evaluation and overfitting analysis
- Deployment using Streamlit

---

## 🎯 Objective
The main objective of this project is to build an accurate machine learning model that can estimate the price of a house based on its characteristics.

---

## 📂 Dataset
The project uses the **King County House Sales Dataset** (`kc_house_data.csv`), which contains house sale records from King County, Washington, USA.

### Important Features
- bedrooms
- bathrooms
- sqft_living
- sqft_lot
- floors
- waterfront
- view
- condition
- grade
- sqft_basement
- latitude
- longitude
- house_age
- is_renovated

### Target Variable
- `price`

---

## 🧹 Data Preprocessing
The following preprocessing steps were performed:
1. Removed unnecessary columns (`id`, `zipcode`)
2. Converted the date column to datetime format
3. Created `house_age`
4. Created `is_renovated`
5. Removed redundant columns
6. Checked for missing values and duplicates
7. Split data into training and testing sets
8. Applied feature scaling where required

---

## 🤖 Machine Learning Models Used

### 1. Linear Regression
A baseline model used to establish a simple relationship between features and house price.

### 2. Random Forest Regressor
An ensemble model that combines multiple decision trees to improve prediction accuracy.

### 3. XGBoost Regressor
A gradient boosting model that provided the best performance in this project.

---

## 📊 Evaluation Metrics
The models were evaluated using:
- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)

---

## 🔍 Overfitting Check
Overfitting was analyzed by comparing:
- Training Score
- Testing Score
- Difference between train and test scores

A smaller difference indicates better generalization.

---

## 🏆 Best Model
XGBoost Regressor achieved the highest accuracy and best generalization performance, and was selected as the final model.

---

## 💾 Model Saving
The trained XGBoost model was saved using Python's `pickle` module as:

- `house_price_model.pkl`

This file is used during deployment to make predictions without retraining the model.

---

## 🌐 Deployment
The model was deployed using Streamlit.

### Deployment Features
- User-friendly web interface
- Input fields for house details
- Real-time price prediction

### Run the Application
```bash
python -m streamlit run app.py

House_Price_Prediction/
│── project.ipynb
│── kc_house_data.csv
│── house_price_model.pkl
│── app.py
│── README.md

▶️ Usage
Train the model using project.ipynb
Generate house_price_model.pkl
Run the Streamlit app
Enter house details
Click Predict Price
View the estimated house price

📝 Conclusion

This project demonstrates how machine learning can be used to accurately predict house prices. By comparing multiple models and evaluating their performance, XGBoost was identified as the best-performing model. The final solution was deployed as an interactive web application using Streamlit.

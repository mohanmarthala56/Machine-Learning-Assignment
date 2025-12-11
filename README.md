# Car Price Prediction Using a Multilayer Perceptron (MLP)

This project applies a **Multilayer Perceptron (MLP)** neural network to predict car prices using mixed-type vehicle attributes such as mileage, engine power, brand, fuel type, and vehicle age.  
The goal is to demonstrate how neural networks can model nonlinear relationships in real-world regression problems.

This README summarises the work described in the full project report.
---

## 🚗 Project Overview

Car pricing varies based on several interacting factors such as technical specs, brand reputation, usage, and condition.  
Traditional linear models often struggle with such nonlinear interactions—an MLPRegressor is better suited to handle these complexities.

This project demonstrates:

- Data preprocessing (encoding + scaling)
- Neural network regression with Scikit-learn
- Evaluation using R², MAE, and visual analysis
- Understanding strengths, limitations, and ethical considerations

---

## 📊 Dataset

The dataset (`car_prediction_data.csv`) contains:

### **Categorical Features**
- Brand  
- Model  
- Fuel type  
- Transmission  

### **Numeric Features**
- Mileage  
- Engine power  
- Engine size  
- Year of manufacture  
- Other descriptive attributes  

### **Target Variable**
- **Price** (continuous)

A histogram of the price column shows a long right-tail distribution (high-value outliers).  
Details in the report.

---

## 🧠 Methodology

### **1. Preprocessing**
- Split into features (X) and label (y)
- One-Hot Encoding for categorical attributes
- StandardScaler for numeric attributes
- Train–test split (80/20, random_state=42)

### **2. MLP Architecture**

| Component | Value |
|----------|--------|
| Hidden Layers | (64, 32) |
| Activation | ReLU |
| Optimizer | Adam |
| Regularization | α = 1e-4 |
| Iterations | 300 |


Shows low average prediction error.

### **True vs Predicted Plot**
- Tight clustering around diagonal for most cars  
- Wider spread for high-priced vehicles (higher variance in data)

More interpretation in the report. :contentReference[oaicite:3]{index=3}

---

## 🧪 Potential Improvements

- Hyperparameter tuning (hidden layers, neurons, learning rates)
- Log-transforming price to reduce skew
- Using XGBoost, Random Forest, CatBoost for comparison
- Feature importance analysis
- Add early stopping or increase training iterations

---

## ⚖️ Ethical Considerations

Although car price prediction has fewer risks than medical/financial domains, caution is still needed:

- Automated pricing tools may reinforce market biases
- Users should not rely solely on model predictions
- Data transparency is important
- Predictions should guide—not replace—human judgment

---

## 📚 References

- Scikit-learn Documentation  
- Bishop, C. (2006). *Pattern Recognition and Machine Learning*  
- Automotive pricing datasets (generic references)  
- Course lecture materials on neural networks and preprocessing  

---

## 📎 GitHub Repository

https://github.com/mohanmarthala56/Machine-Learning-Assignment.git

---

## 📝 License

This project is released under the **MIT License** (see LICENSE file).





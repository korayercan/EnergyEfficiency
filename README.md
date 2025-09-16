# EnergyEfficiency

## 📌 Project Overview
This project explores **machine learning models for predicting building energy efficiency**.  
The dataset contains **eight architectural features** and two target variables:

- **Heating Load (y1)**  
- **Cooling Load (y2)**  

The goal is to evaluate different regression algorithms and compare their performance on both targets.

---

## 📊 Dataset
- Source: [UCI Energy Efficiency Dataset](https://archive.ics.uci.edu/ml/datasets/Energy+efficiency)  
- Features:  
  - X1: Relative Compactness  
  - X2: Surface Area  
  - X3: Wall Area  
  - X4: Roof Area  
  - X5: Overall Height  
  - X6: Orientation (categorical)  
  - X7: Glazing Area  
  - X8: Glazing Area Distribution (categorical)  
- Targets:  
  - y1: Heating Load  
  - y2: Cooling Load  

Categorical features were encoded with **One-Hot Encoding**, numerical features were standardized.

---

## 🧠 Models Tested
The following regression models were implemented using `scikit-learn` Pipelines:

- Linear Regression  
- RidgeCV  
- LassoCV  
- ElasticNetCV  
- DecisionTreeRegressor (with and without GridSearch hyperparameter tuning)  
- (SVR experiments prepared, optional GridSearch tuning)  

Each model was trained separately for **Heating Load** and **Cooling Load**.

---

## 📈 Results
Performance was evaluated using **MSE**, **MAE**, and **R²**.  

**Heating Load**  
- Linear models: MSE ≈ 9, R² ≈ 0.917  
- Decision Tree: MSE ≈ 0.40, R² ≈ 0.996 (possible overfitting, to be validated with CV)  

**Cooling Load**  
- Linear models: MSE ≈ 12.5, R² ≈ 0.877  
- Decision Tree: MSE ≈ 7.67, R² ≈ 0.924 (GridSearch improved to MSE ≈ 6.16, R² ≈ 0.939)  

---

## ⚙️ Usage
- Open the project in **Google Colab** by clicking the Colab button in the notebook (`.ipynb`) file.  
- Or clone the repository and run locally:

```bash
# Clone the repository
git clone https://github.com/korayercan/EnergyEfficiency.git
cd EnergyEfficiency

# Install requirements
pip install -r requirements.txt

# Run the notebook
jupyter notebook notebooks/energy_efficiency.ipynb
```

# Maritime-Container-Throughput-Forecasting-Through-Hybrid-Statistical-and-Machine-Learning-Models

## 📌 Project Overview

This repository contains the research work and implementation developed for my Master’s Thesis:

**“Maritime Container Throughput Forecasting using Statistical, Machine Learning, and Hybrid Models.”**

The study investigates how statistical time-series models and advanced machine learning algorithms can be applied to forecast monthly maritime container throughput (TEUs). The research evaluates whether hybrid modeling frameworks can improve predictive accuracy by combining linear time-series modeling with nonlinear residual learning.

The objective is to provide a robust forecasting framework to support port authorities, logistics planners, and policymakers in improving operational efficiency and strategic decision-making.

---

## 🎯 Research Objectives

- Develop accurate forecasting models for monthly maritime container throughput.
- Implement and compare statistical time-series models (SARIMA, SARIMAX).
- Apply machine learning models (Random Forest, XGBoost).
- Develop hybrid models:
  - SARIMAX + Random Forest  
  - SARIMAX + XGBoost  
- Evaluate whether hybrid frameworks improve predictive accuracy.
- Analyze the influence of macroeconomic and trade-related indicators.
- Provide methodological insights for real-world maritime forecasting applications.

---

## ⚙️ Methodology

### Data Source

Monthly maritime container throughput dataset including:

- Export (constant & current USD)
- Import (constant & current USD)
- Industrial production
- Retail market index

### Data Preprocessing

- Convert Date column to datetime format
- Set monthly frequency (Month End)
- Sort chronologically
- Select target and exogenous variables
- Validate missing values
- Chronological Train–Validation–Test split (70%–15%–15%)

### Feature Engineering

For machine learning and residual modeling:

- Lag features (1, 2, 3, 4, 5, 6, 12)
- Seasonal lag (12 months)
- Rolling mean (3-month)
- Rolling standard deviation (3-month)
- Month feature for seasonality

---

## 🧠 Models Implemented

### 1️⃣ Statistical Models
- SARIMA
- SARIMAX (with exogenous variables)

### 2️⃣ Machine Learning Models
- Random Forest Regressor
- XGBoost Regressor

### 3️⃣ Hybrid Models

Hybrid framework:

Ŷ(t)_Hybrid = Ŷ(t)_SARIMAX + ê(t)_ML

Where:
- SARIMAX captures trend, seasonality, autocorrelation, and exogenous effects.
- ML model learns nonlinear residual patterns.

---

## 📊 Evaluation Metrics

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- Mean Absolute Percentage Error (MAPE)
- Residual diagnostics (ACF, Ljung-Box test)

---

---

## 📈 Key Findings

- Machine learning models outperform standalone statistical models.
- XGBoost achieves strong predictive performance due to boosting optimization.
- Hybrid models capture nonlinear residual structure.
- SARIMAX effectively models economic drivers and seasonality.
- Hybrid SARIMAX + XGBoost reduces forecasting error compared to standalone SARIMAX.

Approximate model performance comparison:

| Model | MAPE |
|-------|------|
| SARIMAX | ~9.1% |
| Random Forest | ~6.3% |
| XGBoost | ~5.9% |
| SARIMAX + XGBoost | ~8.5% |

---

## 💻 Installation & Usage

### Requirements

- Python 3.8+
- Jupyter Notebook

### Required Libraries

- numpy
- pandas
- matplotlib
- statsmodels
- scikit-learn
- xgboost


cd maritime-throughput-forecasting

### Install Dependencies

### Run Notebook

Run cells sequentially to reproduce experiments and results.

---

## 🔬 Hybrid Modeling Framework

Stage 1 – SARIMAX  
- Models linear structure  
- Captures trend and seasonality  
- Incorporates exogenous variables  

Stage 2 – Machine Learning Residual Model  
- Learns nonlinear residual structure  
- Uses lagged residual features  
- Applies recursive forecasting  

Final Forecast:

Forecast = SARIMAX Prediction + ML Residual Prediction

This approach combines interpretability with predictive strength.

---

## 🔒 Ethical Considerations

- Dataset used strictly for academic research.
- No personal or sensitive data involved.
- Transparent and reproducible modeling process.

---

## 🚀 Future Work

- LSTM-based deep learning models
- Transformer-based time-series forecasting
- Real-time forecasting dashboard
- SHAP-based explainable AI analysis
- Multivariate deep hybrid frameworks

---

## 👨‍💻 Author

**Pakanati Mohan Gandhi**  
MSc Data Science, AI & Digital Business  
GISMA University of Applied Sciences  
Berlin, Germany  

---

## 📚 Citation

If you use this work, please cite:

Pakanati Mohan Gandhi,  
“Maritime Container Throughput Forecasting using Statistical, Machine Learning, and Hybrid Models.”  
Master’s Thesis, 2026.

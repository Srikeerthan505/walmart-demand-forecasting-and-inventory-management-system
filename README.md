# 🛒 Walmart Demand Forecasting & Inventory Optimization System

[![Python 3.10](https://img.shields.io/badge/Python-3.10-blue.svg)](https://www.python.org/)
[![Streamlit Deployed](https://img.shields.io/badge/Streamlit-Deployed-FF4B4B.svg)](https://walmart-demand-forecasting-keerthan.streamlit.app/)
[![Model ARIMA & LSTM](https://img.shields.io/badge/Models-ARIMA%20%7C%20LSTM-orange.svg)]()
[![Dataset Scale](https://img.shields.io/badge/Dataset-400K%2B%20Records-success.svg)]()

> **Live Application:** [View the Interactive Streamlit Dashboard Here](https://walmart-demand-forecasting-keerthan.streamlit.app/)

## 📌 Business Overview

An end-to-end predictive analytics pipeline designed to solve the retail "Goldilocks Problem": preventing out-of-stock scenarios (lost revenue) while minimizing overstock (tied-up capital). By analyzing a massive historical dataset and integrating exogenous variables, this system forecasts localized departmental demand to recommend highly optimized weekly inventory levels.

## 🧠 Key Technical Engineering

* **Multivariate Deep Learning:** Engineered an LSTM neural network architecture to capture complex, non-linear demand shocks (e.g., extreme weather events, holiday spikes) that traditional statistical models miss.
* **Statistical Baselining:** Implemented ARIMA to capture baseline linear trends and standard retail seasonality.
* **Advanced Feature Engineering:** Processed over 400,000 records, engineering lag features ($t-7$, $t-30$), handling missing markdown data, and encoding critical holiday impacts (Super Bowl, Thanksgiving).
* **Production Deployment:** Built an interactive, caching-optimized (`@st.cache_data`) Streamlit web application for real-time stakeholder inference.

## 🛠️ Tech Stack

| Domain | Tools Used |
| :--- | :--- |
| **Core & Data Wrangling** | Python, Pandas, NumPy |
| **Time Series & Stats** | Statsmodels (ARIMA) |
| **Deep Learning** | TensorFlow / Keras (LSTM) |
| **Deployment & UI** | Streamlit |

## 📁 Project Architecture

The repository is structured to separate exploratory data science from production software engineering:

```text
WALMART-DEMAND-FORECASTING/
├── data/                  # Sample datasets (Full 400k dataset ignored via .gitignore)
├── notebooks/             # Exploratory phase: "Showing the Math"
│   ├── 01_EDA_and_Cleaning.ipynb
│   ├── 02_Feature_Engineering.ipynb
│   └── 03_Model_Evaluation_ARIMA_vs_LSTM.ipynb
├── src/                   # Production modular scripts
│   ├── data_loader.py     
│   ├── preprocess.py      
│   ├── model.py           
│   ├── lstm_model.py      
│   └── metrics.py         
├── app.py                 # Streamlit application entry point
├── requirements.txt       
└── README.md
```

## ▶️ Run Locally 
1. Clone the repository:
   git clone [https://github.com/Srikeerthan505/walmart-forecast](https://github.com/Srikeerthan505/walmart-forecast)
cd WALMART-DEMAND-FORECASTING
2. Install the required dependencies:
   pip install -r requirements.txt
3. Launch the Streamlit app:
   streamlit run app.py

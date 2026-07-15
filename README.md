# 🌾 Food Security Early Warning System for East Java (EWS-Jatim)

> **A Web-Based Early Warning System for Rice Production Forecasting and Food Security Monitoring in East Java Using SARIMAX and Hierarchical Bayesian Time Series**

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?logo=fastapi)
![React](https://img.shields.io/badge/React-Frontend-61DAFB?logo=react)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Under%20Development-orange)
![Research](https://img.shields.io/badge/Research-Bachelor%20Thesis-success)

---

# 📌 Overview

Food Security Early Warning System for East Java (**EWS-Jatim**) is a research-based web application developed to forecast monthly rice production and monitor regional food security across **38 districts/cities in East Java, Indonesia**.

The system integrates **Earth Observation (EO)** data, historical rice production records, demographic information, and rice consumption statistics to generate accurate forecasts using:

- **SARIMAX (Seasonal ARIMA with Exogenous Variables)**
- **Hierarchical Bayesian Time Series (HBTS)**

Forecast results are transformed into food security indicators through the **Food Security Ratio (FSR)**, enabling early identification of districts potentially facing food shortages.

---

# 🎯 Research Objectives

This project aims to:

- Forecast monthly rice production at district level.
- Compare SARIMAX and HBTS forecasting performance.
- Quantify forecasting uncertainty using Bayesian inference.
- Estimate regional rice availability and demand.
- Calculate Food Security Ratio (FSR).
- Develop a web-based Early Warning System.
- Support evidence-based decision making for food security management.

---

# 🌾 Research Workflow

```
Historical Data
       │
       ▼
Data Cleaning & Validation
       │
       ▼
Master Dataset Construction
       │
       ▼
Exploratory Data Analysis
       │
       ▼
Feature Engineering
       │
       ▼
SARIMAX
       │
       ├───────────────┐
       ▼               ▼
HBTS         Model Evaluation
       │
       ▼
Rice Production Forecast
       │
       ▼
Rice Availability Estimation
       │
       ▼
Food Security Ratio (FSR)
       │
       ▼
Early Warning Classification
       │
       ▼
Interactive Dashboard
```

---

# ✨ Key Features

## 📈 Rice Production Forecasting

Forecast monthly rice production using:

- SARIMAX
- Hierarchical Bayesian Time Series

---

## 🌾 Food Security Assessment

Automatically estimate:

- Rice Production
- Rice Availability
- Rice Demand
- Food Security Ratio (FSR)
- Deficit Probability
- Food Security Status

| Food Security Ratio | Status |
|--------------------|--------|
| ≥ 1.20 | 🟢 Safe |
| 1.00 – <1.20 | 🟡 Alert |
| <1.00 | 🔴 Critical |

---

## 🗺 Interactive GIS Dashboard

Interactive district-level visualization featuring:

- Choropleth Maps
- Risk Classification
- District Comparison
- Time Series Visualization
- Filtering
- Interactive Pop-up Information

---

## 📊 Analytics Dashboard

Dashboard modules include:

- Historical Production Trends
- Forecast Visualization
- Environmental Monitoring
- Food Security Monitoring
- District Comparison
- Forecast Performance
- Model Evaluation

---

## 📥 Export

Export:

- Forecast Results
- Reports
- Tables
- Charts

---

# 📂 Dataset

The project integrates multiple official datasets.

## 🌾 Rice Production

| Item | Description |
|------|-------------|
| Source | Badan Pusat Statistik (BPS) |
| Frequency | Monthly |
| Level | District / City |
| Period | Jan 2018 – Apr 2026 |

---

## 🌍 Earth Observation Variables

Monthly environmental indicators:

- NDVI
- Rainfall
- Air Temperature
- Soil Moisture

Sources:

- Google Earth Engine
- CHIRPS
- NASA POWER

---

## 👥 Population

Source:

- Badan Pusat Statistik

Frequency:

Annual

---

## 🍚 Rice Consumption

Source:

- SUSENAS
- Badan Pusat Statistik

---

# 🧹 Data Pipeline

```
Raw Data
    │
    ▼
Cleaning
    │
    ▼
Missing Value Handling
    │
    ▼
Validation
    │
    ▼
Integration
    │
    ▼
Master Dataset
    │
    ▼
EDA
    │
    ▼
Feature Engineering
    │
    ▼
Forecasting Models
```

---

# 📊 Feature Engineering

The following preprocessing and feature engineering steps are applied before forecasting:

- Missing Value Handling
- Duplicate Checking
- Outlier Inspection
- Time Series Validation
- Rolling Statistics
- Moving Average
- Cross-Correlation Function (CCF)
- Lag Selection
- Exogenous Lag Features
- Seasonal Dummy Variables
- Multicollinearity Analysis (VIF)
- Train/Test Split

---

# 🧠 Forecasting Models

## 1. SARIMAX

Seasonal ARIMA with Exogenous Variables.

### Exogenous Variables

- NDVI
- Rainfall
- Air Temperature
- Soil Moisture

---

## 2. Hierarchical Bayesian Time Series (HBTS)

Bayesian hierarchical model using partial pooling across districts.

Advantages:

- Probabilistic Forecasting
- Credible Interval
- Posterior Distribution
- Uncertainty Quantification
- Partial Pooling
- Robust Prediction

---

# 📊 Model Evaluation

Forecasting performance is evaluated using:

- RMSE
- MAE
- MAPE
- R²

HBTS additionally evaluates:

- Posterior Predictive Distribution
- 95% Credible Interval
- Uncertainty Coverage

---

# 🏗 System Architecture

```
                React Dashboard
                       │
                REST API (FastAPI)
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
    SARIMAX          HBTS      Data Processing
        │              │
        └───────┬──────┘
                ▼
          Forecast Results
                │
                ▼
      Food Security Analysis
                │
                ▼
       Early Warning Dashboard
```

---

# 🛠 Technology Stack

## Backend

- FastAPI
- Python

## Frontend

- React
- Tailwind CSS
- Plotly
- React Leaflet

## Machine Learning

- Pandas
- NumPy
- Statsmodels
- PyMC
- ArviZ
- Scikit-learn

## Visualization

- Plotly
- GeoJSON
- Leaflet

## Development

- Git
- GitHub
- VS Code
- Jupyter Notebook

---

# 📁 Repository Structure

```
food-security-ews-jatim/

│
├── data/
│   ├── raw/
│   ├── external/
│   ├── interim/
│   ├── processed/
│   └── final/
│
├── models/
│   ├── sarimax/
│   ├── hbts/
│   └── artifacts/
│
├── notebooks/
│   ├── 01_data_validation.ipynb
│   ├── 02_time_series_eda.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_sarimax.ipynb
│   ├── 05_hbts.ipynb
│   └── 06_ews.ipynb
│
├── reports/
│   ├── figures/
│   ├── tables/
│   └── results/
│
├── src/
│   ├── preprocessing/
│   ├── features/
│   ├── modeling/
│   ├── forecasting/
│   └── ews/
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

# 🚀 Getting Started

Clone the repository

```bash
git clone https://github.com/yourusername/food-security-ews-jatim.git
```

Install dependencies

```bash
pip install -r requirements.txt
```

Run Jupyter Notebook

```bash
jupyter notebook
```

---

# 📅 Development Roadmap

## Phase 1

- Literature Review
- Proposal Development
- Data Collection

## Phase 2

- Data Cleaning
- Validation
- Dataset Integration
- EDA
- Feature Engineering

## Phase 3

- SARIMAX
- HBTS
- Model Evaluation

## Phase 4

- FastAPI Backend
- React Frontend
- GIS Dashboard
- Interactive Visualization

## Phase 5

- Deployment
- Documentation
- Thesis Finalization

---

# 👥 Team

**Bachelor of Data Science**

Telkom University Surabaya

Project Members

- Alfia Damayanti
- Auliya Ardhini Putri
- Ayunda Dewi Agustin

---

# 📖 Research

This repository supports:

- Bachelor's Thesis
- Internship Project

**Thesis Title**

> *Food Security Early Warning System Based on Rice Production Forecasting Using SARIMAX and Hierarchical Bayesian Time Series in East Java Province*

---

# 📄 License

Licensed under the MIT License.

---

# 🙏 Acknowledgements

This research is conducted as part of the Bachelor's Thesis and Internship Program at **Telkom University Surabaya**, with support from the **Department of Food Security and Agriculture, Surabaya City Government**.

Special thanks to all open-data providers, including **BPS**, **Google Earth Engine**, **NASA POWER**, and **CHIRPS**, for making this research possible.
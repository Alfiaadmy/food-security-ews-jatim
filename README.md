# 🌾 Food Security Early Warning System for East Java (EWS-Jatim)

> **A Web-Based Early Warning System for Rice Production Forecasting and Food Security Monitoring in East Java Using SARIMAX and Hierarchical Bayesian Time Series**

---

## 📌 Project Overview

Food Security Early Warning System (EWS-Jatim) is a web-based decision support system designed to provide early warnings regarding rice production and food security conditions across districts/cities in East Java, Indonesia.

The system integrates historical agricultural production data with environmental variables to forecast future rice production and estimate food security conditions using the **Food Security Ratio (FSR)**.

This project combines statistical forecasting, Bayesian hierarchical modeling, interactive visualization, and geospatial analysis into one integrated platform that can support government agencies and stakeholders in monitoring regional food security.

---

## 🎯 Objectives

The main objectives of this project are:

- Forecast monthly rice production for every district/city in East Java.
- Compare forecasting performance between SARIMAX and Hierarchical Bayesian Time Series (HBTS).
- Develop an Early Warning System (EWS) for food security.
- Visualize forecasting results through an interactive dashboard.
- Assist policymakers in identifying areas with potential food insecurity.

---

# 🚀 Key Features

### 📈 Rice Production Forecast

Forecast monthly rice production using:

- SARIMAX
- Hierarchical Bayesian Time Series (HBTS)

---

### 🌾 Food Security Ratio (FSR)

Automatically calculate:

- Rice Availability
- Rice Demand
- Food Security Ratio

Classification:

| FSR | Status |
|------|---------|
| ≥ 1.20 | 🟢 Safe |
| 1.00 – <1.20 | 🟡 Alert |
| <1.00 | 🔴 Critical |

---

### 🗺 Interactive Map

Display district-level food security conditions using an interactive map.

Features:

- Choropleth Map
- Color-based Risk Classification
- Popup Information
- Zoom & Navigation

---

### 📊 Interactive Dashboard

Visualize:

- Production Trends
- Forecast Results
- Exogenous Variables
- Food Security Status
- District Comparison
- Monthly Analysis

---

### 📥 Export Result

Users can export:

- Forecast Results
- Food Security Reports
- Charts
- Tables

---

# 🧠 Forecasting Models

## 1. SARIMAX

Seasonal AutoRegressive Integrated Moving Average with Exogenous Variables

Exogenous Variables:

- NDVI
- Rainfall
- Soil Moisture
- Air Temperature

---

## 2. Hierarchical Bayesian Time Series (HBTS)

Hierarchical Bayesian model with partial pooling across districts.

Advantages:

- Probabilistic Forecast
- Credible Interval
- Uncertainty Estimation
- Information Sharing Between Districts

---

# 📂 Dataset

The system uses historical data collected from several official sources.

### Rice Production

- Monthly Rice Production
- District/City Level
- 2018–2024

Source:
- BPS (Statistics Indonesia)

---

### Exogenous Variables

- NDVI
- Rainfall
- Air Temperature
- Soil Moisture

Sources:

- Google Earth Engine
- CHIRPS
- NASA POWER

---

### Population

District Population

Source:

- BPS

---

### Rice Consumption

Average Rice Consumption per Capita

Source:

- SUSENAS / BPS

---

# 🏗 System Architecture

```
                    React Dashboard
                           │
                           │ REST API
                           ▼
                      FastAPI Backend
                           │
        ┌──────────────────┼─────────────────┐
        ▼                  ▼                 ▼
     SARIMAX            HBTS           Data Processing
        │                  │                 │
        └──────────────────┼─────────────────┘
                           ▼
                    Master Dataset
```

---

# 🛠 Tech Stack

## Frontend

- React
- Tailwind CSS
- Plotly.js
- React Leaflet
- Axios

---

## Backend

- FastAPI
- Python

---

## Data Science

- Pandas
- NumPy
- Scikit-Learn
- Statsmodels
- PyMC
- ArviZ

---

## Visualization

- Plotly
- Leaflet
- GeoJSON

---

## Development

- Git
- GitHub
- VS Code
- Jupyter Notebook

---

# 📁 Project Structure

```
food-security-ews-jatim/

│

├── app/
│   ├── backend/
│   ├── frontend/
│   ├── api/
│   └── assets/
│
├── data/
│   ├── raw/
│   ├── interim/
│   ├── processed/
│   └── external/
│
├── notebooks/
│
├── models/
│
├── reports/
│   ├── figures/
│   └── tables/
│
├── docs/
│
├── tests/
│
├── config/
│
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
└── CHANGELOG.md
```

---

# 🔄 Workflow

```
Raw Data
      │
      ▼
Data Cleaning
      │
      ▼
Master Dataset
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Feature Engineering
      │
      ▼
SARIMAX Model
      │
      ▼
HBTS Model
      │
      ▼
Forecast
      │
      ▼
Food Security Ratio
      │
      ▼
Early Warning Classification
      │
      ▼
Interactive Dashboard
```

---

# 📊 Dashboard Modules

- Home
- Overview
- Rice Production
- Forecast
- Early Warning
- Interactive Map
- District Analysis
- Model Comparison
- Download Report

---

# 📅 Development Roadmap

## Phase 1

- [x] Literature Review
- [x] Proposal
- [x] Dataset Collection

---

## Phase 2

- [ ] Data Cleaning
- [ ] Master Dataset
- [ ] Exploratory Data Analysis

---

## Phase 3

- [ ] SARIMAX Development
- [ ] HBTS Development
- [ ] Model Evaluation

---

## Phase 4

- [ ] FastAPI Backend
- [ ] React Frontend
- [ ] Interactive Dashboard

---

## Phase 5

- [ ] Deployment
- [ ] Documentation
- [ ] Final Report

---

# 👥 Team

**Data Science Undergraduate Program**

Telkom University Surabaya

Project Members:

- Alfia Damayanti
- Auliya Ardhini Putri
- Ayunda Dewi Agustin

---

# 📖 Research

This repository is part of:

**Bachelor Thesis**

> Early Warning System Kerentanan Pangan Berbasis Forecasting Produksi Padi Menggunakan SARIMAX dan Hierarchical Bayesian Time Series di Provinsi Jawa Timur

and

**Internship Project**

Department of Food Security and Agriculture, Surabaya City.

---

# 📜 License

This project is released under the MIT License.

---

# ⭐ Future Development

Potential future improvements include:

- PostgreSQL Integration
- Docker Deployment
- Authentication & Authorization
- Automated Data Pipeline
- Real-time Weather Integration
- Multi-Crop Forecasting
- Cloud Deployment
- Mobile Responsive Dashboard

---

> Developed with ❤️ using Python, React, FastAPI, and Bayesian Statistics.
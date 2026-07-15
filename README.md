# 🌾 Food Security Early Warning System for East Java (EWS-Jatim)

> **A Web-Based Early Warning System for Rice Production Forecasting and Food Security Monitoring in East Java Using SARIMAX and Hierarchical Bayesian Time Series**

---

## 📌 Project Overview

The **Food Security Early Warning System for East Java (EWS-Jatim)** is a web-based decision support system developed to provide early warnings regarding rice production and regional food security across **38 districts/cities** in East Java, Indonesia.

The system integrates historical rice production data with environmental variables derived from Earth Observation (EO) datasets to forecast future rice production and estimate regional food security conditions using the **Food Security Ratio (FSR)**.

This project combines **time series forecasting**, **Bayesian hierarchical modeling**, **geospatial visualization**, and **interactive dashboards** into a single platform that supports evidence-based decision making for government agencies, researchers, and other stakeholders in the agricultural sector.

---

## 🎯 Project Objectives

The primary objectives of this project are to:

* Forecast monthly rice production for each district/city in East Java.
* Compare the forecasting performance of **SARIMAX** and **Hierarchical Bayesian Time Series (HBTS)** models.
* Develop an Early Warning System (EWS) for regional food security monitoring.
* Estimate rice availability, demand, and Food Security Ratio (FSR).
* Visualize forecasting results through an interactive web dashboard.
* Support policymakers in identifying districts with potential food insecurity.

---

# 🚀 Key Features

## 📈 Rice Production Forecasting

Forecast monthly rice production using two complementary approaches:

* **SARIMAX (Seasonal ARIMA with Exogenous Variables)**
* **Hierarchical Bayesian Time Series (HBTS)**

---

## 🌾 Food Security Ratio (FSR)

Automatically calculate:

* Rice Production
* Estimated Rice Availability
* Population-Based Rice Demand
* Food Security Ratio (FSR)

### Food Security Classification

| Food Security Ratio (FSR) | Status      |
| ------------------------: | :---------- |
|                    ≥ 1.20 | 🟢 Safe     |
|             1.00 – < 1.20 | 🟡 Alert    |
|                    < 1.00 | 🔴 Critical |

---

## 🗺 Interactive GIS Dashboard

Visualize district-level food security conditions through an interactive map.

Features include:

* Choropleth Map
* Risk-Based Color Classification
* Interactive Pop-up Information
* Zoom & Navigation
* District Filtering

---

## 📊 Interactive Analytics Dashboard

Dashboard modules include:

* Historical Production Trends
* Forecast Results
* Exogenous Variable Monitoring
* Food Security Status
* District Comparison
* Monthly Time Series Analysis
* Model Performance Evaluation

---

## 📥 Export & Reporting

Generate downloadable outputs including:

* Forecast Results
* Food Security Reports
* Charts
* Summary Tables

---

# 🧠 Forecasting Models

## 1. SARIMAX

Seasonal AutoRegressive Integrated Moving Average with Exogenous Variables.

### Exogenous Variables

* NDVI (Normalized Difference Vegetation Index)
* Rainfall
* Air Temperature
* Soil Moisture

---

## 2. Hierarchical Bayesian Time Series (HBTS)

A Bayesian hierarchical model that applies **partial pooling** across districts/cities to improve forecasting performance.

### Advantages

* Probabilistic Forecasting
* Credible Intervals
* Uncertainty Quantification
* Information Sharing Across Districts
* Improved Forecast Stability for Limited Data

---

# 📂 Dataset

The project utilizes integrated datasets collected from multiple official and open-access sources.

## 🌾 Rice Production

**Level:** District/City (Monthly)

**Period:** January 2018 – April 2026

**Source:**

* Badan Pusat Statistik (BPS)

---

## 🌍 Environmental (Exogenous) Variables

Monthly environmental indicators extracted from satellite and climate datasets:

* NDVI
* Rainfall
* Air Temperature
* Soil Moisture

**Sources**

* Google Earth Engine (GEE)
* CHIRPS
* NASA POWER

---

## 👥 Population Data

**Level:** District/City (Annual)

**Period:** 2018–2026

**Source**

* Badan Pusat Statistik (BPS)

---

## 🍚 Rice Consumption

Average annual rice consumption per capita.

**Period:** 2018–2025

**Source**

* SUSENAS
* Badan Pusat Statistik (BPS)

---

# 🧹 Data Preparation Pipeline

The master dataset is constructed through several preprocessing stages:

* Data Collection
* Data Cleaning
* Missing Value Handling
* Duplicate Checking
* District Name Standardization
* Dataset Validation
* Data Integration
* Master Dataset Construction

The resulting master dataset consists of:

* **38 Districts/Cities**
* **3,800 Monthly Observations**
* Integrated production, environmental, demographic, and consumption variables.

---

# 🏗 System Architecture

```text
                    React Dashboard
                           │
                    RESTful API
                           │
                           ▼
                    FastAPI Backend
                           │
      ┌────────────────────┼────────────────────┐
      ▼                    ▼                    ▼
   SARIMAX              HBTS            Data Processing
      │                    │                    │
      └────────────────────┼────────────────────┘
                           ▼
                    Master Dataset
                           │
                           ▼
               Food Security Early Warning
```

---

# 🛠 Technology Stack

## Frontend

* React
* Tailwind CSS
* Plotly.js
* React Leaflet
* Axios

---

## Backend

* FastAPI
* Python

---

## Data Science & Machine Learning

* Pandas
* NumPy
* Statsmodels
* PyMC
* ArviZ
* Scikit-Learn

---

## Data Visualization

* Plotly
* Leaflet
* GeoJSON

---

## Development Tools

* Git
* GitHub
* Visual Studio Code
* Jupyter Notebook

---

# 📁 Project Structure

```text
food-security-ews-jatim/

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

```text
Raw Data
      │
      ▼
Data Cleaning
      │
      ▼
Data Validation
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
Forecasting
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

# 📊 Dashboard Modules

* Home
* Overview
* Rice Production
* Forecasting
* Early Warning
* Interactive Map
* District Analysis
* Model Comparison
* Download Report

---

# 📅 Development Roadmap

## Phase 1 — Research & Planning

* [x] Literature Review
* [x] Proposal Development
* [x] Dataset Collection

---

## Phase 2 — Data Engineering

* [x] Data Cleaning
* [x] Data Validation
* [x] Master Dataset Construction
* [ ] Exploratory Data Analysis
* [ ] Feature Engineering

---

## Phase 3 — Forecasting Models

* [ ] SARIMAX Development
* [ ] Hierarchical Bayesian Time Series Development
* [ ] Model Evaluation

---

## Phase 4 — Web Application

* [ ] FastAPI Backend
* [ ] React Frontend
* [ ] Interactive Dashboard
* [ ] GIS Visualization

---

## Phase 5 — Deployment

* [ ] Testing
* [ ] Documentation
* [ ] Deployment
* [ ] Final Thesis

---

# 👥 Team

**Bachelor of Data Science**

**Telkom University Surabaya**

### Project Members

* Alfia Damayanti
* Auliya Ardhini Putri
* Ayunda Dewi Agustin

---

# 📖 Research

This repository supports the development of:

## Bachelor's Thesis

**Early Warning System Kerentanan Pangan Berbasis Forecasting Produksi Padi Menggunakan SARIMAX dan Hierarchical Bayesian Time Series di Provinsi Jawa Timur**

---

## Internship Project

**Department of Food Security and Agriculture**

Surabaya City Government

---

# 📜 License

This project is licensed under the **MIT License**.

---

# ⭐ Future Development

Potential future enhancements include:

* PostgreSQL Database Integration
* Docker Containerization
* Authentication & Authorization
* Automated Data Pipeline
* Real-Time Weather Integration
* Multi-Crop Forecasting
* Cloud Deployment
* Mobile-Responsive Dashboard
* API Documentation
* Model Monitoring

---

## ❤️ Acknowledgements

This project is developed as part of the Bachelor's Thesis and Internship Program at **Telkom University Surabaya**, with support from the **Department of Food Security and Agriculture, Surabaya City**.

---

> **Developed with Python, FastAPI, React, Bayesian Statistics, and Earth Observation Data for Sustainable Food Security Monitoring.**

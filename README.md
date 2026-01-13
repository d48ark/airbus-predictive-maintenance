# ✈️ AI-Powered Predictive Maintenance for Aircraft Engines

> **Goal:** Build an AI-based system to predict the **Remaining Useful Life (RUL)** of aircraft engines using NASA’s C-MAPSS sensor dataset.  
> Integrated with **MLOps (MLflow + Docker)** for experiment tracking and deployment, and **RPA (UiPath)** to automate maintenance report generation — directly addressing Airbus's industrial AI and RPA needs.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Architecture](#architecture)
- [Dataset](#dataset)
- [Tech Stack](#tech-stack)
- [Project Workflow](#project-workflow)
- [Results](#results)
- [How to Run](#how-to-run)
- [Future Scope](#future-scope)
- [Author](#author)

---

##  Project Overview
- Developed a **Predictive Maintenance** pipeline for aircraft engines.
- Predicts **RUL (Remaining Useful Life)** from real-time sensor data.
- Supports **controlled experiments**, **model monitoring**, and **automated report generation**.
- Directly applicable in **aviation maintenance & manufacturing operations** at Airbus.

---

##  Architecture

     ┌──────────────────────┐
     │  Raw Sensor Data     │
     └─────────┬────────────┘
               │
       Data Preprocessing
               │
     Feature Engineering (Stats)
               │
    ┌──────────┴──────────┐
    │                     │
ML Models (RF) DL Models (LSTM)
│ │
└──────────┬──────────┘
│
MLflow Experiment Tracking
│
Dockerized Deployment + Monitoring
│
RPA Bot Generates Reports
│
Streamlit Dashboard UI


---

## Dataset

- **Name:** NASA C-MAPSS Turbofan Engine Degradation Dataset  
- **Source:** [NASA](https://www.kaggle.com/datasets/behrad3d/nasa-cmaps?resource=download)  
- Using subset **FD001** (1 operating condition, 1 fault mode)  
- Data format: Multivariate time-series (sensor readings per engine cycle)

---

##  Tech Stack

**Languages:** Python  
**Libraries:** pandas, numpy, scikit-learn, TensorFlow/Keras, matplotlib, seaborn  
**MLOps:** MLflow, Docker, Prometheus/Grafana  
**RPA:** UiPath  
**Visualization:** Streamlit

---


## How to Run

```bash
# Clone repo
git clone https://github.com/<your-username>/airbus-predictive-maintenance.git
cd airbus-predictive-maintenance

# Install dependencies
pip install -r requirements.txt

# Run notebooks in order
jupyter notebook notebooks/01_data_ingestion.ipynb

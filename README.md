# Predicting the Approach Probability of Coastal Fish Schools Using IoT Sonar Data

## 📌 Project Overview
This project aims to predict the short-term approach probability of coastal fish schools using IoT-based hydroacoustic (sonar) sensor data combined with environmental variables. The goal is to support efficient and sustainable coastal fishing by providing early warnings when fish schools are likely to approach a monitored area.

This project is developed as part of the **Internet of Things and Applied Data Science** course and demonstrates an end-to-end IoT data science workflow, from data ingestion to cloud deployment.

---

## 🎯 Problem Statement
We want to **predict whether a fish school will approach a specific coastal area within the next 10–30 minutes**, because early detection improves fishing efficiency, reduces fuel and time costs, and supports sustainable fisheries management.

We use data collected from **IoT sonar (hydroacoustic) sensors**, along with environmental data such as water temperature, tide level, and wind conditions.

**Success Criteria:**
- ROC-AUC ≥ 0.85  
- High-precision alerts (≥ 80%) for early warnings  

---

## 📊 Data Sources
The project uses publicly available datasets, including:
- Hydroacoustic (sonar) water-column data
- Environmental sensor data (e.g., water temperature, tide, wind)

Possible data sources include NOAA hydroacoustic datasets and open sonar datasets from Kaggle or academic repositories.

---

## 🧠 Methodology
1. **Data Ingestion**  
   Load sonar and environmental sensor data (CSV format)

2. **Data Cleaning & Preprocessing**  
   Handle missing values, noise filtering, normalization

3. **Feature Engineering**
   - Sonar energy and backscatter statistics
   - Temporal features (moving averages, trends)
   - Environmental context features

4. **Modeling**
   - Baseline models: Logistic Regression, Random Forest
   - Output: Probability of fish school approach

5. **Evaluation**
   - ROC-AUC, Precision, Recall, F1-score

6. **Visualization**
   - Time-series plots
   - Probability-based alert visualization

7. **Deployment**
   - Streamlit dashboard deployed on AWS EC2

---

## 🖥️ Dashboard
A Streamlit-based interactive dashboard provides:
- Probability of fish school approach over time
- Historical sonar signal trends
- Alert indicators for high-risk periods

The dashboard is deployed on an AWS EC2 instance (Free Tier).

---

## ☁️ Deployment (AWS EC2)
1. Launch an EC2 Free Tier instance  
2. Install Python, Git, and required dependencies  
3. Clone this repository  
4. Install Python packages  
5. Run the Streamlit dashboard  

```bash
streamlit run dashboards/streamlit_app.py

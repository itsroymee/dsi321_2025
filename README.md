# DSI321 : Wild Fire Alert System Project

## Overview

This project aims to develop a develop a near real-time wildfire alert system for Thailand using data from NASA FIRMS and OpenWeatherAPI, orchestrated by Prefect and visualized via Streamlit. It supports the work of the National Disaster Management Subcommittee by integrating technical data workflows with practical data governance and machine learning analysis.

The System Include:
- ETL pipe line via Prefect
- Data Versioning with LakeFS
- Interactive map-based dashboard (Streamlit+Folium)
- Fire prediction analysis using Random Forest

# Part 1: Technical Implementation

## 1. Repository Setup

* Repository created within the first week.
* Repository name: dsi321_2025
* File Structure:
    * `data/` – Weather data in Parquet format
    * `visualization/shape_file/` – Geospatial shape files
    * `machine_learning.ipynb` – ML model
    * `api/` – Scripts for ETL (e.g., `firmapiflow.py`, `apiweatherflow.py`)
    * `visualization/` – Streamlit dashboard

## 2. Commit Frequency

* Maintained a steady commit frequency:
    * ≥ 5 commits/week for 3 consecutive weeks

## 3. README Quality

* README contains > 1,000 characters
* Provides detailed breakdown of project objective, tools used, architecture, grading alignment

# 4. Dataset Quality

| Criteria                 | Status | Notes                                                 |
| ------------------------ | ------ | ----------------------------------------------------- |
| ≥ 1,000 Records          | ✅     | Data collected every 15 min; > 96 records/day         |
| 24-Hour Time Coverage    | ✅     | Daily collection via Prefect schedule                 |
| Data Completeness ≥ 90%  | ✅     | Verified during ingestion using quality checks in Prefect |
| No `object` Columns      | ✅     | Parquet format with clearly defined schema            |
| No Duplicate Records     | ✅     | Deduplication logic in Prefect ETL pipeline           |

# 5. Schema Consistency

* Structured fields:
    * `timestamp` (datetime), `latitude`, `longitude`, `brightness`, `confidence`
    * `temperature`, `humidity`, `wind_speed` – all numeric
* Data types enforced via Parquet and LakeFS schema tracking

# Part 2: Project Report

## 1. Data Visualization

* Tools used: Streamlit, Folium, GeoPandas
* Key Visuals:
    * Heatmap of fire hotspots by province
    * Correlation matrix (weather vs brightness)
    * Scatter plots (e.g., temp vs brightness)
* Features:
    * Interactive map
    * Zoomable and filterable timeline!
  ![Image](https://github.com/user-attachments/assets/35c5d4a8-6437-4b47-80a4-7ff9f4c606a3)

## 2. Machine Learning

* Model: Random Forest Regression
* Target: `brightness`
* Features: `temperature`, `humidity`, `wind_speed`
* Results:
    * Feature importance analysis highlights temperature and humidity as key indicators
    * Correlation matrix supports feature relationships
* Tools: Scikit-learn, Matplotlib!
![Image](https://github.com/user-attachments/assets/4230aa79-e33a-4917-b23a-4c89e19ecf0b)

# 🛠️ Tools & Architecture

| Component          | Tool/Technology        |
|--------------------|------------------------|
| Data Ingestion     | Prefect                |
| Data Storage       | LakeFS + Parquet       |
| Dashboard          | Streamlit + Folium     |
| Geospatial Handling| GeoPandas              |
| Machine Learning   | Scikit-learn (RandomForest) |
| Metadata Management| CKAN                   |

---

## ✅ Outcomes

* Automated ETL pipeline for real-time fire + weather data
* Complete interactive dashboard for decision makers
* Validated model identifying environmental factors affecting fire intensity
* Designed with scalability and data governance in mind


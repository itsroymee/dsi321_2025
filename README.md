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

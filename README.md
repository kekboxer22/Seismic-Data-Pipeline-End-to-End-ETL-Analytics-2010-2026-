# Seismic Data Pipeline: End-to-End ETL & Analytics (2010–2026)
# Project Overview
This repository contains a professional ETL (Extract, Transform, Load) pipeline designed to process, analyze, and store global earthquake data. The project handles a massive dataset of over 1,000,000 raw events, refining them into a high-performance analytical core stored in a PostgreSQL relational database.

The Goal: Transform messy, multi-format seismic logs into actionable insights and production-ready data storage.

# Technical Stack
Language: Python 3.x

Data Engineering: Pandas, NumPy

Database: PostgreSQL, SQLAlchemy (ORM & Engine)

Visualization: Matplotlib, Seaborn

Environment: Jupyter Notebook / Professional IDE

# Pipeline Architecture
1 Data Extraction & Auditing
Ingested raw CSV data containing 1.05M+ rows.

Performed initial data auditing to handle missing values and inconsistent geographical labels.

#2 Transformation (The "Heavy Lifting")
Feature Engineering: Converted complex raw time formats (Year + Day of Year + Hour) into high-precision ISO-8601 Timestamps.

Data Refinement: Filtered the dataset to focus on the modern instrumental era (2010–2026).

Optimization: Reduced the dataset to 690,505 clean, validated records ready for analysis.

#3 Visual Analytics & Insights
Weekly Dynamics: Resampled data to identify global seismic "pulses" and activity spikes.

Hotspot Analysis: Identified the top 10 most volatile regions (South Sandwich Islands, Fiji, Hawaii).

Anomaly Detection: Separated "background noise" (Average Magnitudes) from extreme events (Magnitude > 7.5) using minimalist visualization techniques.

#4 Database Loading (PostgreSQL)
Implemented an automated migration script using SQLAlchemy.

Successfully migrated 690,505 rows into a structured SQL table (quakes) for persistent storage and BI integration.

# Key Metrics
Total Rows Processed: 690,505

Max Magnitude in Dataset: 9.1 (Tohoku, Japan)

Time Resolution: Weekly & Monthly Aggregations

Database Status: Fully Synchronized with PostgreSQL

#How to Run
https://colab.research.google.com/github/kekboxer22/Seismic-Data-Pipeline-End-to-End-ETL-Analytics-2010-2026-/blob/main/Data%20Poject%20Earthquick.ipynb

# Visualization Preview
The pipeline generates high-density charts including Weekly Incident Dynamics and Geographical Hotspot distributions.

# Final Note
This project demonstrates the ability to manage the full data lifecycle: from handling raw, inconsistent CSV files to deploying a structured database ready for a corporate BI environment.

Project Status: Completed & Migrated to SQL.

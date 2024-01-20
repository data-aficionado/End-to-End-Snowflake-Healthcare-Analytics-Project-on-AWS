# End to End Healthcare Analytics using Snowflake and AWS

## Overview
This project aims to leverage healthcare analytics to improve patient outcomes and reduce healthcare costs by focusing on analyzing the Length of Stay (LOS) in healthcare facilities. It integrates Snowflake for data handling and AWS Sagemaker for machine learning model development.

## Business Context
Healthcare analytics is crucial in enhancing the delivery of healthcare services. This project specifically targets the analysis of patient LOS, a key metric affecting patient outcomes, healthcare costs, and hospital capacity.

## Objectives
- Analyze patient LOS data to identify improvement areas in care delivery.
- Predict patient LOS using machine learning models.
- Utilize Snowflake for data storage and processing.
- Deploy models in AWS Sagemaker and schedule regular scoring.

## Technical Workflow
1. **Introduction to Snowflake**: Understanding the Snowflake platform and its application in data analytics.
2. **Exploratory Data Analysis (EDA) in Snowflake**: Performing initial data exploration within Snowflake.
3. **Feature Engineering in Snowflake**: Enhancing data for model building.
4. **AWS Sagemaker Setup**: Configuring the AWS Sagemaker environment for model development.
5. **Data Fetching**: Using `snowflake-connector-python` and `snowflake-sqlalchemy` for data extraction.
6. **Data Preprocessing**: Preparing data for modeling.
7. **Feature Selection**: Choosing relevant features for the model.
8. **Model Building**: Developing models like Linear Regression, Random Forest Regression, and XGBoost Regression.
9. **Model Predictions**: Generating and analyzing predictions.
10. **Inserting Predictions in Snowflake**: Storing model outputs back into Snowflake.
11. **Scoring Function Deployment and Scheduling**: Automating the model scoring process.
12. **Sending Status Emails**: Setting up notifications regarding the process status.

## Aim
- To conduct comprehensive data analysis within Snowflake.
- To predict patient LOS with machine learning models.
- To schedule and automate model processes in AWS Sagemaker.
- To perform live data scoring and integrate predictions into Snowflake.
- To implement a system for sending status updates via email.

## Data
- **Training Data**: Data on 230k patients across various regions and hospitals, with 19 features.
- **Simulation Data**: Prediction data for 71k patients.

## Tech Stack
- **Tools**: AWS Sagemaker, Snowflake
- **Language**: Python
- **Libraries**: `snowflake-connector-python`, `snowflake-sqlalchemy`, `xgboost`, `pandas`, `numpy`, `scikit-learn`




## Project Structure

```plaintext
End-to-End-Snowflake-Healthcare-Analytics-Project-on-AWS/
├── README.md                     # Project README
└── Code/                         # Main code directory
    ├── Data/                     # Data directory
    │   ├── health_data.csv       # Health data CSV file
    │   └── simulation_data.csv   # Simulation data CSV file
    ├── Python Files/             # Python scripts and notebooks
    │   ├── LOS_Preprocessing.py                  # LOS preprocessing script
    │   ├── MODEL_FEATS.pkl                       # Pickle file for model features
    │   ├── MODEL_XGB.model                       # XGBoost model file
    │   ├── MODEL_training_data_with_final_features.pkl # Pickle file for training data
    │   ├── Preprocessing _ Model Building.ipynb  # Jupyter notebook for preprocessing and model building
    │   ├── Scoring Script.ipynb                  # Jupyter notebook for scoring script
    │   ├── mail_creds.py                         # Python script with mail credentials
    │   └── snowflake_creds.py                    # Python script with Snowflake credentials
    └── SQL Queries/              # SQL query files
        ├── Snowflake-EDA.sql                     # SQL file for EDA
        ├── Snowflake-Feature Engineering.sql     # SQL file for feature engineering
        └── Snowflake-Scoring Script.sql          # SQL file for scoring script


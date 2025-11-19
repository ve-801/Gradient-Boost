ATM & Machine Learning Project – README
📌 Overview

This project combines two independent learning components:

ATM Simulation System
A simple interactive ATM model demonstrating authentication, withdrawals, deposits, balance tracking, and basic input validation.

Machine Learning Regression Pipeline
A modular ML workflow using Pandas, NumPy, Scikit-Learn, LightGBM, and Optuna for regression tasks such as predicting continuous values (e.g., insurance charges).

Both parts are designed for educational purposes, showcasing Python fundamentals, user input handling, data analysis, preprocessing, model training, evaluation, and hyperparameter tuning.

📂 Project Structure
project/
│
├── atmproj.ipynb         # Jupyter notebook with ATM + ML code fragments
├── README.md             # Project documentation
├── models/               # Saved ML models (if generated)
├── atm_accounts/         # Account data for ATM simulation (if implemented)
└── data/
       └── dataset.csv    # Training dataset for ML pipeline (you provide)

💳 Part 1: ATM Simulation
🎯 Purpose

The ATM simulation demonstrates:

Basic Python programming

User interaction with input()

PIN authentication logic

Conditional statements

Validation of numeric input

Withdrawal & deposit logic

Balance updates

This is a simple, console-based simulation meant for learning, not for real banking use.

🧠 Features

PIN Authentication
The user is prompted to enter a PIN before accessing account operations.

Withdrawal Logic

Checks if amount is positive

Checks per-transaction withdrawal limit

Checks sufficient balance

Deposit Logic

Ensures positive deposit amount

Updates the balance

Balance Inquiry
Displays the current available balance.

Simple Menu System
Users can repeatedly choose options until they exit.

⚠️ Limitations (Educational Only)

PIN is hard-coded (not secure)

No real database integration

No hashing or encryption

No multi-user account system

No overdraft or daily limits

No persistent transaction history unless manually implemented

📊 Part 2: Machine Learning Pipeline
🎯 Purpose

This section demonstrates how to build a complete regression pipeline including:

Data loading

Handling missing values

Feature selection

Splitting into training/testing sets

Model training (Linear Regression or LightGBM)

Hyperparameter tuning (Optuna)

Evaluation using MAE/MSE/RMSE

Optional model saving using joblib

🧠 Key Concepts
✔ Data Preprocessing

Handles missing numeric values via median imputation

Categorical values can be encoded

Separates target variable (e.g., charges)

Prepares features (age, bmi, children, etc.)

✔ Model Training

Supports:

Baseline models (Linear Regression)

Advanced models (LightGBM)

✔ Hyperparameter Tuning

Uses Optuna for automated search

Evaluates models based on validation RMSE or MAE

Selects best parameters for final training

✔ Evaluation

Metrics used:

MAE – Mean Absolute Error

MSE – Mean Squared Error

RMSE – Root Mean Squared Error

✔ Model Saving

Model + preprocessing pipeline can be saved with:

joblib.dump()

📦 Requirements

Install dependencies:

pip install numpy pandas scikit-learn lightgbm optuna joblib


If Jupyter Notebook is required:

pip install notebook jupyter

▶️ How to Run
ATM Simulation

Open the notebook and run the ATM cells:

jupyter notebook atmproj.ipynb


Follow the prompts in the console:

Enter PIN

Choose options:

Withdraw

Deposit

Check balance

Exit

Machine Learning Pipeline

Place your dataset (e.g., insurance.csv) inside /data folder

Update the file path in the notebook

Run the notebook step-by-step:

Load dataset

Preprocess data

Train model

Tune with Optuna

Evaluate model

Save the trained model

🛠️ Future Improvements
ATM Section

Add database storage (SQLite / PostgreSQL)

Secure password hashing

Multi-account support

Daily withdrawal limit

GUI-based ATM screen simulation

Proper transaction history logging

ML Section

Add data visualizations

Train multiple models and compare performance

Add pipelines for classification tasks

Deploy model using Flask/FastAPI

Integrate model monitoring & drift detection

📘 Notes

The project is purely educational and not intended for real banking or financial decision-making.

You may extend both the ATM and ML components independently.

The notebook contains incomplete or placeholder sections; fill in dataset paths and missing logic as needed.

👤 Author

Vengadesan G
Learning Python, Full Stack Development, and Machine Learning.

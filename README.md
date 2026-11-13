# Cybersecurity Analysis: AI & Data Science Machine Learning Pipeline

## Project Overview & Objectives
This project takes a raw cybersecurity dataset (Dataset 1) and implements a complete machine learning workflow to solve two distinct predictive problems:
1. **Classification Task:** Predict whether a network session is "Benign" or an "Attack" (`is_attack`) to support threat detection.
2. **Regression Task:** Predict the duration of a network session (`session_duration`) for bandwidth and resource planning.

## Tech Stack & Libraries
* **Language & Environment:** Python, Google Colab
* **Libraries:** Scikit-Learn (`StandardScaler`, `LabelEncoder`, `RandomForestClassifier`, `RandomForestRegressor`), Pandas, NumPy, Seaborn, Matplotlib

## Data Preprocessing & Methodology
* **Missing Value Imputation:** Addressed missing data in `protocol`, `bytes_received`, and `signal_strength` using median imputation for numerical features and mode imputation for categorical features to avoid data loss and noise distortion.
* **Feature Engineering & Selection:** Dropped `session_id` due to zero predictive power and potential overfitting. Used Label Encoding for categorical features and `StandardScaler` to normalize numerical ranges.
* **Exploratory Data Analysis:** Built correlation heatmaps revealing that `anomaly_score` and `login_attempts` are major indicators of security threats.

## Key Results & Performance
* **Classification Model (Random Forest):** Achieved a high **Recall of 98%** for attack detection, ensuring that almost all security threats are successfully flagged to minimize false negatives.
* **Regression Model (Random Forest):** Achieved an **$R^2$ Score of 0.4057** and a Mean Absolute Error (MAE) of **10.20 seconds**, proving that network session durations can be reliably predicted using traffic features like `bytes_received`.

## Links & Evidence
* [View Full Project Report PDF](./Fund_AI&DS_Project.pdf)
* [Google Colab Notebook](https://colab.research.google.com/drive/1ydyjViwTPrPNpmqGtgBqj5J8GjDApJt0?usp=sharing)

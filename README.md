California Wildfire Severity Prediction
📌 Overview
This project focuses on predicting the severity of wildfires in California using data from CAL FIRE. The dataset underwent thorough cleaning, preprocessing, and visualization before applying multiple machine learning models to predict wildfire severity (Low/Medium vs. High).
We compared multiple classifiers — Random Forest, Gradient Boosting, Logistic Regression, and SVM — and selected the best-performing model based on accuracy and ROC-AUC scores.
The final deployed model was Logistic Regression, achieving:
Test Accuracy: 61.44%
Test ROC-AUC: 0.6338
Cross-Validation Accuracy: 61.89% (±29.53%)
Cross-Validation ROC-AUC: 0.8228

📂 Project Structure
Cleaned_Cali_Fire.csv → Preprocessed wildfire dataset
wildfire_severity_model.pkl → Trained best model (Logistic Regression)
feature_scaler.pkl → StandardScaler used for feature scaling
model_metadata.csv → Metadata (accuracy, ROC-AUC, features, etc.)
wildfire_prediction.py → Main training and evaluation script

⚙️ Methodology
Data Cleaning & Preprocessing
Removed nulls, duplicates, and irrelevant features.
Final features: incident_longitude, incident_latitude, year, month.
Exploratory Data Analysis (EDA)
Visualized fire locations, frequency by year/month, and severity distribution.
Balanced dataset (50% Low/Medium, 50% High).

Model Training
Implemented and compared:
Random Forest
Gradient Boosting
Logistic Regression
Support Vector Machine (SVM)
Evaluated using Accuracy, ROC-AUC, Confusion Matrix, and Classification Report.
Model Selection & Validation
Logistic Regression chosen as the best model.
Performed 5-fold cross-validation to validate results.
Saving & Deployment
Saved model (.pkl), scaler, and metadata for future predictions.

House Price Prediction System
Command Line Machine Learning Application
This project is a command line based machine learning system for predicting house prices in Indonesia. Run it directly from the terminal. It supports numeric price prediction and price category classification.

System purpose.
You use this system to estimate house prices or classify them into price ranges using historical housing data. It is designed for model experimentation and learning, not web deployment.

Main features.

• Predicts house prices using regression
• Classifies houses into Murah, Sedang, Mahal
• Supports Random Forest and XGBoost models
• Handles imbalanced data using SMOTE
• Cleans noisy price and area formats
• Uses location encoding for categorical data
• Runs fully in the command line

Machine learning tasks.

Regression mode.
Predicts a numeric house price in Rupiah.

Classification mode.
Predicts a price category. Murah, Sedang, or Mahal.

Models used.

• Random Forest Regressor
• XGBoost Regressor
• Random Forest Classifier
• XGBoost Classifier

Data preprocessing.

• Converts price strings such as 750jt or 1.2M into numbers
• Converts area values like 120 m² into floats
• Cleans price per square meter values
• Encodes location names using LabelEncoder
• Drops rows with missing required values
• Balances class labels using SMOTE

Dataset requirements.

Your CSV file must include these columns.

• price
• listing-floorarea
• listing-floorarea 2
• listing-location
• bed
• bath

Example values.

price: 750jt, 1.2M, 2500000000
listing-floorarea: 120 m²
listing-location: Tangerang Selatan
bed: 3
bath: 2

How the system works.
Load the dataset from a CSV file
Clean and preprocess all features
Encode categorical values
Split data into training and testing sets
Train regression and classification models
Ask the user for input via terminal
Generate a prediction based on selected mode and model

User input flow.
You will be prompted to enter.

• Prediction mode. regresi or klasifikasi
• Number of bedrooms
• Number of bathrooms
• Land area in square meters
• Building area in square meters
• Location selection from a numbered list
• Model choice. rf or xgb

Output:
Regression output.
Perkiraan harga rumah dalam Rupiah.
Classification output.
Kategori harga. Murah, Sedang, atau Mahal.

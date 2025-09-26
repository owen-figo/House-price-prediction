🏡 House Price Prediction Web App

This is a Flask-based machine learning web application for predicting house prices in Indonesia.
It supports both regression (numeric price prediction) and classification (categorical price range: Murah, Sedang, Mahal).

📖 Table of Contents

✨ Features

🛠️ Tech Stack

🚀 Installation & Usage

📂 API Endpoints

📊 Example Workflow

📌 Dataset Requirements

📜 License

✨ Features

📂 Upload dataset (.csv) for model training

🔄 Cleans messy price/area values (e.g., 750jt, 1,2M, Rp 900.000.000)

⚖️ Removes outliers (max cap: Rp 100B)

🏷️ Classifies houses into Murah, Sedang, Mahal

🤖 ML Models:

Random Forest Regressor → Predicts numeric prices

Random Forest Classifier → Predicts price category

⚖️ Imbalanced dataset handling with SMOTE

🌍 Encodes categorical features (location, category) with LabelEncoder

🔮 REST API endpoints for training & prediction

🛠️ Tech Stack

Backend: Flask (Python)

ML Models: scikit-learn (RandomForest), XGBoost (optional)

Data Handling: pandas, NumPy

Preprocessing: LabelEncoder, SMOTE (imbalanced-learn)

Frontend: HTML templates (extendable)

🚀 Installation & Usage
1. Clone the Repository
git clone https://github.com/YOUR_USERNAME/house-price-predictor.git
cd house-price-predictor

2. Install Dependencies
pip install -r requirements.txt

3. Run the Flask App
python app.py

4. Open in Browser
http://127.0.0.1:5000

📂 API Endpoints
🔹 POST /upload

Upload a dataset to train the models.

Input: CSV file (csv-file)

Output: JSON confirmation with available locations

🔹 POST /predict

Make a price prediction.

Input (JSON):

{
  "filename": "your_dataset.csv",
  "model": "rf",
  "mode": "regresi",
  "bed": 3,
  "bath": 2,
  "bangunan": 120,
  "location": "Jakarta Barat"
}


Output (JSON):

{
  "success": true,
  "prediction": "Perkiraan Harga: Rp 1,200,000,000"
}

📊 Example Workflow

Upload houses.csv → App trains RandomForest models

API returns available locations (Jakarta Barat, Bandung, Surabaya, etc.)

Send prediction request with house details

Get predicted price or category

📌 Dataset Requirements

Your dataset must include at least these columns:

price (e.g., "750jt", "1.2M", "Rp 2,500,000,000")

listing-floorarea (e.g., "120 m²")

listing-location (e.g., "Jakarta Barat")

bed (integer, e.g., 3)

bath (integer, e.g., 2)

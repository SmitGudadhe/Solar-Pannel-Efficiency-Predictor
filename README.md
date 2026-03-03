# ☀️ Solar Panel Efficiency Predictor & Smart Forecaster

An AI-powered web application that predicts the real-time power output and efficiency of a solar panel system based on live environmental conditions. 

This project was developed as a capstone for the **Advanced Course on Green Skills and Artificial Intelligence** (Skills4Future Program) supported by the Edunet Foundation, AICTE, and Shell India.

## 🚀 Project Overview
Solar energy generation is highly dependent on weather conditions like irradiance and temperature. This project bridges the gap between raw weather forecasts and actionable energy insights. By leveraging machine learning and live API data, the application scales industrial solar plant data down to a residential 5kW system, providing users with accurate, location-specific power predictions.

## ✨ Key Features
* **Live Smart Forecasting:** Enter any city name to fetch real-time weather data and predict current solar power output.
* **Manual Simulation Mode:** Adjust sliders for Irradiance, Air Temperature, and Module Temperature to see how different conditions affect power generation.
* **Efficiency & Fault Detection:** Compares actual inverter readings against the AI's expected output to calculate an efficiency rating (e.g., flagging if panels need cleaning).
* **Keyless API Integration:** Utilizes the Open-Meteo API for reliable, free, and keyless geocoding and weather data retrieval.

## 🛠️ Tech Stack
* **Language:** Python 3.12
* **Machine Learning:** Scikit-Learn (`RandomForestRegressor`)
* **Data Processing:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Web Framework:** Streamlit
* **APIs:** Open-Meteo (Geocoding & Forecast APIs)

## 🧠 How It Works (Architecture)
1. **Data Preprocessing:** Trained on the *Plant_1* solar dataset (~68,000 records of generation and weather sensor data). 
2. **Model:** A Random Forest Regressor (`n_estimators=100`) was trained to understand the non-linear relationship between Irradiance, Temperature, and DC Power, achieving an $R^2$ accuracy of ~95%.
3. **Scaling:** The raw multi-megawatt predictions are scaled down (using a factor of 45,000) to simulate a standard residential 5kW rooftop system.
4. **Live Pipeline:** User City ➡️ Geocoding API (Lat/Lon) ➡️ Weather API (Irradiance/Temp) ➡️ ML Model ➡️ Output Prediction.

## 💻 Run It Locally

Follow these steps to run the application on your own machine:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/SmitGudadhe/Solar-Pannel-Efficiency-Predictor.git](https://github.com/SmitGudadhe/Solar-Pannel-Efficiency-Predictor.git)
   cd Solar-Pannel-Efficiency-Predictor

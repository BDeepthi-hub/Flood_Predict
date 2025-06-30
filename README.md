# Flood_Predict
**🌊 Flood Prediction & Multilingual Alert System**
This project is a smart and scalable web-based flood alert system built using Python, Flask, and machine learning. It is designed to help communities across India anticipate and prepare for potential flood situations by leveraging real-time weather data, a trained ML model, and automated multilingual SMS alerts.

The system not only predicts the type and severity of floods but also actively notifies users in their regional languages, making it accessible and practical for real-world use in rural or vulnerable areas.

**🔍 Key Features**

**🌦️ Real-Time Weather Monitoring:**
Integrates with the OpenWeatherMap API to fetch city-specific weather data including rainfall, humidity, and wind speed.

**🤖 Machine Learning Flood Prediction:**
Utilizes a trained model (flood_model.pkl) built from historical flood data to predict:

Whether a flood may occur

The type of flood (e.g., river, urban)

Its expected impact (e.g., low, moderate, severe, extreme)

**📲 SMS Alerts in Local Languages:**
Sends automatic flood alerts to affected users via the Twilio SMS API, with messages translated into local languages such as:

Hindi

Telugu

Tamil

Kannada
This is done using the Deep Translator package (Google Translate backend).

**🌐 City-Wise Risk Assessment:**
The system supports multiple cities across India, allowing different users to subscribe based on their city of residence.

**🧑‍💻 User-Friendly Interface:**
A clean Flask-based UI allows admins or users to:

View live weather and risk reports

Check flood alerts by city

Manually test flood predictions using form inputs

**📊 Modular Design:**
Components like model prediction, weather API, and SMS messaging are separated for easy maintenance and scalability.

**🛠️ Technologies Used**
Area	Technology Used
Backend	Python, Flask
Machine Learning	scikit-learn, joblib
APIs	OpenWeatherMap, Twilio, Google Translate
Data	CSV files: flood_data.csv, user_data.csv
Frontend	HTML5, Jinja2 (Bootstrap supported)

**📁 Project Structure**

📦 flood-prediction-alert/
### Flask main application logic
├── app.py  
### Separate script to test flood model
├── check_model.py  
### Trained ML model (logistic regression or similar)
├── flood_model.pkl    
### Historical weather and flood data
├── flood_data.csv    
### List of users and their city details
├── user_data.csv  
### HTML templates for UI (home, alert, report)
├── templates/ 
### Optional: CSS, JS, image files
├── static/       

**📸 Key Outputs
✅ No Flood Detected:**
Displays message when no flood risk is predicted.

**⚠️ Flood Alert Message:**
Warns about cities likely to be affected and their severity level.

**📤 SMS Confirmation:**
Indicates successful sending of localized messages to users in the affected areas.

**🚀 How It Works (Workflow)**
User/admin accesses the web portal

System fetches live weather data from OpenWeatherMap

Data is fed into the ML model for flood prediction

If flood risk is detected:

Cities are marked as flood-prone

Users from those cities (from user_data.csv) are selected

Localized SMS messages are sent to those users

The UI displays flood alerts for admin or users

**🧪 Future Improvements**
Replace rule-based translation with NLP-based language preference detection

Add historical maps or GIS flood overlays

Store SMS alerts and logs in a relational DB (e.g., MySQL or PostgreSQL)

Add Telegram/WhatsApp API integration for broader alerting

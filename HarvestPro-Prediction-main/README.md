# HarvestPro-Prediction
HarvestPro is an advanced agricultural prediction tool designed to forecast crop yields and optimize farming practices using machine learning and data analytics. This project leverages various data sources to provide accurate and actionable predictions to help farmers make informed decisions.


![image](https://github.com/BeheraSas/HarvestPro-Prediction/assets/148372851/ab49b583-c797-4e41-b105-0960ebd76c3b)

**Features:**

**Crop Yield Prediction:** Utilizes historical data and machine learning algorithms to predict crop yields.

**Weather Data Integration:** Incorporates real-time and historical weather data to improve prediction accuracy.

**Soil Analysis:** Analyzes soil conditions using sensor data to provide recommendations for soil management.

**Data Visualization:** Provides intuitive visualizations of data and predictions to facilitate better decision-making.

**User-Friendly Interface:** Offers an easy-to-use interface for farmers to input data and access predictions.

![Screenshot 2024-03-30 180844](https://github.com/BeheraSas/HarvestPro-Prediction/assets/148372851/cf2be496-4e4b-4ed8-ac23-73678905ac74)

## Project Description

The application logic is contained in the `app.py` file. This file contains the Flask application and routes for the API endpoints.

## Setup

To set up the Flask application, follow these steps:

1. Clone the repository.
2. Navigate to the project directory.
3. Create a virtual environment using venv:
   ```bash
   python3 -m venv env
   ```
4. Activate the virtual environment:
   ```
     env\bin\activate # On MacOS use `source env/bin/activate`
   ```
5. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

## Run application

To run the application, use the following command:

```

    python3 app.py

```

## API Endpoint

### /api/predict
This endpoint accepts POST requests with the following payload:

        {
            "latitude": 19.0728,
            "longitude": 72.8826
        }

The response will be:

        {
            "conditions": {
                "humidity": 63.809895833333336,
                "rainfall": 0.0,
                "temperature": 28.35866275926431
            },
            "predicted_crops": [
                "muskmelon (53.00%)",
                "mothbeans (24.00%)",
                "lentil (21.00%)"
            ]
        }

### /api/forecast
This endpoint accepts POST requests with the following payload:

        {
            "latitude": 19.0728,
            "longitude": 72.8826
        }

The response will be:

    {
    "response": {
        "humidity": 63.809895833333336,
        "rainfall": 0.0,
        "temperature": 28.35866275926431,
        "weather_data": []
        }
    }

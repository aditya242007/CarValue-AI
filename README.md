# CarValue AI - Used Car Price Prediction

A smart web app that predicts the resale value of a used car using a trained machine learning model. The project combines a Flask backend, a clean interactive UI, and a predictive model to estimate a fair market price based on vehicle details like brand, year, mileage, fuel type, power, engine size, and more.

This project is designed to help users quickly understand how much a used car may be worth before buying or selling it.

## Project Overview

CarValue AI allows a user to answer a few questions about a car and then get:

- an estimated price in lakhs
- a confidence range around that value
- a quick market-style valuation based on real data patterns

The app is built as a lightweight web interface, making it easy to use even for non-technical users.

## Features

- Predicts used car market price using a trained ML model
- Accepts inputs such as:
  - Brand
  - Year
  - Fuel type
  - Transmission
  - Ownership type
  - Kilometers driven
  - Engine displacement
  - Power
  - Mileage
  - Location
  - Number of seats
- Provides estimated price and an approximate valuation range
- Includes a modern, responsive web interface
- Ready for local deployment and cloud hosting

## Tech Stack

- Python
- Flask
- Pandas
- NumPy
- scikit-learn
- XGBoost
- Joblib
- HTML/CSS/JavaScript
- Gunicorn (for deployment)

## Project Structure

```text
Used-Car-Price-Prediction-Model-
├── README.md
├── Code/
│   ├── app.py
│   ├── Dockerfile
│   ├── ProcFile.txt
│   ├── requirements.txt
│   ├── model/
│   │   ├── model_options.joblib
│   │   └── used_car_price_model.joblib
│   ├── static/
│   │   ├── brand-logos.js
│   │   ├── script.js
│   │   ├── style.css
│   │   └── images
│   └── templates/
│       └── index.html
└── .gitignore
```

## How It Works

1. The user enters details about the car in the browser.
2. The frontend sends the data to the Flask app.
3. The backend transforms the data into the format expected by the model.
4. The trained model predicts a resale price.
5. The result is returned to the user and displayed in the dashboard.

## Local Setup

Follow these steps to run the project on your machine.

### 1. Clone the repository

```bash
git clone https://github.com/aditya242007/Used-Car-Price-Prediction-Model-.git
cd Used-Car-Price-Prediction-Model-
```

### 2. Create a virtual environment

```bash
python -m venv venv
source venv/bin/activate
```

On Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
cd Code
pip install -r requirements.txt
```

### 4. Run the app

```bash
python app.py
```

Then open the browser and visit:

```text
http://127.0.0.1:5000
```

## Deployment

The project includes a Dockerfile and a Procfile for deployment.

### Docker example

```bash
cd Code
docker build -t carvalue-ai .
docker run -p 8080:8080 carvalue-ai
```

The app runs with Gunicorn in the container and exposes port 8080 by default.

## Model Notes

The model files are stored in the `Code/model` folder and are loaded by the Flask app at runtime.

- `used_car_price_model.joblib` contains the trained prediction model
- `model_options.joblib` contains metadata used by the app for labels and options

## Future Improvements

Possible next steps for this project:

- add more car brands and cities
- improve accuracy with more training data
- add image upload support
- compare multiple models and show the best one
- create a dashboard for transaction trends
- deploy on cloud platforms like Render, Railway, or Heroku

## License

This project is currently intended for educational and personal use. If you plan to use it commercially, please review licensing for the model, dataset, and deployment environment before publishing.

## Author

This project was created as a practical machine learning and web application example for used car price prediction.

If you want to improve it further, feel free to expand the model, refine the UI, or add new features.

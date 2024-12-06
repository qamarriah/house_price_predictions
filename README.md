# house_price_prediction
 
House Price Prediction Model
This project implements a machine learning pipeline to predict house prices based on various features such as size, location, number of rooms, and other related factors. It uses a Linear Regression model and provides an API endpoint for predictions using Flask.

Project Description
The House Price Prediction Model enables users to estimate the price of a house given specific features such as its size, location, number of rooms, year built, distance to the city center, and nearby amenities. The project covers data preprocessing, feature engineering, model training, evaluation, and deployment of the trained model as a Flask API.
Key features include:
•	Data preprocessing: Handling missing values, scaling numerical data, and encoding categorical data.
•	Exploratory Data Analysis: Visualization of correlations and feature importance.
•	Linear Regression model for predicting house prices.
•	Deployment of a Flask-based API for real-time predictions.
Setup and Installation Instructions
Follow these steps to set up the project on your local machine:
Prerequisites
•	Python 3.8 or higher
•	Libraries: Install using the provided requirements.txt file.
Installation
1.	Clone the Repository:
2.	git clone https://github.com/qamarriah/house-price-predictions.git
3.	cd house-price-prediction
4.	Install Required Libraries: Create a virtual environment and install dependencies:
5.	python -m venv venv
6.	source venv/bin/activate # For Windows: venv\Scripts\activate
7.	pip install -r requirements.txt
8.	Add the Dataset: Place your dataset file (e.g., house_prices_dataset.csv) in the project directory. Update the URL path in the script if necessary.
9.	Run the Script: To train the model and save it:
10.	python house_price_model.py
11.	Start the Flask API: To serve the model via an API:
12.	flask run
13.	Test the API: Use a tool like Postman or cURL to test predictions.
Functionality and Features
1. Data Preprocessing
•	Drops irrelevant columns (e.g., House ID).
•	Handles categorical variables using one-hot encoding.
•	Scales numerical features using StandardScaler.
2. Feature Engineering
•	Adds a derived feature: Price per sq ft for exploratory purposes.
•	Visualizes feature correlations using a heatmap.
3. Model Training
•	Uses Linear Regression to predict house prices.
•	Splits the dataset into training (80%) and testing (20%) sets.
•	Saves the trained model and scaler using joblib.
4. Model Evaluation
•	Evaluates model performance using MAE, MSE, and R².
•	Provides plots for actual vs. predicted prices and residuals.
5. Flask API
•	Serves predictions using a RESTful API.
•	Accepts input data in JSON format and returns predictions in real time.

API Usage
Endpoint: /predict
•	Method: POST
•	Request Body: JSON object containing input features. Example: 
•	{
•	  "Size (sq. ft.)": 1500,
•	  "Number of Rooms": 3,
•	  "Number of Bathrooms": 2,
•	  "Year Built": 2015,
•	  "Distance to City Center (km)": 10,
•	  "Nearby Amenities": 5,
•	  "Location_CityName": 1 // One-hot encoded location feature
•	}
•	Response: Predicted price as a JSON object. Example: 
•	{
•	  "predicted price": 300000
•	}

Future Enhancements
•	Incorporate advanced models such as Random Forest or XGBoost for better accuracy.
•	Add validation and error handling for API inputs.
•	Deploy the API using a cloud service (e.g., AWS, Azure, Heroku).
•	Include a front-end interface for better user interaction.

License
This project is licensed under the MIT License.

Contributing
Contributions are welcome! Please open an issue or submit a pull request with your suggestions.

Contact
For any questions or issues, feel free to reach out:
•	Email: tushez98@gmail.com
•	GitHub: qamarriah


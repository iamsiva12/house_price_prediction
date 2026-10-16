House Price Prediction

Machine learning project that predicts house prices from features like area, bedrooms, bathrooms and amenities. Built with Python and scikit-learn using data cleaning, encoding, scaling and EDA. Linear Regression model achieves about 72% R² score on a dataset of 545 houses.

Table of Contents
Overview
Dataset
Project Workflow
Result
Tech Stack
Project Structure
How to Run
Future Improvements
Author
Overview

The goal of this project is to predict the price of a house based on its characteristics. It is a regression problem: the model learns patterns from houses with known prices and then estimates the price of unseen houses.

Dataset
Size: 545 houses
Target: price
Missing values: none
Feature	Description
area	Size of the house
bedrooms	Number of bedrooms
bathrooms	Number of bathrooms
stories	Number of floors
parking	Number of parking spaces
mainroad	Located on a main road (yes/no)
guestroom	Has a guest room (yes/no)
basement	Has a basement (yes/no)
hotwaterheating	Has hot water heating (yes/no)
airconditioning	Has air conditioning (yes/no)
prefarea	Located in a preferred area (yes/no)
furnishingstatus	Furnished / semi-furnished / unfurnished
Project Workflow
Data loading and exploration: checked data types, missing values and summary statistics.
Encoding: converted yes/no columns to 1/0 and furnishing status to numeric values.
Scaling: standardised area and price using StandardScaler.
EDA: correlation heatmap and histograms to understand feature relationships and distributions.
Train-test split: 80% training and 20% testing.
Model training: Linear Regression.
Evaluation: R² score on the test set.
Result
Model	R² Score
Linear Regression	~72%

Note: R² shows how much of the variation in price the model explains. It is not the same as classification accuracy.

Tech Stack
Python
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
Jupyter Notebook
Project Structure
house-price-prediction/
├── house_price_prediction.ipynb   # Main notebook
├── Housing.csv                    # Dataset
├── requirements.txt               # Libraries needed
└── README.md                      # Project documentation
How to Run
Clone the repository
bash
   git clone https://github.com/iamsiva12/house-price-prediction.git
   cd house-price-prediction
Install the required libraries
bash
   pip install -r requirements.txt
Open the notebook
bash
   jupyter notebook house_price_prediction.ipynb
Run all cells.
Future Improvements
Split the data before scaling to avoid data leakage
Apply a log transform to the skewed price column
Compare Ridge, Random Forest and XGBoost models
Use 5-fold cross-validation for more reliable scores
Tune hyperparameters with GridSearchCV
Add feature engineering (for example total rooms, area per bedroom)
Report MAE and RMSE and show feature importance

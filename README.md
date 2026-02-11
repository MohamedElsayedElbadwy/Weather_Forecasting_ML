Weather Prediction using Random Forest Regressor 🌦️🤖
Project Overview
This project aims to predict daily maximum temperatures (MaxTemp) using historical weather data. The focus was on handling a "messy" real-world dataset, performing extensive data cleaning, and feature engineering to build a robust regression model.


Challenges & Data Preprocessing 🛠️
The dataset initially contained significant noise and missing values. Here is how I handled the challenges:
• Handling Missing Values (NaNs): Columns with more than 60% missing data (like FTI, ITH, RVG) were dropped to reduce noise.
• Trace Precipitation: The Precip column contained 'T' (Trace), which was replaced with 0 and converted to a numeric float type.
• Feature Engineering (Date Extraction): To resolve DTypePromotionError and capture seasonality, I extracted Year, Month, and Day from the original Date column.
• Zero-Null Strategy: Applied mean/interpolation imputation to ensure a clean dataset with no null values before training.


Model 🧠
I chose the Random Forest Regressor because of its ability to handle non-linear relationships and its robustness against outliers in weather data.
• Algorithm: RandomForestRegressor
• Library: Scikit-learn
• Features Used: MinTemp, Precip, Year, Month, Day.


Results 📊
• Successfully trained the model to predict MaxTemp.
• Handled data inconsistencies and type errors effectively.
• (Optional: Add your R2 Score here, e.g., R2 Score: 92%)



How to Run
1. Clone this repository.
2. Install dependencies: pip install pandas numpy scikit-learn matplotlib.
3. Open the ipynb file in Jupyter Notebook or VS Code.

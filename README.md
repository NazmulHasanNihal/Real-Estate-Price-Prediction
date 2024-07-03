# Real Estate Price Prediction

This project aims to predict real estate prices using machine learning models. The dataset used for this project includes various features such as the number of bedrooms, bathrooms, property size, latitude, longitude, etc.

Prerequisites
Before you begin, ensure you have the following installed:

Python 3.7+
Pandas
Numpy
Matplotlib
Seaborn
Scikit-learn
Joblib

pip install pandas numpy matplotlib seaborn scikit-learn joblib

Data Preparation
Load the dataset: Load the dataset from a CSV file.
Handle missing values: Use SimpleImputer to fill missing values with the median.
Feature Engineering: Create a new feature, PRICE_PER_SQFT.

Exploratory Data Analysis
Pairplot: Visualize relationships between features using Seaborn's pairplot.

Data Preprocessing

Define Features:
Categorical features: ['BROKERTITLE', 'TYPE', 'STATE', 'MAIN_ADDRESS', 'ADMINISTRATIVE_AREA_LEVEL_2', 'LOCALITY', 'SUBLOCALITY', 'STREET_NAME']

Numerical features: ['BEDS', 'BATH', 'PROPERTYSQFT', 'LATITUDE', 'LONGITUDE']

Column Transformer: Use ColumnTransformer to apply StandardScaler to numerical features and OneHotEncoder to categorical features.

Train-Test Split: Split the data into training and testing sets using train_test_split.

Model Training and Evaluation
Scaling: Scale the features using StandardScaler.

Train Models:

Linear Regression
Random Forest Regressor
Gradient Boosting Regressor
AdaBoost Regressor

Evaluate Models: Evaluate the models using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R^2) metrics.

Hyperparameter Tuning: Use GridSearchCV to find the best hyperparameters for Random Forest and Gradient Boosting models.

Voting Regressor: Combine the best models using a Voting Regressor and evaluate its performance.

Feature Importance

Permutation Importance: Calculate and plot feature importance using permutation importance.

Save and Load Model

Save Model: Save the trained voting regressor model using joblib.

Predict New Data: Define a function to predict new data using the saved model.

This project demonstrates the process of building a machine learning model to predict real estate prices. By following these steps, you can understand how to handle data preprocessing, model training, evaluation, hyperparameter tuning, and making predictions on new data.
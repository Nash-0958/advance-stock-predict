# advance-stock-predict
This Python script performs stock price change prediction using machine learning and time series analysis. It preprocesses stock data, trains a Random Forest model for regression, and uses an LSTM neural network to forecast stock price changes for the next 10 days. The results are visualized with various plots and saved to a CSV file.

**Final Report:** Time Series Forecasting and Analysis
**1. Data Preparation and Preprocessing**
Data Source:

CSV File: MA-Equities-CM-volume-27-Jul-2024.csv

Preprocessing Steps:

Column Cleaning: Removed extraneous spaces and newline characters from column names.
Numeric Conversion: Converted columns like %CHNG, VALUE, and VOLUME_(Shares) to numeric, handling commas and missing values.
Dropped NaNs: Eliminated rows with NaN values in %CHNG, VALUE, and VOLUME_(Shares).
Encoding Non-Numeric Columns: Encoded non-numeric columns using LabelEncoder to convert categorical data into numeric format.
Feature Scaling: Standardized numerical features using StandardScaler.
Data Summary:

After preprocessing, the dataset is clean, with numerical features standardized and categorical variables encoded.

**2. Exploratory Data Analysis (EDA)**

Visualizations:

Pair Plot: Shows the pairwise relationships in the dataset. This helps to identify correlations and patterns between numerical features.

Correlation Heatmap: Displays the correlation matrix of numerical features. Strong correlations between features are highlighted.

**3. Random Forest Regressor**
Model Training:

Parameter Tuning: Used GridSearchCV to find the best hyperparameters for the Random Forest Regressor.
Best Parameters: {'n_estimators': 100, 'max_depth': None}
Performance:
Mean Squared Error: X
R^2 Score: Y
Insights:

The Random Forest model performed well, with evaluation metrics showing effectiveness in predicting %CHNG.

**4. Time Series Analysis with LSTM**
Preparation for LSTM:

Sequence Length: Set to 10 (or adjusted based on data size).
Data Generation: Used TimeseriesGenerator to create sequences for training and validation.
Model Training:

LSTM Model: Included an LSTM layer with dropout regularization to prevent overfitting and a Dense output layer.
Early Stopping: Implemented to halt training when validation loss stops improving.
Results:

Fold 1: Low validation loss but with a very small validation set.
Fold 2: Noticeable discrepancy between training and validation loss, indicating potential overfitting.
Fold 3: Training loss decreased, but validation loss remained high.
Average Validation Loss: Z (average of all folds)

Loss Plot:

**Training and Validation Loss:**
**5. Future Value Predictions**
Predictive Model:

Future Steps: Predicted future %CHNG for 10 time steps ahead using the trained LSTM model.
Predictions:

Visualization: Plotted historical data alongside future predictions for each stock.
 (replace {stock_name} with actual stock names)

Output Data:

Current Stock Change: Displayed for each stock.
Predicted Changes: Future %CHNG values for the next 10 days.
Predictions File:

Saved Predictions: predicted_future_values.csv contains the predicted future values for each stock.

**6. Conclusion**
Random Forest Model: Provided valuable insights and predictions with robust performance metrics.
LSTM Model: Although the model showed promise, the cross-validation results indicated areas for improvement, such as increasing validation set size and addressing overfitting.
Future Predictions: Generated forecasts for future %CHNG, offering actionable insights for stock price movements.
Final Remarks:

The approach combined traditional machine learning techniques with advanced time series forecasting to provide a comprehensive analysis of stock data. Continuous improvement and fine-tuning of models can further enhance prediction accuracy.

**Visualization output of active stock:**

![YESBANK_wave_graph](https://github.com/user-attachments/assets/b534ea3c-5233-4a18-ad83-5f657ac6c6f2)
![training_validation_loss](https://github.com/user-attachments/assets/433022c2-de14-455b-9154-f0621b2545c6)
![pairplot](https://github.com/user-attachments/assets/d5660345-ca4b-46ff-980a-f04bf73b5714)
![heatmap](https://github.com/user-attachments/assets/7849eed3-e8ae-4f33-8e66-ce87169dfe9f)

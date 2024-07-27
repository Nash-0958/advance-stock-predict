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
![TTML_wave_graph](https://github.com/user-attachments/assets/0c2b57ef-7a6b-4c04-87b3-6f380da1e7d3)
![training_validation_loss](https://github.com/user-attachments/assets/433022c2-de14-455b-9154-f0621b2545c6)
![SUZLON_wave_graph](https://github.com/user-attachments/assets/c72224ce-d836-4fd7-8a7c-b241c70831d8)
![SJVN_wave_graph](https://github.com/user-attachments/assets/572db60d-b2d4-4274-a00c-61b5a4e99a4b)
![SANSTAR_wave_graph](https://github.com/user-attachments/assets/e22dcbd4-21e0-4cf9-89b8-1ddbfc7ee6d7)
![RTNPOWER_wave_graph](https://github.com/user-attachments/assets/19d3ab45-9b18-46a8-a536-0540e8b5cf45)
![pairplot](https://github.com/user-attachments/assets/d5660345-ca4b-46ff-980a-f04bf73b5714)
![NHPC_wave_graph](https://github.com/user-attachments/assets/3b3b87c6-bdf2-4534-afd9-ef1ad1a17293)
![MMTC_wave_graph](https://github.com/user-attachments/assets/59be621b-627f-4499-ae21-ecaa38f1894c)
![JPPOWER_wave_graph](https://github.com/user-attachments/assets/f2b506d7-4aa8-409e-bec3-6c83e2e2ca17)
![IRFC_wave_graph](https://github.com/user-attachments/assets/e71fc9f2-2ac3-4b4c-9581-24be9436ffe8)
![INFIBEAM_wave_graph](https://github.com/user-attachments/assets/6e2c9617-368b-4cc0-b4ce-352127b74858)
![IFCI_wave_graph](https://github.com/user-attachments/assets/bf5f19d9-9be6-4dff-a350-313964046e7f)
![IDFCFIRSTB_wave_graph](https://github.com/user-attachments/assets/6839c58e-94cd-4af2-9df7-a434a6702376)
![IDEA_wave_graph](https://github.com/user-attachments/assets/8a19f54b-e644-4592-8c88-40bbc0b06273)
![IDBI_wave_graph](https://github.com/user-attachments/assets/e7021192-143e-4a1b-976f-7a14e7b1cd11)
![heatmap](https://github.com/user-attachments/assets/7849eed3-e8ae-4f33-8e66-ce87169dfe9f)
![HCC_wave_graph](https://github.com/user-attachments/assets/2d19a6c1-f752-4d94-b225-22fea1664d87)
![GTLINFRA_wave_graph](https://github.com/user-attachments/assets/da6ef623-dc5b-493e-8e76-6dac240280f6)
![CANBK_wave_graph](https://github.com/user-attachments/assets/0914f43d-2db2-44bb-bd95-9536e2cc6262)
![ASHOKLEY_wave_graph](https://github.com/user-attachments/assets/fd08785e-a465-4773-a8ba-5e8649eb698c)

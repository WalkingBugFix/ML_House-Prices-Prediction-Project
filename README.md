# ML_House-Prices-Prediction-Project
Develop a predictive model that accurately estimates the sale price of residential homes based on a variety of features describing their physical attributes, location, quality, and other relevant characteristics.

**Solution:**

To address the problem of predicting house prices using the given dataset, a structured and methodical approach was adopted, encompassing exploratory data analysis (EDA), feature engineering, and advanced regression modeling techniques.

Initially, EDA and feature engineering were performed on the training dataset to understand data distributions, handle missing values, detect outliers, and create meaningful derived features. Feature selection techniques were applied to retain only the most relevant predictors, followed by feature scaling to normalize numerical features and prepare the data for model training.

To prevent data leakage, the same preprocessing steps (EDA, feature engineering, feature selection, and scaling) were applied to the test dataset separately, without referencing the training set.

After preparing both datasets, the cleaned test data was imported into the primary training notebook for model evaluation and prediction. Various regression models were evaluated, with XGBoost emerging as the best-performing model. Random Forest also performed competitively, but XGBoost was chosen due to its slightly superior performance and better generalization on validation data. The selected model achieved a Root Mean Squared Logarithmic Error (RMSLE) of 0.154253 on the validation dataset.

The final predictions were inverse log-transformed to revert to the original price scale and then saved to a CSV file for submission, following the required format.

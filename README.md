# Carbon Intensity Forecast BI

This project forecasts carbon intensity using various machine learning models and data from different regions of India. The pipeline includes data collection, preprocessing, model training, evaluation, and result analysis.

## Project Pipeline

1. **Data Collection**
   - Raw hourly data for each region is stored in the `BI DATA/` folder, organized by region and year.
   - Files like `IN-EA_2021_hourly.csv` contain hourly data for Eastern region for 2021, and similarly for other regions and years.

2. **Data Combination**
   - `all_regions_combined_data.csv`: Combines all regional data into a single dataset for unified analysis.

3. **Preprocessing**
   - `data_preprocessing.ipynb`: Jupyter notebook for cleaning, scaling, and transforming raw data.
   - `processed_data.csv`: Output of preprocessing, ready for modeling.
   - `minmax_scaler.pkl`, `standard_scaler.pkl`, `pytorch_lstm_scaler_X.pkl`, `pytorch_lstm_scaler_y.pkl`: Saved scaler objects used for feature scaling.
   - `preprocessing_info.json`: Metadata about preprocessing steps.

4. **Model Training & Evaluation**
   - **Linear Regression**
     - `linear_reg_model.ipynb`: Notebook for training linear regression model.
     - `linear_regression_model.pkl`: Saved linear regression model.
     - `linear_regression_results.csv`: Predictions and evaluation metrics.
     - `linear_regression_summary.json`: Summary of model performance.
   - **LSTM (PyTorch)**
     - `lstm_model.ipynb`: Notebook for training LSTM model.
     - `pytorch_lstm_model.pth`, `best_pytorch_lstm_model.pth`: Saved PyTorch LSTM models.
     - `pytorch_lstm_results.csv`: LSTM predictions and metrics.
     - `pytorch_lstm_summary.json`: LSTM model performance summary.
   - **XGBoost**
     - `xg_boost_model.ipynb`: Notebook for XGBoost model training.
     - `xgboost_model.pkl`: Saved XGBoost model.
     - `xgboost_results.csv`: XGBoost predictions and metrics.
     - `xgboost_summary.json`: XGBoost model performance summary.
     - `xgboost_shap_samples.csv`, `xgboost_shap_values.npy`: SHAP values for model interpretability.

5. **Documentation & Utilities**
   - `Docs/`: Contains reference code and pipeline documentation.
     - `import pandas as pd.txt`: Example code for importing pandas.
     - `pipeline.txt`: Text description of the pipeline.

## File Descriptions

- **all_regions_combined_data.csv**: Combined data from all regions and years.
- **processed_data.csv**: Preprocessed data ready for modeling.
- **BI DATA/**: Raw data files organized by region and year.
- **minmax_scaler.pkl, standard_scaler.pkl, pytorch_lstm_scaler_X.pkl, pytorch_lstm_scaler_y.pkl**: Scaler objects for feature scaling.
- **preprocessing_info.json**: Details of preprocessing steps.
- **linear_reg_model.ipynb, lstm_model.ipynb, xg_boost_model.ipynb**: Notebooks for model training.
- **linear_regression_model.pkl, pytorch_lstm_model.pth, best_pytorch_lstm_model.pth, xgboost_model.pkl**: Saved models.
- **linear_regression_results.csv, pytorch_lstm_results.csv, xgboost_results.csv**: Model predictions and metrics.
- **linear_regression_summary.json, pytorch_lstm_summary.json, xgboost_summary.json**: Model performance summaries.
- **xgboost_shap_samples.csv, xgboost_shap_values.npy**: SHAP values for XGBoost interpretability.
- **Docs/**: Documentation and code snippets.

## How to Use

1. Review the data in `BI DATA/` and `all_regions_combined_data.csv`.
2. Run preprocessing using `data_preprocessing.ipynb`.
3. Train models using respective notebooks.
4. Evaluate results and review summaries.
5. Refer to `Docs/` for additional information.

---

Feel free to reach out for any clarifications or contributions!

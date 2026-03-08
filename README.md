# Regression Model Comparison and Validation

This project evaluates multiple linear regression models using different transformation and model correction strategies. The objective is to determine which model provides the best balance between explanatory power and predictive performance.

## Models Compared
Five regression models were constructed using different transformation strategies:

- Model 1: Linear regression with original variables
- Model 2: Linear regression with predictor transformation
- Model 3: Log transformation of the response variable
- Model 4: Log transformation of both response and predictors (log-log model)
- Model 5: Box-Cox transformation

## Model Selection Criteria
Models were evaluated using several statistical metrics:

- Adjusted R-squared
- AIC (Akaike Information Criterion)
- BIC (Bayesian Information Criterion)

Among the five models, **Model 4 performed best**, achieving:

- Highest Adjusted R² (0.803)
- Lowest AIC (-363.4)
- Lowest BIC (-339.6)

These results suggest that the log-log transformation provides the best balance between model fit and complexity.

## Model Validation

Two validation approaches were used to assess predictive performance:

### 1. Training-Testing Validation
- Dataset randomly split into **80% training and 20% validation**
- Model training and prediction repeated **100 times**
- Mean Squared Error (MSE) computed for each model

Results showed that **Model 1 achieved the lowest average MSE (14.98)**, though differences across models were relatively small.

### 2. 10-Fold Cross Validation
- Dataset divided into **10 folds**
- Each fold used once as validation
- Average cross-validation error computed

Results indicate **Model 1 again produced the lowest average error (15.35)**, but all models demonstrated similar predictive performance.

## Key Insights

- Log transformation improves model fit and explanatory power.
- Model 4 (log-log transformation) performs best according to statistical metrics.
- Model 1 performs slightly better in predictive validation tests.
- Differences between models are relatively small, suggesting similar predictive capabilities.

## Tools Used

- Python
- pandas
- numpy
- statsmodels
- scikit-learn
- matplotlib

## Files

- `Assignment3.ipynb` – analysis notebook
- `dataset.csv` – dataset used in the study
- `report.pdf` – full analytical report

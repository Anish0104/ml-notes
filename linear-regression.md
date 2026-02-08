# Linear Regression

Linear regression models the relationship between input features and a continuous target variable.

## Formula

y = mx + b

Where:
- m = slope
- b = intercept

## Cost Function

Mean Squared Error (MSE):

MSE = (1/n) * Σ(y_pred - y_actual)^2

## Key Points
- Used for predicting continuous values
- Sensitive to outliers
- Assumes linear relationship

## Sklearn Example

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()
model.fit(X_train, y_train)
predictions = model.predict(X_test)

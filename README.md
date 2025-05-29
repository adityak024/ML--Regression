📊 Regression Analysis Project – Simple, Multiple & Polynomial
This project explores and implements Simple Linear Regression, Multiple Linear Regression, and Polynomial Regression to understand relationships between variables, build predictive models, and evaluate model performance using both theoretical concepts and practical implementation in Python.

📁 Project Contents
simple_linear_regression.py

multiple_linear_regression.py

polynomial_regression.py

regression_analysis.ipynb – All models combined in a single interactive notebook

datasets/ – Sample CSV datasets used for training and evaluation

README.md – Project documentation

📘 Theory & Concepts Covered
🔹 Simple Linear Regression
B. What is Simple Linear Regression?
Simple Linear Regression models the relationship between two variables using a straight line. It predicts the dependent variable (Y) based on the independent variable (X).

)- What are the key assumptions of Simple Linear Regression?

Linearity between X and Y

Homoscedasticity (constant variance of errors)

Independence of observations

Normal distribution of residuals

5. What does the coefficient m represent in the equation Y = mX + c?
m represents the slope – the rate of change in Y with respect to X.

E. What does the intercept c represent in the equation Y = mX + c?
c is the Y-intercept, the predicted value of Y when X = 0.

2. How do we calculate the slope m in Simple Linear Regression?
Using the formula:

ini
Copy
Edit
m = Σ((Xi - X̄)(Yi - Ȳ)) / Σ((Xi - X̄)²)
. What is the purpose of the least squares method?
To minimize the sum of squared residuals (errors), ensuring the best-fitting line.

#. How is the coefficient of determination (R²) interpreted?
R² indicates the proportion of the variance in Y explained by X. R² = 1 is a perfect fit.

🔸 Multiple Linear Regression
. What is Multiple Linear Regression?
An extension of linear regression with two or more independent variables predicting a single dependent variable.

A. Main difference from Simple Linear Regression:
Multiple predictors are used instead of just one.

BD. Key assumptions of Multiple Linear Regression:

Linearity of relationships

No or low multicollinearity

Homoscedasticity

Normal distribution of residuals

BB. What is heteroscedasticity?
It refers to non-constant variance of residuals, which can invalidate statistical tests.

B). Improving multicollinearity:

Use Variance Inflation Factor (VIF) to detect it

Remove or combine correlated features

Apply regularization techniques (Ridge, Lasso)

B5. Transforming categorical variables:

Use One-Hot Encoding, Label Encoding, or Ordinal Encoding

BE. Role of interaction terms:
They capture the combined effect of two or more variables on the outcome.

B2. Interpretation of intercepts:
In multiple regression, intercept is the predicted Y when all X variables = 0, which may not be meaningful.

B. Significance of slope:
Represents the effect of each predictor on Y, holding other variables constant.

B#. Intercept context:
Helps understand the baseline value of Y before adding effects from predictors.

B. Limitations of using R² alone:

Doesn’t penalize complexity

May be high even for irrelevant models

BA. Large standard error interpretation:
Indicates low confidence in the estimated coefficient – it may not be statistically significant.

). Heteroscedasticity in residual plots:**
Seen as a funnel shape or pattern. It violates regression assumptions and must be addressed with transformations or robust regression.

)B. High R² but low Adjusted R²:
Suggests that additional variables don’t improve the model and may be overfitting.

)). Why scale variables?
Important for algorithms sensitive to magnitude (e.g., gradient descent), and for comparing feature importance.

🔷 Polynomial Regression
)5. What is polynomial regression?
It models nonlinear relationships by adding higher-degree terms of the predictor(s).

)E. How does it differ from linear regression?
Polynomial regression can fit curved lines, unlike the straight line of linear regression.

)2. When is it used?
When data shows nonlinear trends that linear models cannot capture.

). General equation:

ini
Copy
Edit
Y = b0 + b1X + b2X² + b3X³ + ... + bnXⁿ
)#. Can it be applied to multiple variables?
Yes, with interaction and polynomial terms for each variable (e.g., X1², X1*X2).

). Limitations:

Prone to overfitting with high degrees

Sensitive to outliers

)A. Model fit selection:
Use cross-validation, AIC/BIC, and adjusted R² to choose optimal polynomial degree.

5D. Why visualization matters:
Helps assess how well the curve fits the data and identifies under/overfitting.

5B. Implementation in Python:
Use PolynomialFeatures from sklearn.preprocessing, and model with LinearRegression.

🛠️ Tools & Libraries Used
Python

pandas, numpy – Data wrangling

matplotlib, seaborn – Visualization

sklearn.linear_model – Regression models

sklearn.preprocessing – Feature engineering

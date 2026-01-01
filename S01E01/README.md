Summary
- Goal: Predict yearly customer spending using session/app/website usage and membership length.
- Dataset: "Ecommerce Customers.csv" (500 rows, 8 columns).

What we did
- Loaded data with pandas and inspected (head, info, describe, nulls).
- Exploratory Data Analysis with seaborn:
    - Jointplots for Time on Website and Time on App vs Yearly Amount Spent.
    - Pairplot for overall variable relationships.
    - Regression plot for Length of Membership vs Yearly Amount Spent.
- Prepared features X = ['Avg. Session Length','Time on App','Time on Website','Length of Membership'] and target y = 'Yearly Amount Spent'.
- Split data: train/test (70%/30%) with sklearn.model_selection.train_test_split.
- Trained a LinearRegression model (sklearn).
- Predicted on X_test and visualized predictions vs actuals.

Key findings
- Length of Membership is the strongest positive predictor of yearly spending.
- Time on App has a noticeable positive effect; Time on Website shows little to no positive effect.
- Model predictions align reasonably well with actual values (scatter plot of y_test vs predictions used for visual evaluation).
- Coefficients were inspected to determine feature importance.

Files / Cells of interest
- Data load and inspection (cell where df is read).
- EDA: jointplot, pairplot, lmplot cells.
- Modeling: feature selection, train_test_split, LinearRegression fit, predictions, coefficient inspection, scatter plot of predictions.

Dependencies
- pandas, matplotlib, seaborn, scikit-learn, numpy

Next steps / Improvements
- Compute quantitative metrics (MSE, RMSE, R^2) for model evaluation.
- Try regularization (Ridge/Lasso) or more complex models if needed.
- Feature engineering (interaction terms, normalization) and cross-validation.
- Investigate causal factors or business experiments to validate model-driven recommendations.

Conclusions for business
- Prioritize improving and retaining long-term members.
- Invest more in the mobile app experience (higher ROI) than the desktop website based on this dataset.

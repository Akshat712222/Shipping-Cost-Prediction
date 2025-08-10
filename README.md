Shipping Cost Prediction
By Akshat Garg

Accurately forecasting logistics expenses is a cornerstone of financial planning for any business involved in shipping goods. This project addresses the critical task of predicting shipping costs by leveraging machine learning to analyze the various factors that influence freight charges. By creating a reliable predictive model, businesses can optimize their supply chain, offer competitive pricing, and improve budget accuracy.

Python libraries such as Pandas, NumPy, Scikit-learn, and XGBoost are employed to process the data, train the model, and evaluate its performance in predicting shipping costs.

Dataset Description
The dataset for this project contains transactional data for various shipments, detailing the key attributes associated with each freight movement. The primary data is stored in shipment.csv.

Column Name

Description

Country

Destination country of the shipment.

Shipment Mode

The method of transportation (e.g., "Air", "Ocean").

Manufacturing Site

The location where the product was made.

Weight (Kilograms)

The gross weight of the shipment.

Line Item Value

The total value of the items in the shipment.

Pack Price

The price per pack of the item.

Unit Price

The price per unit of the item.

Freight Cost (USD)

The target variable; the total cost of the shipment in USD.

Model Selection
To achieve the highest accuracy in predicting shipping costs, the XGBoost Regressor was selected as the final model. XGBoost (Extreme Gradient Boosting) is a powerful and efficient implementation of the gradient boosting framework. It excels at handling complex, non-linear relationships in tabular data and consistently delivers high performance through its optimized tree-based learning algorithm.

Other models were also evaluated to benchmark performance:

Linear Regression

Random Forest Regressor

Support Vector Regressor (SVR)

Neural Network

Model Performance: R-squared Score
The performance of each model was measured using the R-squared (R 
2
 ) metric, which indicates the proportion of the variance in the dependent variable that is predictable from the independent variables.

Model

R-squared (R 
2
 ) Score

Linear Regression

0.78

Support Vector Regressor

0.84

Random Forest Regressor

0.89

Neural Network (Keras)

0.87

XGBoost Regressor

0.94

Why the Model is Not Overfitting
Several checks were performed to ensure the model generalizes well to new, unseen data and is not overfitting to the training set.

Cross-Validated R-squared: The model achieved a consistent cross-validated R 
2
  score of 0.92, indicating stable performance across different subsets of the data.

Residuals Plot: The plot of the model's residuals (the differences between predicted and actual values) shows a random pattern centered around zero. This lack of a discernible pattern confirms that the model's errors are random and not systematic, which is a key indicator of a well-fitted model.

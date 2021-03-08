## Overview/Problem Statement

In this project, I will be evaluating different housing features like "bathroom quality, kitchen size, and roof styles" to optimize a model which predict house prices. Through the qualitatively impact features the homeowners who wishes to sell their house will be able to identify which features of their house should or shouldn't be mentioned to their real estate agent to get the most value out of the pricing.

## Data

The data given consisted of 2 datasets with roughly 80 unique features that are both numerical and categorical. Only one of the 2 datasets contain the SalePrice column, which contains the price of the house. That dataset will be used as a model to predict the price of the house in the second dataset.

## Process

The process will start off with assessing null values within the data, and outliers that may negatively impact the quality of our models.
Creating additional features, such as age and total living space, that may increase the accuracy of our model's prediction
LinearRegression, Lasso, Elastic, and Ridge models will be created and evaluated in this project. The first sets of models used features that have the highest correlation with the price of the house. This model was decent but underfitting.
To counter the high bias, low variance problem from he first sets of models, models that contained large amount of features were made. Using lasso and Elastic models, we can determine the quality of each features. Ones that are negatively impacting our models' quality will be zeroed out.
Once the quality features were defined we can create an optimized model, in which did not contain too high or too low variance. Additionally, it perform decently well on unseen data. 

## Evaluation of the features / Business Recommendation
### Product model: Ridge model with 55 most impactful features (dummies included)
Due to the quality of the features, none of them were zeroes out.
The Models that came before this one were overfitting and underfitting. This model was the most obtimal out of all my models. This is due to the 55 features (dummy features included) which is not a overwhelming amount of variance. This model perform well on unseen data since the 55 features were filtered as the most possitively impactful features (None was zeroed out).
The features that relates to sizing (size of the living space, lot, garage, etc.), quality and condition (in excellent quality), location (neighborhood), and age has the highest impact on the price of the house
Age being the most negatively impacting the price of the house. With an increase in only 1 year of age, the price of the house would roughly drop by USD 10,000.
As a homeowner looking to improve the price of a house, making changes to the quality of the interior takes priority. For example, ensuring that the quality of the kitchen is excellent will roughtly drive the price of your house by USD 5600.
The NeightborHoods that increase the price of the house ordering from highest increase to lowest increase: Neighborhood_NridgHt, Neighborhood_StoneBr, Neighborhood_NoRidge, Neighborhood_Somerst, Neighborhood_Crawfor, and Neighborhood_NWAmes (This neighborhood has negative impact to price)
Because Neightborhood helps a lot with the quality of my model, the model is not generalize universally. However, this model would perform okay without the Neightboorhood features on other cities.
At the base, the price of houses would start at 181, 350
Most Impactful features (in order): Ground Living Area, Age, Overall Qual, Total Interior space, Total Basement space, Overall Condition.

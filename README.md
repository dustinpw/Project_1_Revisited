# Food Sales Predictions 
An analysis to confirm the best model to be used for predicting food sales at different types of grocery stores.

**Author**: Dustin W

### Business problem:

To help the retailer understand the properties of products and outlets that play crucial roles in predicting sales


### Data:
![sample image](download_3(1).png)


## Methods
- Linear Regression Model
- Decision Tree Regressor Model
- Tuned Decision Tree Regressor Model

## Results




#### Heatmap of all numeric columns in dataset
![sample image](download_1.png)

> The heatmap the correlation of the numeric columns of the dataset. There is not much correleation, but Item_MRP and Item_Outlet_Sales have the greatest correlation.
#### Scatterplot of MRP and Item Outlet Sales
![sample image](download_2.png)

> To expand further on the correlation mentioned above, the scatter plot below confirms that as Item_MRP increases, so does Item_Outlet_Sales. This is an example of a positive correlation.
## Model

- Linear Regression Model (Testing Set):
  - R^2: -6.835227208182029e+23
  - RMSE: 1373252949182061.8

- Decision Tree Regressor Model (Testing Set):
  - R^2: 0.5960564372160062
  - RMSE: 1373252949182061.8


## Recommendations:

I recommend using the Regression Tree Model to predict sales. The R2 score for the training and testing data is about .6. The model can explain 60% of the variation in the target for the training and testing datasets.



For any additional questions, please provide a comment.

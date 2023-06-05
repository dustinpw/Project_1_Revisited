# Project_1_Revisited
 
# Food Sales Predictions 
An analysis to confirm the best model to be used for predicting food sales at different types of grocery stores.

**Author**: Dustin W

### Business problem:

To help the retailer understand the properties of products and outlets that play crucial roles in predicting sales


### Data:
<p align="center">
  <img src="/png/download_3.png" width="60%" height="60%">
</p>


## Methods
- Linear Regression Model
- Decision Tree Regressor Model
- Tuned Decision Tree Regressor Model

## Results




#### Heatmap of all numeric columns in dataset
<p align="center">
  <img src="/png/download_1.png" width="60%" height="60%">
</p>


> The heatmap the correlation of the numeric columns of the dataset. There is not much correleation, but Item_MRP and Item_Outlet_Sales have the greatest correlation.
#### Scatterplot of MRP and Item Outlet Sales
<p align="center">
  <img src="/png/download_2.png" width="60%" height="60%">
</p>


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

## Importances & Coefficients

<p align="center">
  <img src="/png/LR_Top3.png" width="75%" height="75%">
</p>

The top 3 most impactful features and the interpretations of their coefficients are as follows:
- If the store is classified as Outlet_Type_Supermarket Type3, the model will increase Item_Outlet_Sales by $2091.64

- If the store is classified as Outlet_Size_High, the model will increase the Item_Outlet_Sales by $614.94

- If the store is classified as Outlet_Type_Grocery Store, the model will decrease the Item_Outlet_Sales by $1526.50

<p align="center">
  <img src="/png/Dec_tree_top5.png" width="75%" height="75%">
</p>

The top 5 most important features for the model are `Item_MRP`, `Outlet_Type_Grocery Store`, `Outlet_Type_Supermarket Type3`, `Outlet_Establishment_Year`, `Outlet_Type_Supermarket Type1`. 

- The most important of these 5 is `Item_MRP` and the least important is `Outlet_Type_Supermarket Type1`. Any feature outside of these 5 are unimportant features for the model.


## SHAP Summary Plots for Global Explanations

<p align="center">
  <img src="/png/bar_sum.png" width="75%" height="75%">
</p>

Both the top 3 most impactful features found by shap vs feature importance are the exact same.


<p align="center">
  <img src="/png/dot_sum.png" width="75%" height="75%">
</p>

Item_MRP, Outlet_Type_Grocery Store, Outlet_Type_Supermarket Type3 are the most important features.

- If the there is a higher Item MRP the model is likely to predict higher sales

- A grocery store is likley to predict lower sales

- A super market type 3 is likely to predict higher sales


## Lime Tabular explantions 
Since the target feature we are analyzing is the Outlet Sales, I decided to use 2 samples. 1 sample is from a high outlet sales and the other sample is from a low outlet sales.


<p align="center">
  <img src="/png/lim_least.png" width="75%" height="75%">
</p>

<p align="center">
  <img src="/png/lim_high.png" width="75%" height="75%">
</p>


- Both the Least Sales and Highest Sales top 3 influential features are the same. 
- In the highest sales, it shows 2 additional features that negatively impact the total sales amount.


## Individual Force Plot 

<p align="center">
  <img src="/png/least.png" width="75%" height="75%">
</p>

- Accoriding to SHAP, Outlet Type Grocery Store and Item MRP provided the greatest influence to sales
- 
<p align="center">
  <img src="/png/highest.png" width="75%" height="75%">
</p>

- Accoriding to SHAP, Outlet Type Grocery Store, outlet type supermarket, and Item MRP provided the greatest influence to sales

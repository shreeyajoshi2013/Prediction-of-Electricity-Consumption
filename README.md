# Prediction of Electricity Consumption 

Goal of this project is building a data model that predicts electricity consumption, located in the KWH field in the dataset.
This dataset contains information of energy costs and usage for heating, cooling, appliances and other end uses, from a sample of housing units. <br>
The dataset taken from [link](https://www.eia.gov/consumption/residential/data/2009/index.php?view=mic). <br>
(Number of Rows: approx. 12000, <br>
Number of Columns: approx. 940)

### Built with

* Google Colab

### Highlights
* Random Forest Regressor <br>

### Libraries used 
* Pandas
* Numpy
* Matplotlib
* Seaborn
* Scikit-learn <br>


### What is being done?

1.   Data understanding <br>
      * Data exploration
2.   Data preparation <br>
      *  One-Hot Encoding the categorical columns <br>
      *  Handling NaN values <br>
      *  Removing the unneacesary columns <br>
      *  Assumptions and considerations: <br>
      *   Columns starting with 'Z' are the imputation flags for other variables. So are to be removed as they will not contribute in the prediction.<br>
      *   Columns with thermal unit other than KWH are assumend to be not helpful. Hence are removed. <br>
      *   Columns which show the total consumptions of elements' electricity usage are redundant as the individual contributions by those elements are already present in the data. Hence are removed for avoiding data redundancy. <br>
3.   Data Analysis <br>
      * Finding the correlation of features with output variable and visualizing <br>
4.   Random Forest Regressor <br>
      *  Using GridSearchCV for selecting optimal hyperparameters for the model <br>
      *  Choosing important features by calculating feature importances <br>

## Conclusion <br>
There are about 14 features from the entire dataset that are found to be contributing the most towards the consumption of electricity, and are found after several steps of data cleaning, processing and feature engineering. <br>
Random Forest Regressor is giving fair output for prediction of the consumption in Kilo Watt Hour (KWH ) with R2 score of 0.875. With more data exploration and manipulation, more optimised prediction can be obtained.

### Further Tasks <br>
Other models such as Neural Networks can be used for the prediction. <br>
The features can be dugged deep with more EDA and by using libraries such as FeatureSelector to further improve the model and working more on feature importance.

### References <br>
*  https://towardsdatascience.com/a-feature-selection-tool-for-machine-learning-in-python-b64dd23710f0
*  https://machinelearningmastery.com/feature-selection-with-real-and-categorical-data/
*  https://www.youtube.com/watch?v=ioXKxulmwVQ&t=0s
*  https://towardsdatascience.com/a-feature-selection-tool-for-machine-learning-in-python-b64dd23710f0
*  https://machinelearninghd.com/gridsearchcv-hyperparameter-tuning-sckit-learn-regression-classification/
*  https://towardsdatascience.com/improving-random-forest-in-python-part-1-893916666cd

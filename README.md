# Prediction of Electricity Consumption 

Goal of this project is building a data model that predicts electricity consumption, located in the KWH field in the dataset.
This dataset contains information of energy costs and usage for heating, cooling, appliances and other end uses, from a sample of housing units. <br>

The dataset taken from [link](https://www.eia.gov/consumption/residential/data/2009/index.php?view=mic).

### Built with

* Google Colab

### Libraries used 
* Pandas
* Numpy
* Matplotlib
* Seaborn
* Scikit-learn <br>

### Highlights
* Random Forest Regressor <br>


### What is being done?

1.   Data understanding <br>
    *  Data exploration  <br>
2.   Data preparation <br>
    *  One-Hot Encoding the categorical columns <br>
    *  Handling NaN values <br>
    *  Removing the unneacesary columns <br>
       *  Assumptions and considerations: <br>
            *   Columns starting with 'Z' are the imputation flags for other variables. So are to be removed as they will not contrubute in the prediction.<br>
            *   Columns with thermal unit other than KWH are assumend to be not helpful. Hence are removed. <br>
            *   Columns which show the total consumptions of elements' electricity usage are redundant as the individual contributions by those elements are already present in the data. Hence are removed for avoiding data redundancy. <br>
3.   Data Analysis <br>
    * Finding the correlation of features with output variable and visualizing <br>
4.   Random Forest Regressor <br>
    *  Using GridSearchCV for selecting optimal hyperparameters for the model <br>
    *  Choosing important features by calculating feature importances <br>

## Conclusion <br>

##Further Tasks <br>
##References <br>
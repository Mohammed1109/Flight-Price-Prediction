# Flight-Price-Prediction
# Introduction
<h4>Objective:</h4> Develop a machine learning model that can accurately predict flight prices based on various input features.
<h4>Features Considered:</h4> The dataset contains Airline, Date_of_journey, source, destination, route, departure_time, arrival_time ,  duration, total_stops, additional_info, price.

# Data Exploration and Preprocessing
<li>Except for the Price feature every other feature had dtype as the object that needed to be processed. Features such as Airline, Source, Destination, Total_Stops, and Additional_Info are categorical features while the rest had object type but the values were continuous.</li>

<li>Checking missing values and duplicates in the dataset and then drop that missing and duplicate values to maintain data integrity. Converting total_stops into numerical feature for better understanding. Dividing dataset into numerical and categorical features and then do label encoding for the categorical features.</li>

<li>The Date of the Journey, Departure Time, and Arrival Time had datatype as an object whereas it is then changed to datetime for better understanding. Furthermore, the Date of the Journey was split into Journey day and Journey month. Similarly, Departure Time and Arrival Time were split into Hours and Minutes. After conversion Date of the Journey, Departure Time, and Arrival Time were dropped. And, duration was converted into minutes and convert that feature into numerical format.</li>

<li>Checking for outliers also using boxplot for different features and then removing that outlier using zscore method. Also improving the skew for continuous feature.</li>



# EDA
<li>Finding the average price for all months to get the analysis in which month price is less</li> 
<li>Finding the average price for a particular flight in each month</li>
<li>Finding number of flight per day for each airline across all month</li>
<li>Finding number of flight per day for each airline from a every source for each month</li>
<li>Finding the average price with respect to stops for each airline</li>
<li>Checking the average price with respect to the number of stops for each airline.</li>
<li>Analyzing the most preferable stop that most of the airlines preferred.</li>
<li>Analyzing the average price between the source and destination for each airline.</li>

# Model Building
<li>This problem is of regression which can be solved by a Regression model. Models such as Linear Regression, Random Forest Regressor, Decision tree, bagging, Adaboost, ExtraTree 
    regressor, Gradient Boosting, XGBoost are used to build and predict flight ticket prices. </li>
<li>First, Linear Regressor is built with every feature to predict the R2 score. After that I do cross validation for that linear regression model. Then I built and analyze model with 
    different algorithms and get the R2 score.</li>

# Model Evaluation

| Model                     | MSE          | MAE          | R2            |
|---------------------------|--------------|--------------|---------------|
| Linear Regression         | 7538341.9679 | 2171.0000    | 0.5282        |
| Random Forest Regressor   | 1292145.0764 | 596.93898    | 0.9191        |
| Decision Tree Regressor   | 2000910.2661 | 646.08217    | 0.8748        |
| Bagging Regressor         | 1355474.3039 | 616.77545    | 0.9152        |
| ExtraTrees Regressor      | 1213055.5124 | 548.72345    | 0.9241        |
| AdaBoost Regressor        | 6328993.8876 | 2120.81984   | 0.6039        |
| Gradient Boost Regressor  | 2626301.3866 | 1169.57325   | 0.8356        |
| XG Boost Regressor        | 1120845.9965 | 647.20978    | 0.9298        |

# Conclusion
XG Boost Regressor has the least MSE among all the models which is followed by Extra Trees Regressor. Also, the accuracy of XG Boost is 93% we can say and 92.4% for ExtraTrees Regressor. However, the Linear Regression model has an accuracy score of only 53% also it has high MSE and MAE in comparison to other models.
 

# Used Car Price Prediction Model
## Abstract:
Machine learning is a technology that has seen a
rapid increase in popularity and usage over the last few years.
It is rapidly progressing with vast capabilities and applications
in automating processes that do not require human
participation or explicit programming. The power of machine
learning is so strong that its applications may be found
practically everywhere in our daily lives. Many previously
unsolved problems have been solved by machine learning, and
businesses around the world have advanced significantly. In this
project, we'll look at one such real-world scenario and use
machine learning to create a model. The price of the car begins
to decrease as soon as it is purchased, and continues to
depreciate with every passing year. The value of a car drops to
1/5th of its price in the first year. Our goal is to create a machine
learning model that estimates the value based on characteristics
such as total kilometres driven, overall vehicle condition, and
several other parameters that influence the car's resale value in
the Indian market. As we advance with this project, we'd like to
train our model to not only anticipate the price, but also to assist
the seller in obtaining the best possible price.

## Dataset:
The data was downloaded from kaggle having 1000 enteries and 6 columns. The 5 features of the ML model are: company, model,fuel_type, kms_driven and the year. 
| Feature | Description |
| --- | --- |
| `company` | The company of the car eg: Tesla, Maruti etc|
| `model` | Show model of the car eg: Maruti Suzuki 800 |
| `fuel_type` | Indicates the fuel type of the model eg: Petrol, Diesel etc |
| `year` | The year in which the car was purchased |
| `kms_driven` | The number of kilometers the car has driven |

## Data PreProcessing
We began by inspecting the dataset for any missing values. Next, we addressed data type inconsistencies: the 'year' column, initially in string format, was converted to an integer for better handling in modeling. The 'price' column, also in string format, contained commas which were removed. Five rows in the 'price' column had erroneous values, and given the negligible impact (ratio of 1000:5), we chose to drop these rows. After cleaning, we split the data, treating 'Price' as the target variable and using the remaining columns as features for model training.

## EDA
1. **Data Distribution Analysis**: I started by analyzing the distribution of key numerical features like 'price' and 'year' using histograms and box plots. This helped me identify outliers, understand the spread of the data, and spot any skewness that might affect model performance.

2. **Summary Statistics**: I generated summary statistics for all numerical columns to get an overall view of the dataset. This included calculating the mean, median, standard deviation, and quartiles to understand central tendencies and variation in the data.

3. **Correlation Analysis**: To explore relationships between the features, I created a correlation matrix heatmap. This helped me identify which features were strongly correlated with the target variable ('Price') and if there were any multicollinearity issues among the independent variables.

4. **Outlier Detection**: I conducted an outlier analysis using Z-scores and box plots, particularly focusing on the 'price' column. This helped me identify any extreme values that could potentially skew the model results or require further treatment.

5. **Feature Relationships**: I visualized relationships between key features and the target variable by creating scatter plots. For instance, I looked at how 'year' and 'price' interacted, which gave me insights into possible trends and patterns that could guide feature selection for modeling.

These steps ensured a deeper understanding of the dataset before moving on to model building.

## Modelling
The simplest model for regression analysis is Linear Regression, and as a data scientist, I believe in using the most straightforward model that effectively meets our needs. If a simple model can provide accurate predictions, it should always be the first choice. With this in mind, we opted to proceed with Linear Regression for our analysis.

## Conclusion
Received a R2 score of 0.89

## Model Deployment
This is the rearmost stage of any artificial intelligence model.
We have designed a user-friendly interface. We used flask
software for making an HTML file for predicting or
estimating used second hand cars ,which takes the input for
each parameter and predicts the sale price for a used car.



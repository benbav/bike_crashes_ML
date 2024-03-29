# Chicago Bike Crashes Data Mining / Machine Learning Project

## Objective

The objective of this data science project is to identify the variables that contribute to the most dangerous bike crashes in Chicago. By analyzing a dataset of reported bike crashes, we aim to uncover insights and patterns that can help improve bike safety measures in the city.

![Feature Importances](images/feature_importances.png)

## Dataset

The dataset used for this project was obtained from the City of Chicago public database of traffic accidents, available at [https://data.cityofchicago.org/](https://data.cityofchicago.org/). The dataset consists of reported bike crashes that occurred in Chicago between 2016 and 2023.

- Size: ~10,000 records
- Format: CSV
- Source: [https://data.cityofchicago.org/resource/85ca-t3if.csv](https://data.cityofchicago.org/resource/85ca-t3if.csv)

## Data Preprocessing and Cleaning

Prior to analysis, the following preprocessing and cleaning steps were performed on the dataset:

- The target variable was created by combining bike crashes categorized as 'incapacitating' or 'fatal'.
- Missing categorical values were imputed using the most frequent value.
- Dates were split into separate columns for day, hour, and month.
- Missing numerical values were imputed using the K-nearest neighbors (KNN) algorithm.
- The numerical features were scaled to ensure comparability across different scales.

## Main Features

The main features or variables in the dataset include:

- Street name: The name of the street where the bike crash occurred.
- Latitude/Longitude: The geographic coordinates of the crash location.
- Weather condition: The prevailing weather condition at the time of the crash.
- Time information: The day, hour, and month of the crash.

These features are relevant to the project objective as they help identify the factors associated with dangerous bike crashes in Chicago.

## Exploratory Data Analysis (EDA)

Exploratory data analysis was conducted on the dataset, revealing the following insights and patterns:

- Time and day show a strong relationship with many of the crashes.

![Bike Crashes by Day and Hour](images/bike_crashes_day_hour.png)

- A geojson file was downloaded to map out the most frequent bike crash locations and fatalities on an overlaid map of Chicago.
- More deaths are concentrated on the west side of Chicago.

![Chicago Bike Crashes and Deaths](images/chicago_bike_crashes_and_deaths.png)

![Bike Crash Street](images/bike_crash_street.png)

## Machine Learning and Statistical Techniques

For analysis and prediction, a random forest model was trained using the dataset. The most important features from the model were then extracted to answer the leading question about the variables influencing dangerous bike crashes.

## Evaluation Metrics

The performance of the random forest model was assessed using the following evaluation metrics:

- F1 score: The model was optimized to achieve the best F1 score, which balances precision and recall.
- Learning curve: The learning curve was plotted to evaluate the model's training and validation performance.
- ROC curve: The ROC curve was used to assess the model's discriminatory power.

![ROC Curve](images/ROC.png)

## Data Split

The dataset was divided into training and testing sets using an 80/20 split ratio. Due to the heavy imbalance in the dataset (only 10% positive for the target variable), the random forest model incorporated balanced class weights. Additionally, the data split was stratified to include approximately equal amounts of the positive target variable in both the training and testing sets.

## Programming Language and Tools

This data science project was implemented using Python for ETL, Matplotlib and Searborn for data visualizations, and sklearn for the machine learning portion.

## Actionable Insights

### Time and Day Awareness:
- Increase awareness and safety measures during high-risk time periods and days, as the analysis revealed a strong relationship between these factors and bike crashes.
### Geographic Focus:
- Prioritize safety initiatives on the west side of Chicago, where a concentration of bike crash fatalities was observed.
### Street-specific Safety Measures:
- Implement targeted safety measures on streets identified as frequent crash locations to reduce the occurrence of dangerous bike crashes.
### Weather-based Interventions:
- Consider implementing weather-specific safety protocols, especially during adverse weather conditions, as weather was identified as a key variable affecting bike crash severity.
### Education and Outreach:
- Conduct educational campaigns to enhance awareness among cyclists and motorists about safe practices and potential dangers associated with specific streets or conditions.
### Law Enforcement Presence:
- Increase law enforcement presence or safety measures in areas identified as high-risk based on the analysis.
### Continuous Monitoring:
- Advocate for or invest in infrastructure improvements such as better signage, bike lanes, or traffic calming measures in areas prone to bike crashes.
### Targeted Training Programs:
Develop targeted training programs for both cyclists and motorists, focusing on identified risk factors and safe behaviors targeted towards the high risk young male group 


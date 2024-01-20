# App-Rating-Prediction-Python
Project Overview
# Goal
Develop a predictive model to assess and predict the app ratings on the Google Play Store based on the provided dataset ("googleplaystore.csv"). The aim is to enable the Google Play Store team to identify and promote apps that are likely to receive high ratings from users. By leveraging various features and attributes available in the dataset, the goal is to create a robust model that can accurately predict the potential success and user satisfaction of new apps. This predictive model will contribute to the new feature, boosting the visibility of promising apps in recommendations, search results, and other relevant sections, ultimately enhancing the overall user experience on the Google Play Store platform.

# Project Steps
**Data Loading and Cleaning**

**Load Data**: Utilize the pandas library to load the dataset.

**Check Null Values**: Identify and count null values in each column.

**Drop Null Records**: Remove records with null values.

# Data Type Correction and Formatting

**Size Column**: Convert sizes to numeric, considering Kb and Mb.

**Reviews Column**: Convert reviews from string to numeric.

**Installs Column**: Convert installs to numeric, removing commas and the plus sign.

**Price Column**: Remove the dollar sign and convert to numeric.

# Sanity Checks
Drop rows with ratings outside the range of 1 to 5.

Drop rows where reviews exceed installs.

For free apps, ensure the price is not greater than 0.

# Univariate Analysis
**Boxplot for Price**: Identify outliers.

**Boxplot for Reviews**: Check for apps with very high review numbers.

**Histogram for Rating**: Observe the distribution of ratings.

**Histogram for Size**: Examine the distribution of app sizes.

# Outlier Treatment
**Price**: Drop records with very high prices.

**Reviews**: Drop records with more than 2 million reviews.

**Installs**: Identify and drop records with very high install numbers based on percentiles.

# Bivariate Analysis
**Scatter Plot for Rating vs. Price**: Examine the relationship between rating and app price.

**Scatter Plot for Rating vs. Size**: Explore the correlation between rating and app size.

**Scatter Plot for Rating vs. Reviews**: Assess the relationship between rating and the number of reviews.

**Boxplot for Rating vs. Content Rating**: Investigate if content rating affects app ratings.

**Boxplot for Ratings vs. Category**: Identify genres with the best ratings.

# Data Pre-processing
**Log Transformation**: Apply log transformation to reduce skewness in Reviews and Installs.

**Drop Columns**: Remove irrelevant columns such as App, Last Updated, Current Ver, and Android Ver.

**Dummy Encoding**: Convert categorical columns (Category, Genres, Content Rating) into dummy variables.

# Train-Test Split
Split the dataset into training and testing sets using a 70-30 split.

# Model Building
**Linear Regression**: Build a linear regression model to predict app ratings.

**R2 Score**: Report the R2 score on the training set.

# Model Evaluation
**Predictions**: Make predictions on the test set.

**R2 Score**: Report the R2 score on the test set.

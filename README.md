# Bike-Sharing-Prediction-Modeling

**Author:** Elliot Ly

## Overview
This project uses the Bike Sharing Dataset from Washington D.C. (2011–2012) to predict daily bike rentals based on environmental and temporal factors. The analysis focuses on how weather, season, and other external factors impact the total number of bike rentals.

## Data & Source
- **Dataset:** Bike Sharing Dataset (daily rentals)  
- **Source:** UCI Machine Learning Repository  
  [Dataset Link](https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset)  
- **Citation:** Fanaee-T, H. (2013). Bike Sharing [Dataset]. https://doi.org/10.24432/C5W894

## Key Steps
1. **Exploratory Data Analysis (EDA):**
   - **Histogram:** Examined the distribution of daily bike rentals, revealing most days fall between 3,000 and 6,000 rentals with a few outliers.
   - **Scatterplot:** Explored the positive correlation between normalized temperature and bike rentals.
   - **Boxplots:** Compared rental counts by season and weather situation to uncover seasonal trends.
   - **Correlation Matrix:** Identified strong relationships between temperature variables and rentals, and slight negative effects from humidity and windspeed.

2. **Data Preparation:**
   - Verified that the daily bike data contained no missing values.
   - Split the data into training and testing sets, stratifying by the total rental count.
   - Created a preprocessing recipe that included dummy encoding for categorical predictors.

3. **Model Building & Evaluation:**
   - **Models Used:** Linear Regression, K-Nearest Neighbors (KNN), Random Forest, and Boosted Trees.
   - **Cross-Validation:** Applied 5-fold cross-validation to assess model performance.
   - **Results:**  
     - *KNN* achieved the lowest training RMSE (495) with an R² of 0.939.
     - On testing data, KNN’s RMSE increased to 729 and R² dropped to 0.862.
   - The performance suggests that while the KNN model captures much of the variance in the training data, it may be overfitting, indicating a potential need for a model that balances complexity and generalizability (e.g., GAM or QDA).

## Conclusion
The project demonstrates that environmental factors, especially temperature, significantly affect bike rental counts. Although the KNN model performed best on the training data, its decreased performance on testing data suggests that further model refinement is needed. Future work could involve exploring alternative models and refining preprocessing techniques to improve prediction accuracy.


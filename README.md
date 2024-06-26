# Seattle Weather Analysis and Classification

## Table of Contents
1. [Introduction](#introduction)
2. [Data Description](#data-description)
3. [Data Preprocessing](#data-preprocessing)
4. [Exploratory Data Analysis](#exploratory-data-analysis)
5. [Statistical Analysis](#statistical-analysis)
6. [Machine Learning Models](#machine-learning-models)
7. [Evaluation and Comparison](#evaluation-and-comparison)
8. [Prediction on New Data](#prediction-on-new-data)
9. [Resampling Techniques](#resampling-techniques)
10. [Conclusion](#conclusion)


## Introduction
This project analyzes Seattle weather data and builds machine learning models to classify weather types based on various weather parameters. The primary goal is to understand weather patterns and create predictive models that can classify weather conditions accurately.

## Data Description
The dataset used in this project is `seattleweather.csv`, which contains the following columns:
- `date`: The date of the weather observation.
- `precipitation`: The amount of precipitation.
- `temp_max`: The maximum temperature.
- `temp_min`: The minimum temperature.
- `wind`: The wind speed.
- `weather`: The type of weather (rain, sun, fog, drizzle, snow).

## Data Preprocessing
1. **Date Conversion:** Convert the `date` column to datetime format.
2. **Feature Extraction:** Extract day of the week, month, and year from the date.
3. **Season Extraction:** Define a function to get the season based on the month.
4. **Missing Values:** Check for and handle missing values.

## Exploratory Data Analysis
1. **Distribution Analysis:** Plot histograms of precipitation, max temperature, min temperature, and wind speed.
2. **Time Series Analysis:** Line plots of weather variables over time.
3. **Seasonal Analysis:** Average max temperature by month and distribution of max temperature by season.

## Statistical Analysis
Perform a T-test to compare the maximum temperatures between rainy and sunny days.

## Machine Learning Models
1. **Data Splitting:** Split data into training and testing sets.
2. **Resampling Techniques:** Apply SMOTE to handle class imbalance.
3. **Model Training:**
   - **XGBoost Classifier**
   - **Logistic Regression**
   - **K-Nearest Neighbors (KNN)**
   - **Balanced Bagging Classifier**
4. **Evaluation:** Use confusion matrix, classification report, and ROC curves to evaluate model performance.

## Evaluation and Comparison
Compare the performance of different models based on metrics such as accuracy, precision, recall, F1-score, and AUC scores.

## Prediction on New Data
Use the trained models to make predictions on new data points and calculate accuracy.

## Resampling Techniques
**Resampling Techniques:**
Imbalanced datasets, where one class is significantly more prevalent than others, pose a challenge for machine learning models. In our weather dataset, we might have unequal occurrences of different weather types, leading to biased model predictions. To address this issue, we employ resampling techniques, such as Synthetic Minority Over-sampling Technique (SMOTE).

**SMOTE (Synthetic Minority Over-sampling Technique)**
SMOTE works by creating synthetic samples of the minority class to balance the class distribution. This is crucial because machine learning algorithms tend to perform poorly when one class dominates the dataset, as they may become biased towards the majority class and ignore the minority class.

**Why Use SMOTE?**

Improved Model Performance: By balancing the class distribution, SMOTE ensures that the model is trained on a more representative dataset, leading to better performance and generalization.
Reduced Bias: SMOTE helps in reducing bias towards the majority class, ensuring that the model learns to distinguish between different classes effectively.
Preservation of Information: Synthetic samples generated by SMOTE are created by interpolating between existing samples, ensuring that the underlying information of the dataset is preserved.
By applying SMOTE to our dataset, we aim to enhance the robustness and accuracy of our machine learning models, particularly in scenarios where imbalanced classes are prevalent.

## Conclusion
This project provides a comprehensive analysis of Seattle weather data and builds effective machine learning models to classify weather conditions. The models can be used to predict weather types based on various input features, aiding in weather forecasting and related decision-making processes.

## Usage
To run this project:
1. Clone the repository.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Place the `seattleweather.csv` file in the project directory.
4. Run the Jupyter notebook or Python script containing the code.


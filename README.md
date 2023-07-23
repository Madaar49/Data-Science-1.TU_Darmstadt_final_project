# [Data Science 1 - Final Project]

## Project Title : Predicting the ambient electrical energy output (PE) of a Combined Cycle Power Plant (CCCP) by Machine Learning

## Introduction
This project aims at predicting the Energy Output (PE) of a Combined cycle power plant CCCP using Machine Learning.

## Data and Methods
- Data: The <a href="https://archive.ics.uci.edu/ml/datasets/combined+cycle+power+plant">Combined cycle power plant</a> dataset is one of the many ML datasets in the UC Irvine data repository. The dataset contains 9568 data points collected from a Combined Cycle Power Plant over 6 years (2006-2011), when the power plant was set to work with full load. Features consist of hourly average ambient variables Temperature (T), Ambient Pressure (AP), Relative Humidity (RH) and Exhaust Vacuum (V) to predict the net hourly electrical energy output (PE) of the plant.

- Methods
  - Exploratory Data Analysis 
  - Hypothesis Testing
  - Experimental models with one predictor 
  - Final Models using train_test_split ( MLR, MLR-polynomial, Ridge Regression, Lasso Regression)
  
## Results 
- Hypothesis Testing
  - Hypothesis testing was done to test the suitablity of 'RH' to be a relevant predictor of 'PE', since the correlation coeff of 0.39 shows that RH seems like a weak predictor variable. The results from the hypothesis testing showed that at a p-value of 0.0000 which is less than the significant level of 0.05 therefore RH is a good predictor of PE
- Experimental Models
  - Experimental models using MLR and MLR-Polynomial regressors showed no significant difference in `MAE`, `MSE` and `RMSE` values
- Final Models
  - The `MLR` models shows approximately same RMSE scores (~ 4) in training and test datasets 
  - The Ridge and Lasso Regressors were used to optimize and improve the model performance. There was little difference between them, with Ridge (RMSE of ~17.51 and MAE of ~4.18 ) and Lasso (RMSE of ~18.22 and MAE of ~4.26).
  - The best performing models in terms of `R2 score` are `Ridge Regression` with 93.6% accuracy, followed by `MLR` with 92.7% accuracy
  
  
## Conclusion
The models shows that Temperature (AT), Ambient Pressure (AP), Relative Humidity (RH) and Exhaust Vacuum (V) are good predictors for the net hourly electrical energy output (PE) of the plant. In short we can infer that there is a linear relationship between the above named predictors and the target. Despite the efficiency of the model, it is limited in predicting values within the time span of the data, therefore any data outside the time period is not certain to be predicted with the same accuracy.

## References
1. Pınar Tüfekci, Prediction of full load electrical power output of a base load operated combined cycle power plant using machine learning methods, International Journal of Electrical Power & Energy Systems, Volume 60, September 2014, Pages 126-140, ISSN 0142-0615

2. Heysem Kaya, Pınar Tüfekci , Sadık Fikret Gürgen: Local and Global Learning Methods for Predicting Power of a Combined Gas & Steam Turbine, Proceedings of the International Conference on Emerging Trends in Computer and Electronics Engineering ICETCEE 2012, pp. 13-18 (Mar. 2012, Dubai)

3. Dataset: <a href="https://archive.ics.uci.edu/ml/datasets/combined+cycle+power+plant">Combined cycle power plant Dataset</a>

4. OLS details: <a href="https://www.youtube.com/watch?v=6biU48ZAx3o">How to Run a Regression in Python
 </a>

5. Data Science 1 course: Fachbereich Elektrotechnik und Informationstechnik- TU Darmstadt

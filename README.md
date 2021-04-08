# ERCOT_Time_Series_Project
Time series analysis, modeling, and forecasting energy loads for ERCOT's South Central Weather Zone
 
 Analysis Code To Come!...Just need to find time to pretty it up a bit. I also plan on adding more to the readme
 but in the meantime, feel free to check out the full report and presentation slides if you're interested
 
 
# Abstract
Accurate prediction of electrical load requirement is crucial to maintaining integrity of
any electrical grid. Reliable energy prediction is especially important in the case of ERCOT or
the Electric Reliability Council of Texas since it operates on a competitive wholesale bulk-power
market or energy-only business model which requires frequent power dispatch scheduling based
on short term 1 hour, daily and mid-term weekly forecasts. To ensure proper operation, ERCOT
currently aims for a 12.5% power supply margin over maxim load utilizing complex hybrid
models to predict energy load which rely on expensive proprietary data services to achieve
necessary levels of accuracy. 

This work explores implementation of statistics-based time series
modelling and analysis techniques for predicting energy load for ERCOT’s South-Central
weather zone. 43,824 load and local air temperature measurements each starting on Jan. 1st, 2015
01:00 through Dec. 31st, 2019 24:00 serve as the training set for model fitting purposes and
model testing spans the first week or 168 data points of 2020. Time series models for load were
trained on linear residuals of standardized data in order to address heteroscedasticity and remove
non-stationarity whereas the temperature data model was fitted directly to raw values. Model
selection consisted of F-test criterion and minimum AIC for scalar and vectoral ARMA models,
respectively. Prediction error is defined in terms of Green’s Function coefficients and variance of
residuals by orthogonal Wold’s decomposition and application of the conditional expectation of
squared error. 

A scalar ARMA(36,35) model is found to be adequate for linear residuals of
standardized load data and had a RSS of 262.34. Similarly, ARMAV(35,35,34) was found to be
the most appropriate model for linear residuals of load data with air temperate as input and zero
lag and had an RSS of 263.28. In both cases, actual load values were within 6% of 1-hour ahead
load predictions meeting ERCOT’s 12.5% margin requirement while actual load did exceed this
margin for 24-hour ahead predictions. Likewise, actual load exceeded 12.5% of ARMA
generated 1-week ahead forecasts over the testing data time span. However, ARMAV generated
1-week ahead forecasts were found to be acceptable for capacity planning requirements. While
statistically inconclusive, this result does suggest ARMAV is better suited for predicting actual
load and more appropriate for use in real-world power dispatch scheduling. Overall, time series
modeling alone is able to accurately and reliably predict load values 1-hour ahead and even 1-
week ahead utilitzing vectoral ARMA modelling with local air temperature input.

# OM-of-offshore-wind-turbine
Title: A DE based approach for predictive maintenance optimization of an offshore wind turbine


# Abstract:

# Original data as inputs
SCADA 01 06.zp- include scada data of turbine T01 and T06
SCADA 07 011.zp- include scada data of turbine T07 and T011
failures.csv-failure logs of turbines
norelec.csv-electricity price
# Outputs from codes
Results of autoencoder-results of reconstruction error from autoencoder
Results.zip-
Sensiticity analysis- results of different population size and location parameters
OM based on predictions-results of solutions based on different conditions
figs-plot of system degradation, anomaly detection and rewards over generations

# Autoencoder
A three layer autoencoder is trained by the normal data from turbine 01. Then it is applied on other abnormal phases and turbines. Results of autoencoder reveals that it can detect anomalys without retraining. 


# Gaussian regression model 
GPR models are inserted in the environment class to give predictions. Three attitudes are set to select confidence intervals of predictions for decision making. 

# Interactive JADE (differential evolution algorithm) 

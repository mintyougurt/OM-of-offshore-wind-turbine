# OM-of-offshore-wind-turbine
Title:A differential evolution based approach for short-term predictive maintenance optimization of an offshore wind turbine
This is for my second publication on ocean engineering. Please cite this link and the paper https://doi.org/10.1016/j.oceaneng.2025.121507

# Abstract:
Offshore wind energy is growing rapidly but faces high maintenance costs. To implement predictive maintenance (PdM) in this field, this paper proposes a novel optimization approach for short-term PdM of a single offshore wind turbine (OWT). It combines an adaptive differential evolution algorithm with optional archive (JADE) and Gaussian process regression (GPR) models through a reinforcement learning (RL) framework. Temperatures from four OWTs are processed by an autoencoder to create a database. Using this database, a case study involving an OWT with five components is conducted. First, GPR models generate probabilistic remaining useful life (RUL) predictions for each component. An RL agent then simulates future degradation trajectories based on these predictions. JADE is applied across different scenarios to optimize maintenance by interacting with the virtual environment, considering external factors such as electricity and component prices, wind speeds, and maintenance duration. Results show that the maintenance plan based on pessimistic RUL forecasts exhibits the highest robustness across scenarios. This approach delivers highly precise and robust PdM schedules under prognostic uncertainty. It bridges a critical gap in integrating failure prognostics with maintenance optimization for OWTs.

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
Please see the structure of algorithms that have been presented in detail in the paper.

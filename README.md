# Predictive-Analysis-of-NASA-Turbofan-Degradation-simulationDataset
Goal of the project is to predict the remaining useful life (RUL) of turbofan jet engines using the NASA Turbofan Jet Engine Data Set.



# Introduction

This project aims to predict the remaining useful life (RUL) of turbofan jet engines using the NASA Turbofan Jet Engine Data Set from Kaggle. The dataset includes run-to-failure simulated data from turbofan jet engines. The engine degradation simulation was carried out using C-MAPSS, and four different sets were simulated under different combinations of operational conditions and fault modes.

The objective of this project is to predict the number of remaining operational cycles before failure in the test set. The data sets consist of multiple multivariate time series, each from a different engine, and each engine starts with different degrees of initial wear and manufacturing variation. The data is contaminated with sensor noise, and the engine develops a fault at some point during the time series.

# Data

The data is provided as a zip-compressed text file with 26 columns of numbers, separated by spaces. Each row is a snapshot of data taken during a single operational cycle, and each column is a different variable. The columns correspond to unit number, time in cycles, operational settings 1, 2, and 3, and 21 sensor measurements.

The data set is divided into four subsets: FD001, FD002, FD003, and FD004. Each subset consists of training and test data. Data Set: FD001
Train trjectories: 100
Test trajectories: 100
Conditions: ONE (Sea Level)
Fault Modes: ONE (HPC Degradation)

Data Set: FD002
Train trjectories: 260
Test trajectories: 259
Conditions: SIX
Fault Modes: ONE (HPC Degradation)

Data Set: FD003
Train trjectories: 100
Test trajectories: 100
Conditions: ONE (Sea Level)
Fault Modes: TWO (HPC Degradation, Fan Degradation)

Data Set: FD004
Train trjectories: 248
Test trajectories: 249
Conditions: SIX
Fault Modes: TWO (HPC Degradation, Fan Degradation)

source: https://data.nasa.gov/Aerospace/CMAPSS-Jet-Engine-Simulated-Data/ff5v-kuh6/about_data 
Provided By: PCoE


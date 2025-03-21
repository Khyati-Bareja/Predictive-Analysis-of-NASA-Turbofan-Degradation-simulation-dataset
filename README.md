# PredictiveMainenance-Analysis-of-NASA-Turbofan-Degradation-simulationDataset
Aim of the project is to predict the remaining useful life (RUL) of turbofan jet engines using the NASA Turbofan Jet Engine Data Set.

# Basics of Predictive Mainenance and Failure Analysis
Every device has a point of failure, a new device from the manufacturer is healthy but due to wear and tear on the device as it ages it health slowly deteriorates and eventually it fails. 

At this point we need to provide maintenance of the device to get it back to a healthy condition. 

There are 3 types of maintenance: 
Reactive: 
	Where we wait till it fails and then perform maintenance : Results in considerable financial losses 
Preventive/Scheduled: 
	 Here we try to perform the maintenance long before the device's point of failure, but this is not very cost effective, why? 
	 because by performing maintenance early we waste the device life which was still usable.
Predictive: 
	 This is where predictive maintenance helps.
	 Here we predict when the device would fail and schedule maintenance just before that. Following this process we minimize the device of machine's downtime and maximize its lifetime. 


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

# Approach
There are number of ways to approach this problem, 
- # First Principles Modeling technique:
  Requires a lot of Domain expertise, start with some kind of principle like newton's second law and from that we derive equations on how the system behaves and using those equations we can predict the state of the device i.e if its healthy or when will it degrade.
- # Data driven Modeling technique:
  Here we solely depend upon the data collected from the devices and use Machine learning techniques and statistical appraches to develop models based purely on this data to help us derive necessary predictions.
- # Hybrid Appraoches:
  This falls somewhere in middle where I might require some level of First priciple's understanding and use some data driven techniques to help me fill in the gap between the knowledge.
# Files
EDA-and-Modeling + Weibull Curve.ipynb: This Jupyter notebook contains the exploratory data analysis and modeling code for the project. It includes survival analysis methods and a generalized linear model with a binomial link function. It utilizes the methods in survial analysis like Partial Effects on Survival, WeibullAFTFitter and KaplanMeier curve.

LNM.R: This R script contains additional code for the project.

src/EDA-and-Modeling.ipynb: This notebook contains the application of Random Forest Regressor to predict the Remaining Useful Life (RUL) dependent variable.

LogisticRegression.ipynb: This Jupyter notebook contains additional code for the project, including a Hosmer-Lemeshow test, time-series feature generation, application of generalized linear model with binomial link function and confusion matrix.

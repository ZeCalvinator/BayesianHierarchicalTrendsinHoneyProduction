# Bayesian Hierarchical Trends in Honey Production



This project analyzes *state-level trends in honey production across the United States* using data from the USDA Honey Bee Survey. The objective is to examine how honey production per hive changes over time and evaluate potential environmental and biological factors that may influence these trends.

## Project Overview

Honey bees are essential for agricultural pollination and ecosystem stability. In recent years, bee populations have faced several stressors including pests, disease, pesticide exposure, and environmental changes. Understanding how these factors relate to honey production can provide insight into broader patterns in bee health and agricultural productivity.

This project applies *Bayesian hierarchical modeling* to examine variation in honey production across states and years while accounting for differences among states.

## Data

The primary dataset comes from the *USDA Honey Bee Survey*, which reports annual state-level estimates of honey production and colony health indicators.

Variables analyzed include:

* Honey production per hive (HpH)
* Year
* Varroa mite prevalence
* Pesticide exposure
* Disease prevalence
* Pest prevalence
* Average temperature
* Annual precipitation
* State identifiers

Each observation represents a *state–year combination*.

## Methods

The analysis was conducted in *R* using a Bayesian hierarchical modeling framework implemented in *JAGS*.

Key steps include:

1. Data cleaning and preprocessing  
2. Standardization of continuous predictors  
3. Construction of Bayesian regression models  
4. Parameter estimation using Markov Chain Monte Carlo (MCMC)  
5. Model comparison using Deviance Information Criterion (DIC)

Several model structures were explored, including:

* State-specific intercept models  
* State-specific slope models  
* Environmental predictor models  
* Interaction models  
* Fully hierarchical models  

These models allow honey production trends to vary across states while identifying potential drivers of variation.

## Results

Results indicate that honey production varies substantially among states and across years. Hierarchical models allow estimation of state-level baseline production and temporal trends, highlighting regional differences in honey productivity.

Posterior summaries of model parameters were used to evaluate differences among states and assess the influence of environmental and biological factors.

## Tools and Packages

This project was developed using:

* R
* tidyverse
* rjags
* jagsUI
* ggmcmc
* knitr

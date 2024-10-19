# Multivariate Negative Binomial Linldey uisng JAGS

This repository contains the implementation of a Multivariate Negative Binomial Lindley (MVNBL) model using JAGS for Bayesian inference. The model is used for analyzing crash frquency & severity data from Michigan intersections. The workflow involves data preparation, model specification, and estimation using Markov Chain Monte Carlo (MCMC) methods in JAGS.


## Requirements
This project requires the following packages to be installed in R:
`arcgisbinding`, `rlang`, `tidyverse`, `sp`, `rstan`, `MASS`, `R2jags`, `coda`, `readxl`, `ggplot2`, `jagsUI`, and many others.
Please refer to the code for the complete list of packages.


## Usage
**Data Preparation**: Load the Michigan Intersection Dataset (`data/Michigan Intersection Data.xlsx`) and prepare the response and explanatory variables.

**Model Definition**: The JAGS model is defined in `MVNBL_model.txt`, which includes the specification of the MVNBL model.

**Model Execution**: The model is run using the `jags()` function from the `R2jags` package, with parameters specified for MCMC.

**Output**: The model output is saved as an RDS file (`MVNBWLindley.rds`) for future reference and analysis.


To run the model, execute the R scripts in the following order:
1. Load required packages and set up the environment.
2. Prepare the dataset (Data) by loading and transforming the raw data.
3. Define and run the JAGS model.

## Model Description
The Multivariate Negative Binomial Lindley (MVNBL) model is used to model count data where overdispersion is present. This project employs a Bayesian hierarchical structure to model crash severity types jointly, using JAGS for inference. The model includes:

- **Likelihood**: Negative Binomial distribution for crash severity counts.
- **Priors**: Weakly informative priors for regression coefficients and dispersion parameters.
- **MCMC**: Used for parameter estimation, with burn-in and thinning to ensure convergence.

## Files
- **MVNBL_jags.Rmd**: Main R Markdown file that contains the entire code, from data preparation to model execution.
- **MVNBL_model.txt**: JAGS model file that defines the Bayesian model.
- **data/**: Folder containing the dataset (`Michigan Intersection Data.xlsx`).
- **paper/**: Folder containing a published paper that provides more details about the modeling process.

## Contact
If you have any questions or issues regarding the code, feel free to reach out: 
**Author**: [Ali Khodadadi]  
**Email**: [a.khodadadi1994@gmail.com]

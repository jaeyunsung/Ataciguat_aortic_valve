Ataciguat aortic valve 2023
===================================================
# Introduction
This repository contains the source code to reproduce the main data presented in "Reactivation of Oxidized Soluble Guanylate Cyclase as a Novel Treatment Strategy to Slow Progression of Calcific Aortic Valve Stenosis" by Bin Zhang *et al.

# Installation

The following R libraries must be pre-installed to run the scripts:

```
library(ggplot2)
```

The following Python libraries must be pre-installed to run the scripts:
```
pandas
h2o
scipy
numpy
```



# Description of data used in this study

The 'data' directory contains the following input files for the analysis pipelines of this project:

>delta_area_for_regression.csv

Study participants baseline variables (treatment, sex, measurements from blood tests and echocardiograms)

>train

This holds the 23 training sets for the neural network regression model. Each file has 22 sample to use to train the model.

>test

This holds the 23 tests sets for the neural network regression model. Each file has 1 sample to test.

# Description of scripts

The 'scripts' directory contains several jupyter lab Python and R scripts for running the analysis pipelines of this project. Each script calls local data from the 'data' directory. All results used to generate the main text's display items are automatically exported into the 'output' directory.

The scripts found in this repository are the following:




>Figure1B_PCA.R

This script takes the quantile normalized data and first runs an ANOVA test to find features (i.e., autoantibodies) that
have statistically significant variance across study groups. If the *P*-value is less than 0.05, then the feature 
is considered to be statistically significant. Only the significant features are used to project autoantibody profiles onto the
principal component analysis (PCA) ordination plot.



# Running the scripts

Example of how to run a script in the terminal command line:

> Rscript differentially_abundant.R

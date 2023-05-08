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

>neural_net_h2o.ipynb

This python scripts takes in the training data and trains the neural network regression model to predict changes in aortic valve area on the test sets.

>combine_all_predicted_values.ipynb

This python script reads in all the individual predicted changes in aortic valve area and combines them into one dataframe to use in the scatter plot.

>actual_vs_predicted_scatterplot.ipynb

This R script takes the actual changes in aortic valve area and the predicted changes in aortic valve area from the neural network regression model. This script makes a scatter plot of the actual changes in aortic valve area and the predicted changes in aortic valve area.




# Output

This directory contains the output from the neural network regression model for predicting changes in aortic valve area. The features of importance are found here from the neural network regression model as well as the scatter plot of actual changes in aortic valve area compared to predicted changes.

# Running the scripts

Jupyter lab notebooks are run similar to an R markdown file. Each cell contains a section of code to run. There are both Python and R notebooks included in the scripts directory.

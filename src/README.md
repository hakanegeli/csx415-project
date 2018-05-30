# R sripts and Markdowns

## Formal Problem Statemet (FPS)

This Rmarkup file, `01-FPS.Rmd`, formats and knits the Formal Problem Statemet (FPS) and places an html file under the reports folder. For more about the FPS, please refer to the **Reports** section.

## Collect and Shape Data

This Rmarkup file, `02-collect-and-shape.Rmd`, formats and knits the Collect and Shape Data process and places an html file under the reports folder. For more about the Collect and Shape Data, please refer to the **Reports** section.

## Exploratory Data Analysis (EDA)

This Rmarkup file, `03-EDA.Rmd`, contains code to examine correlations between the variables which make up the dataset. The code uses `ggplot2` to graphically illustrate these relationships and the markdown knits the Exploratory Data Analysis report and places an html file under the reports folder. For more about the EDA, please refer to the **Reports** section.

## Model Performance Evaluation

This  Rmarkup file, `model-performance-evaluation.Rmd`, builds the most basic and the simplest model, aka the Naive Model, for our problem. The markdown knits the Model Performance Evaluation report and places an html file under the reports folder. For more about the Model Performance Evaluation, please refer to the **Reports** section.

## Feature Selection

This Rmarkup file, `04-feature-selection.Rmd`, contains code to examine which independent vaiables were the most significant solving the problem. The code uses linear model function `lm` and non-linear model function `rpart` to find the most significant coefficients and evaluates the "fitness" of the model based on the selected independent variables. The markdown knits the Feature Selection report and places an html file under the reports folder. For more about the Feature Selection, please refer to the **Reports** section.

## Model Training and Validation

The Rmarkup file `05-training-and-validation.Rmd` takes the features that we have selected from the Feature Selection process and builds several Regression and also Classification models for comparison.

The program builds several classification models including:

* Decision Tree (**rpart** and **raprt2**),
* Linear Discriminant Analysis with Stepwise Feature Selection (**stepLDA**)**,
* Neural Networks Using Model Averaging (**avNNet**)** which uses different initialization paramters and averages out the results,
* Multinomial Log-linear Regression Model via Neural Networks (**multinom**),
* Random Forest (**rf**),
* Single-hidden-layer Neural Network (**nnet**)** with 20 nodes,
* Support Vector Machines with Linear Kernel (**svmLinear**)
* Support Vector Machines with Radial Basis Function Kernel (**svmRad**)
* Support Vector Machines with Polynomial Kernel (**svmPoly**)

** - We have commented these model out because of the time it takes to train them.

and performes a repeated K-fold cross-validation totaling 10 iterations (5 folds repeated twice) for each model. For each model Accuracy and Kappa values and the standard deviations for these performance metricies are also calculated and tabularized for comparison.

The program performs an analysis for the best two models and calculates a Confusion Metrix and ROC plots for each class for each of the top two models and selects the mest model for deployment.

The markdown knits the Model Training and Validation report and places an html file under the reports folder. For more about the Model Training and Validation, please refer to the **Reports** section.

The R script file `model-training-and-validation.R` performs the same functions as the Rmarkdown version but this version does not depend on ProjectTemplate. As long as the required libraries are installed or available, this file can be executed from the R console and the output will be displayed on the console as well. Please refer to the `deploy/README.md` file for instruction on how to run it.

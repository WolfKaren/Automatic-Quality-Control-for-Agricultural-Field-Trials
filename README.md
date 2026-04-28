# Automatic-Quality-Control-forAgricultural-Field-Trials-Paper-
Data from the simulation study described in the paper 'Automatic Quality Control for Agricultural Field Trials - Detection of Nonstationarity in Grid-indexed Data'.

## OVERVIEW
This repository contains data from the simulation study:
- TRIALS: Simulated and estimated residual patches of each step of the proposed algorithm.
- VISUALISED_TRIALS: Visualisation of the simulated and estimated patches of each step of the proposed algorithm.
- METADATA: Summary of metadata for each simulated trial and the estimation performance of each step of the proposed algorithm.

## ABOUT THE DATA

###  TRIALS

#### DATA STRUCTURE:
We provide the folder 'TRIALS' containing separate CSV files for each simualted dataset and its corresponding estimations
(i.e., Trial0.csv to Trial98.csv).

#### VARIABLES:
Each CSV file contains columns for general information on the data from the simulation study.
- General information is given in the first columns
(i.e., trial identifier name, row and column indentifiers).
- The simulated data is given in the columns starting with 'Simulated_*' and ending with a descriptive title
(e.g., 'Simulated_MarginalResiduals' corresponds to the simulated marginal residuals, 'Simulated_TwoPatchesVerified' corresponds to the two simulated patches, whose borders were verified).
- The estimation results are given in the columns starting with 'Estimated_*' and ending with a descriptive title
(e.g., 'Estimated_PatchesIdentified' corresponds to the estimated patches after identification).
- Missing values correspond to missing values in the simulated two-dimensional grid.

### METADATA

#### DATA STRUCTURE:
We provide a single CSV file that summarises the metadata for all simualted datasets and its corresponding estimations
(i.e., METADATA.csv).

#### VARIABLES:
The CSV file contains columns for general information about the data, the simulation, the estimations and corresponding performance, estimation time and number of iterations.
- General information is given in the first columns
(i.e., identifier name, number of rows and columns of the data).
- Information on the structure of missing values and their clusters is given in the columns starting with 'NA*' and ending with a descriptive title
(e.g., 'NAProportion' corresponds to the proportion of missing values relative to the field size, 'NAMaximumClusterSize' corresponds to the maximum cluster size of missing values).
- The metadata for simulations is given in the columns starting with 'Simulated_*' and ending with a descriptive title
(e.g., 'Simulated_GRFTypePatch0' corresponds to the simulated Gaussian Random Field type (e.g., AR1_c)).
- The metadata for estimations is given in the columnns starting with 'Estimated_*' and ending with a descriptive title
(e.g., 'Estimated_NumberOfPatchesIdentified' corresponds to the number of estimated patches after identification).
- The performance of the estimations (e.g., similarity to simulated residual patches) is given in the columns starting with 'Similarity_*' and ending with a descriptive title
(e.g., 'Similarity_SimulatedTwoPatchesVerified_vs_EstimatedPatchesIdentified' corresponds to the similarity of identified patches to simulated patches).
- The performance of the estimations under the assumption of optimal merging (e.g., oracle similarity to simulated residual patches) is given in the columns starting with 'OracleSimilarity_*' and ending with a descriptive title
(e.g., 'OracleSimilarity_SimulatedTwoPatchesVerified_vs_EstimatedPatchesIdentified' corresponds to the oracle similarity of identified patches to simulated patches).
- The estimation time and number of iterations are given in the columns starting with 'Estimated_Time*' and 'Estimated_Iterations*', each ending with a descriptive title
(e.g., 'Estimated_TimeGlobalAuthentication' and 'Estimated_TimeGlobalVerification' corresponds to the estimation time for global authentication and verification,
'Estimated_IterationsGlobal' corresponds to the number of iterations for global authentication and verification).

### VISUALISED_TRIALS

#### DATA STRUCTURE:
We provide a PDF file for all CSV files from TRIALS
(i.e., VISUALISED_TRIALS.pdf).

#### VARIABLES:
Each page file contains visualisations of the simulations and estimations of its corresponding CSV file from TRIALS.
- All columns of the CSV file starting with 'Simulated_*' or 'Estimated_*' are visualised.
- For all estimations (except those from tree indexation, i.e., columns '*Tree*'), the performance is printed below the visualisation.
(Performance corresponds to the similarity between the estimated and simulated residual patches
(i.e., 'Estimated_*' and 'Simulated_TwoPatchesVerified')).
Trials are ordered in ascending order of similarity of the proposed method (i.e., 'Similarity_SimulatedTwoPatchesVerified_vs_EstimatedPatchesFinalVerifiedAnecdotal').

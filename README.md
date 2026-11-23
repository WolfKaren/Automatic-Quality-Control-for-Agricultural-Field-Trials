README – Data

# OVERVIEW
This repository contains data from the simulation study (folder 'Simulation_Study') and the real data example (folder 'Real_Data_Example').
It can be used to reproduce the simulation study presented in the manuscript and to test other methods on the data.
The repository comprises the following files:
- METADATA: One file for the Simulation Study and one for the Real Data Example.
- SINGLE TRIAL DATA: One single file for each trial.
- VISUALISED TRIALS: One file containing visualisations of all simulated trials.

# ABOUT THE DATA

## METADATA
We provide a CSV file that summarises the metadata for all datasets and its corresponding estimations in tabular form
(i.e., METADATA.csv or METADATA_BYDV.csv).
The CSV file contains columns for general information about the data, the simulation*, the estimations, the corresponding performance*, the estimation time, and the number of iterations (columns which are flagged with '*' are only available for simulated trials; columns flagged with '**' are only available for the real data example).
- General information is given in the first columns
(i.e., trial identifier, GRF used for the analysis**, number of rows and columns of the data).
- Information on the structure of missing values and their clusters is given in the columns starting with 'NA' and ending with a descriptive title*
(e.g., 'NAProportion'* corresponds to the proportion of missing values relative to the field size).
- The metadata for simulations is given in the columns starting with 'Simulated_' and ending with a descriptive title*
(e.g., 'Simulated_GRFTypePatch0'* corresponds to the simulated Gaussian Random Field type (e.g., AR1_c)).
- The metadata for estimations is given in the columnns starting with 'Estimated_' and ending with a descriptive title
(e.g., 'Estimated_NumberOfPatchesIdentified' corresponds to the number of estimated patches after identification).
- The performance of the estimations (e.g., similarity to simulated residual patches) is given in the columns starting with 'Similarity_' and ending with a descriptive title*
(e.g., 'Similarity_SimulatedTwoPatchesVerified_vs_EstimatedPatchesIdentified'* corresponds to the similarity of identified patches to simulated patches).
- The performance of the estimations under the assumption of optimal merging (e.g., oracle similarity to simulated residual patches) is given in the columns starting with 'OracleSimilarity_' and ending with a descriptive title*
(e.g., 'OracleSimilarity_SimulatedTwoPatchesVerified_vs_EstimatedPatchesIdentified'* corresponds to the oracle similarity of identified patches to simulated patches).
- The estimation time and number of iterations are given in the columns starting with 'Estimated_Time' and 'Estimated_Iterations', each ending with a descriptive title
(e.g., 'Estimated_TimeVerification' corresponds to the estimation time for verification).

## SINGLE TRIAL DATA:
We provide separate CSV files for each trial dataset and its corresponding estimations in tabular form
(i.e., Trial0.csv, Trial1.csv, ... for the simulated data; TrialBYDV_IID.csv and TrialBYDV_AR1.csv for the real data example).
Each CSV file contains columns for general information on the data from the simulation study (columns which are flagged with '*' are only available for simulated trials; columns flagged with '**' are only available for the real data example).
- General information is given in the first columns
(i.e., trial identifier, variety identifier**, GRF used for the analysis**, row and column indentifiers, block identifier**).
- The simulated data is given in the columns starting with 'Simulated_' and ending with a descriptive title*
(e.g., 'Simulated_MarginalResiduals'* corresponds to the simulated marginal residuals).
- The real data is given in the columns 'Score'**, 'FittedScore'**,
'ConditionalResdiuals'**, and 'MarginalResiduals'**.
- The estimation results are given in the columns starting with 'Estimated_' and ending with a descriptive title
(e.g., 'Estimated_PatchesIdentified' corresponds to the estimated patches after identification).
- Missing values correspond to missing values in the simulated two-dimensional grid.

## VISUALISED_TRIALS
We provide a PDF file containing visualisations of all simulated Trials (i.e., Trial0.csv, Trial1.csv, …) (i.e., VISUALISED_TRIALS.pdf).
Each page contains visualisations of the simulations and estimations of one simulated trial.
- All columns of the CSV file starting with 'Simulated_' or 'Estimated_' are visualised.
- For all estimations (except those from tree indexation, i.e., columns containing 'Tree'), the performance is printed below the visualisation. Performance corresponds to the similarity between the estimated and simulated residual patches
(i.e., 'Estimated_' and 'Simulated_TwoPatchesVerified').
Trials are ordered in ascending order of similarity of the proposed method (i.e., 'Similarity_SimulatedTwoPatchesVerified_vs_
EstimatedPatchesFinalVerifiedAnecdotal').


# MIMIC-IV
This is a large dataset containing critical care data for over 40,000 patients admitted to intensive care units at the Beth Israel Deaconess Medical Center (BIDMC). For more information, see: https://physionet.org/content/mimiciv/0.4/

The access to this database is restricted and a certification can be obtained by completion of the CITI Data or Specimens Only Research. For more information, see: https://about.citiprogram.org/courses/?reset=true

For this reason, the MIMIC-IV data is stored in the directory `/data/mimiv-iv-0.4/` and included in the `.gitignore` to prevent distribution of sensitive data. To run the code in this directory, gaining access to the MIMIC-IV data and storing it in the mentioned directory is needed.

## Preprocessing
Ultimately, this selects and formats the dataset to prepare it for usage on machine learning algorithms. The output will be stored in the `/data/` directory, with one folder per preprocessing step and one csv file per ethnic group.

### Preprocessing_I: Filtering
This file selects the important data tables and columns and merges these accordingly. The output csv files are saved in `/data/preprocessing_I/`.

### Preprocessing_II: Labeling
This file finds the most occuring diagnose (= kidney related diagnoses) and adds a boolean column to the data called `has_kidney_issues`. The output csv files are saved in `/data/preprocessing_II/`.

### Preprocessing_III: Converting data types
This file converts the selected columns into workable formats (int64, datetime64\[ns\], bool) and replaces NaN values. The output csv files are saved in `/data/preprocessing_III/`.

### Preprocessing_IV: Splitting
This file splits the data into train, test and validation sets based on patients' admission time. The output csv files are saved in `/data/preprocessing_IV/`.

## Hyperparameter Tuning
This file trains random forest classifiers on a variety of different hyperparameters and saves the best performing hyperparameters for each ethnic group in the file `hyperparameters.csv`.

## Federated Forest
This file introduces a federated forest, where the data is horizontally federated. The federated forest aggregates the local random forest models such that each ethnic group is equally weighted. The accuracy, precision, recall and AUC (ROC) of the local models and the global model are calculated for performance comparison and stored in the file `metrics.csv`.

### Citations
Johnson, A., Bulgarelli, L., Pollard, T., Horng, S., Celi, L. A., & Mark, R. (2020). MIMIC-IV (version 0.4). PhysioNet. https://doi.org/10.13026/a3wn-hq05.
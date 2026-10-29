# SWYNEX Internship — Task 1: Data Preparation

## Objective
Prepare a public dataset for data-science work by inspecting its structure, cleaning missing values, handling data types, documenting assumptions, and exporting a cleaned dataset.

## Dataset
**Palmer Penguins** dataset, distributed as a public CSV by the `mwaskom/seaborn-data` repository.

- CSV source: https://raw.githubusercontent.com/mwaskom/seaborn-data/master/penguins.csv
- Dataset information: https://github.com/allisonhorst/palmerpenguins
- The dataset includes penguin species, island, bill measurements, flipper length, body mass, sex, and year.

## Repository structure
```text
swynex-task1-data-preparation/
├── data/
│   └── processed/          # cleaned CSV is generated here
├── notebooks/
│   └── task1_data_preparation.ipynb
├── src/
├── requirements.txt
└── README.md
```

## How to run
1. Install Python 3.10+.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Start Jupyter:
   ```bash
   jupyter notebook
   ```
4. Open `notebooks/task1_data_preparation.ipynb` and run all cells from top to bottom.
5. The notebook saves `data/processed/penguins_cleaned.csv`.

Run the notebook from its own directory if your environment does not resolve relative paths as expected; alternatively change `OUTPUT_DIR` to `Path("data/processed")` when running from the repository root.

## Cleaning steps
- Inspect shape, column names, types, missing values, duplicates, and summary statistics.
- Standardize column names and trim text whitespace.
- Convert expected numeric columns to numeric types.
- Remove exact duplicate rows.
- Fill missing numeric values with column medians.
- Fill missing categorical values with the most frequent category.
- Validate that no missing values or duplicate rows remain.
- Export the cleaned CSV.

## Assumptions
- Blank strings are treated as missing after whitespace trimming.
- Invalid numeric values are treated as missing and then imputed.
- Median imputation is used for numeric columns because it is less sensitive to outliers than the mean.
- Mode imputation is used for categorical columns; it can increase the frequency of the most common category.
- Exact duplicates are removed, but similar-looking records are not automatically considered duplicates.
- No outliers are removed without domain evidence that they are errors.
- Imputed values are estimates, not original measurements.

## Limitations
Imputation can hide uncertainty and may affect downstream analysis. For modelling, fit imputation rules on training data only to avoid data leakage. This task focuses on preparing data and does not train a model.

## License and attribution
The CSV is hosted in the `mwaskom/seaborn-data` public repository. Check the source repository and dataset documentation for current licensing and attribution details before redistribution.

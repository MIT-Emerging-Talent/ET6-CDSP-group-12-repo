# Data Preparation

This folder contains the cleaned and structured datasets
used in our analysis of global crypto adoption and
international migration trends. The data preparation
step involved importing raw Excel files, filtering relevant
columns and rows, standardizing formats, and combining
datasets across multiple years.

## Contents

### 1. Global Crypto Adoption Index (2022–2024)

- **Source:** [Chainalysis](https://www.chainalysis.com/blog/2024-global-crypto-adoption-index/)
- **Raw Data:** [`The_Global_crypto_Adoption_Index_2022_to_2024.xlsx`](../raw_datasets_files/The_Global_crypto_Adoption_Index_2022_to_2024.xlsx)
- **Processing Steps:**
  - Imported sheets for 2022, 2023, and 2024.
  - Selected relevant columns: `Rank`, `Country`, and `Region`.
  - Standardized region names by removing abbreviations (e.g., `(CSAO)`).
  - Merged all years into a single DataFrame called `GCAI_df`.

### 2. International Migrant Stock by Destination and Origin (2024)

- **Source:** [UN DESA Population Division](https://www.un.org/development/desa/pd/content/international-migrant-stock)
- **Raw Data:** [`undesa_pd_2024_ims_stock_by_sex_destination_and_origin.raw.xlsx`](../raw_datasets_files/undesa_pd_2024_ims_stock_by_sex_destination_and_origin.raw.xlsx)
- **Processing Steps:**
  - Imported `Table 2` sheet from the Excel file.
  - Extracted specific rows of interest: 13, 38–40, 44, 45, 47, 50–54, 58, 59.
  - Selected columns `B` (Country/Region) and `E` (2024 migrant stock).
  - Cleaned the result and renamed columns for clarity.

## Tools Used

- **pandas** for data handling and cleaning
- **nbqa** + **black** or **ruff** for notebook formatting and linting

## Output

- Cleaned and combined datasets are now ready for analysis and modeling.
- Can be exported as `.csv` or used directly within notebooks.

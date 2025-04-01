# Raw Data Sources Information

This document provides details about the raw data sources used in this project and the initial processing steps applied. The processed files are stored in the `02_data/02.01_raw/` directory.

## 1. CDC PLACES BRFSS Data

*   **Source:** CDC PLACES: Local Data for Better Health, County Data. Data originates from the Behavioral Risk Factor Surveillance System (BRFSS).
    *   2023 Release (Data Year 2021): `PLACES__Local_Data_for_Better_Health__County_Data_2023.csv`
    *   2024 Release (Data Year 2022): `PLACES__Local_Data_for_Better_Health__County_Data_2024.csv`
*   **Description:** Provides county-level, model-based estimates for various health measures.
*   **Geography:** US Counties.
*   **Years:** 2021, 2022.
*   **Processing Notebook:** `03_code/03.01_data_collection/PLACES_BRFSS_data.ipynb`
*   **Processing Steps:**
    *   Loaded raw CSV files.
    *   Filtered data for years 2021 and 2022.
    *   Selected relevant health measures (Diabetes, General Health, Smoking, Obesity, Checkups, Depression, Health Insurance Access, Mental Health) using `measureid`.
    *   Filtered for 'Age-adjusted prevalence' (`AgeAdjPrv`).
    *   Pivoted data to a wide format, with one row per county and year, and columns for each selected health measure.
    *   Renamed `locationid` to `fips` and formatted as a 5-digit string (zero-padded).
    *   Converted all column names to lowercase.
*   **Output Files:**
    *   `brfss_data_2021.csv`
    *   `brfss_data_2022.csv`

## 2. US Census ACS Data

*   **Source:** US Census Bureau, American Community Survey (ACS) 5-Year Estimates, Data Profiles (`acs/acs5/profile`). Accessed via the `censusdis` Python package.
*   **Description:** Provides demographic, social, economic, and housing characteristics.
*   **Geography:** US Counties.
*   **Years:** 2021, 2022.
*   **Processing Notebook:** `03_code/03.01_data_collection/ACS_data.ipynb`
*   **Processing Steps:**
    *   Downloaded data using the `censusdis` package for specified variables (population, education, age, race, ethnicity, sex, occupation, health insurance, poverty, vehicle availability, broadband access). See notebook `var_map` for specific variables codes and assigned names.
    *   Renamed variables to user-friendly names.
    *   Converted all column names to lowercase.
    *   Created a 5-digit FIPS code (`fips`) by combining state and county codes.
*   **Output Files:**
    *   `acs_data_2021.csv`
    *   `acs_data_2022.csv`

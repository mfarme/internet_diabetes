# Longitudinal Study of Diabetes Prevalence in U.S. Counties and its relationship with Household Internet Adoption
> *__Active Research__*  
> This research is currently in development. Frequent updates and changes are expected.


## Overview
This research project investigates the longitudinal relationship between broadband internet adoption rates and diabetes prevalence in U.S. counties. The study aims to understand how internet access, as a social determinant of health, influences diabetes outcomes while controlling for other relevant factors.
## Abstract

### Background
Access to the internet is increasingly recognized as a key social determinant of health, enabling populations to utilize virtual health services, access health information, and engage with social resources. However, the impact of household internet adoption on chronic disease outcomes, such as diabetes prevalence, remains poorly understood at the population level.

### Methods
We conducted a longitudinal, county-level analysis using data from the 2021 and 2022 American Community Survey (ACS) and the CDC’s Behavioral Risk Factor Surveillance System (BRFSS). Our analytic sample included 3,076 U.S. counties. We engineered features to capture both structural and intermediate social determinants of health, including a novel measure of structural internet adoption. The primary outcome was age-adjusted diabetes prevalence. We applied descriptive statistics, two-stage linear regression, and a test of machine learning models to predict changes in diabetes prevalence from 2021 to 2022. After training the models on 2021 data, model performance was evaluated on unseen 2022 data using R², mean squared error (MSE), mean absolute error (MAE), and root mean squared error (RMSE).

### Results
The best-performing machine learning model (XGBoost) explained 85% of the variance in county-level changes in diabetes prevalence (R² = 0.85, RMSE = 0.89). Feature importance analysis highlighted household internet adoption, alongside other social determinants, as a significant predictor of diabetes prevalence change. Notably, higher rates of internet adoption were associated with lower diabetes prevalence, even after adjusting for demographic, socioeconomic, and health behavior variables.

### Discussion
Our findings demonstrate that advanced machine learning approaches can robustly model and predict changes in diabetes prevalence at the county level, revealing the critical role of internet adoption as a social determinant of health. These results suggest that policies aimed at closing the digital divide may have meaningful impacts on population health outcomes, particularly for chronic diseases like diabetes. Future research should validate these findings at the individual level and further explore the mechanisms linking digital access to health behaviors and outcomes.

## Suggested Citation (BibTeX)
```bibtext
@article{Farmer2025InternetDiabetes,
  title={Diabetes and the Digital Divide: A Longitudinal Study of Diabetes Prevalence in U.S. Counties and its Relationship with Household Internet Adoption},
  author={Matthew S. Farmer and Qingyu Chen},
  year={2025},
  note={Available at: https://github.com/matthewfarmer/internet_diabetes},
}
```
## Project Structure
```
.
├── 01_docs/                    # Project documentation
│   ├── 01.01_manuscripts/     # Manuscript drafts and figures
│   ├── Project Overview.md    # Detailed project description
│   └── requirements.txt       # Python dependencies
├── 02_data/                   # Data files
│   ├── 02.01_raw/            # Raw data files
│   └── raw_data_info.md      # Data documentation
├── 03_code/                   # Analysis code
│   ├── 03.01_data_collection/# Data collection scripts
│   ├── 03.02_analysis/       # Analysis notebooks
│   └── 03.03_visualization/  # Visualization code
└── 04_collaboration/         # Collaboration documentation
```

## Setup Instructions

1. Create a Python virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

2. Install dependencies:
```bash
pip install -r 01_docs/requirements.txt
```

3. Set up environment variables:
Create a `.env` file in the root directory with:
```
CENSUS_API_KEY=your_key_here
```

4. Start Jupyter notebook:
```bash
jupyter notebook
```

## Data Sources
- American Community Survey (ACS) 5-year estimates (2021-2022)
- USDA Rural-Urban Commuting Area (RUCA) Codes
- CDC PLACES: Local Data for Better Health County Data 2023 and 2024 releases
  - Source: https://data.cdc.gov/500-Cities-Places/PLACES-Local-Data-for-Better-Health-County-Data-20/pqpp-u99h
  - Includes county-level health measures including diabetes prevalence
  - Data includes confidence intervals and population denominators
  - Contains multiple health indicators and measures across different categories

## Methodology
- First-differences regression analysis to examine longitudinal relationships
- Control for structural determinants of health (poverty, education, demographics, etc.)
- 2 Stage Linear Regression for controlling endogeneity in Broadband adoption 
- Machine learning models for supplementary analysis

## Key Variables
- **Dependent Variable**: Change in self-reported diabetes prevalence
- **Primary Independent Variable**: Change in broadband internet adoption rate
- **Control Variables**: Changes in poverty levels, education, demographics, income, and geographic location
- **Intermediary Variables**: Changes in healthcare access, health behaviors, and social support measures

## Analysis Environment
- Python-based analysis using:
  - pandas & numpy for data manipulation
  - statsmodels for statistical analysis
  - scikit-learn for machine learning
  - matplotlib, seaborn, and plotly for visualization
  - geopandas for geographic data analysis
- Jupyter notebooks for reproducible analysis
- Version control through Git

## Research Team
- Matthew S. Farmer, PhD RN (Primary Investigator)
- Qingyu Chen, PhD (Mentor)

## License
This project is licensed under the terms of the LICENSE file in the root directory.

## Contributing
Please see `04_collaboration/colab_documentation.md` for contribution guidelines.

## Citation
For detailed references and citations, please see the full project documentation in `01_docs/Project Overview.md`.

## FAIR Principles Implementation
This repository follows FAIR (Findable, Accessible, Interoperable, Reusable) principles:

- **Findable**: DOI: [pending], Published publicly online
- **Accessible**: Available via HTTPS through GitHub
- **Interoperable**: Uses standard file formats and documented APIs
- **Reusable**: Open-source licensed with complete documentation
---
## Acknowledgements
The research reported here was supported by University of Missouri, AIM-AHEAD Coordinating Center, award number OTA-21-017, and was, in part, funded by the National Institutes of Health Agreement No. 1OT2OD032581. The views and conclusions contained in this document are those of the authors and should not be interpreted as representing the official policies, either expressed or implied, of the NIH.

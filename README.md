# Internet Access and Diabetes Prevalence Study

## Overview
This research project investigates the longitudinal relationship between broadband internet adoption rates and diabetes prevalence in U.S. counties. The study aims to understand how internet access, as a social determinant of health, influences diabetes outcomes while controlling for other relevant factors.

## Key Research Questions
1. How do changes in county-level broadband internet adoption rates relate to changes in diabetes prevalence over time?
2. What intermediary factors (healthcare access, health behaviors, social support) mediate this relationship?

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
- Mediation analysis for intermediary factors
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

## Research Questions / Specific Aims
**Specific Aim 1:** To examine the longitudinal association between changes in county-level broadband internet adoption rates and changes in county-level self-reported diabetes prevalence over a two-year period, while controlling for other relevant social determinants of health.

Hypothesis 1:  Counties that experience an increase in broadband internet adoption rates between Year 1 and Year 2 will exhibit a corresponding decrease in self-reported diabetes prevalence between Year 1 and Year 2, after adjusting for changes in other SDOH.

**Specific Aim 2**: To identify the key intermediary factors (e.g., healthcare access, health behaviors, social support) that mediate the relationship between changes in internet adoption and changes in diabetes prevalence.

Hypothesis 2: The relationship between changes in internet adoption and changes in diabetes prevalence will be partially mediated by changes in intermediary factors such as access to healthcare services (e.g., having a usual source of care), health behaviors (e.g., physical activity, diet), and social support.

## Abstract

## Citation (BibTeX)

## Acknowledgements

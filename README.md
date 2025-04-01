# Internet Access and Diabetes Prevalence Study

## Overview
This research project investigates the longitudinal relationship between broadband internet adoption rates and diabetes prevalence in U.S. counties. The study aims to understand how internet access, as a social determinant of health, influences diabetes outcomes while controlling for other relevant factors.

## Key Research Questions
1. How do changes in county-level broadband internet adoption rates relate to changes in diabetes prevalence over time?
2. What intermediary factors (healthcare access, health behaviors, social support) mediate this relationship?

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

## Project Structure
```
.
├── 01_docs/               # Project documentation
├── 02_data/              # Data files
├── 03_analysis/          # Analysis scripts and notebooks
└── 04_output/            # Generated outputs and results
```

## Analysis Environment
- Private GitHub repository for version control and collaboration
- Python-based analysis using pandas, NumPy, statsmodels, and scikit-learn
- Jupyter notebooks for reproducible analysis

## Impact
This research aims to:
- Inform policies and interventions for increasing internet access
- Advance understanding of social determinants of health
- Guide future research on digital health equity
- Support evidence-based decision making for healthcare infrastructure

## References
For detailed references and citations, please see the full project documentation in `01_docs/Project Overview.md`.

## FAIR Principles Implementation
This repository follows FAIR (Findable, Accessible, Interoperable, Reusable) principles:

- **Findable**: DOI: [insert DOI], Published publically online
- **Accessible**: Available via HTTPS through GitHub
- **Interoperable**: Uses standard file formats and documented APIs
- **Reusable**: Open-source licensed with complete documentation

## Research Questions / Specific Aims
**Specific Aim 1:** To examine the longitudinal association between changes in county-level broadband internet adoption rates and changes in county-level self-reported diabetes prevalence over a two-year period, while controlling for other relevant social determinants of health.

Hypothesis 1:  Counties that experience an increase in broadband internet adoption rates between Year 1 and Year 2 will exhibit a corresponding decrease in self-reported diabetes prevalence between Year 1 and Year 2, after adjusting for changes in other SDOH.

**Specific Aim 2**: To identify the key intermediary factors (e.g., healthcare access, health behaviors, social support) that mediate the relationship between changes in internet adoption and changes in diabetes prevalence.

Hypothesis 2: The relationship between changes in internet adoption and changes in diabetes prevalence will be partially mediated by changes in intermediary factors such as access to healthcare services (e.g., having a usual source of care), health behaviors (e.g., physical activity, diet), and social support.

## Research Team

Matthew S. Farmer, PhD RN (Primary Investigator)
Qingyu Chen, PhD (Mentor)

## Abstract

## Citation (BibTeX)

## License

## Acknowledgements

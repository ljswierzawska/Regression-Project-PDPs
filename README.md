The Vanishing Market: The Vanishing Market: Who Gets Left Behind as Medicare Drug Plans Disappears
  
Luiza Swierzawska, Columbia Journalism School, Spring 2026

Project Overview

This project analyzes the contraction of the Medicare Prescription Drug Plan (PDP) market following the Inflation Reduction Act (IRA) of 2022, and examines which populations are most affected by shrinking plan availability.  

Data Sources

┌─────────────────────────────────┬───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┬──────┐
│             Dataset             │                                                        Source                                                         │ Year │
├─────────────────────────────────┼───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┼──────┤
│ CMS Landscape Source File (PDP) │ Centers for Medicare & Medicaid Services (https://www.cms.gov/medicare/coverage/prescription-drug-coverage)           │ 2022 │
├─────────────────────────────────┼───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┼──────┤
│ CMS Landscape Source File       │ Centers for Medicare & Medicaid Services (https://www.cms.gov/medicare/coverage/prescription-drug-coverage)           │ 2026 │
├─────────────────────────────────┼───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┼──────┤
│ Medicare Monthly Enrollment     │ Centers for Medicare & Medicaid Services (https://data.cms.gov/resources/medicare-monthly-enrollment-data-dictionary) │ 2026 │
├─────────────────────────────────┼───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┼──────┤
│ Rural-Urban Continuum Codes     │ USDA Economic Research Service (https://www.ers.usda.gov/data-products/rural-urban-continuum-codes/documentation)     │ 2023 │
└─────────────────────────────────┴───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┴──────┘
  
Data files are not included in this repository due to their large size. All CMS datasets are publicly available at cms.gov (https://www.cms.gov) and the USDA dataset is available at ers.usda.gov (https://www.ers.usda.gov).

Methodology

Four linear regression models were run in R via the rpy2 interface in Python:
  - Model 1 — Does premium change predict the change in PDP availability per state?
  - Model 2 — Does the share of Low-Income Subsidy (LIS) beneficiaries predict county-level PDP enrollment share?
  - Model 3 — Does rural-urban classification predict county-level PDP enrollment share?
  - Model 4 — Combined model: rurality + LIS share as predictors of PDP enrollment share

Requirements: Python 3, R
ibraries: pandas, rpy2, tidyverse


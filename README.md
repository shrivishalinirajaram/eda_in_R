# Ebola Outbreak Simulation – Exploratory Data Analysis in R

## Project Overview

This project performs a detailed exploratory data analysis (EDA) on a simulated 2014–2015 Ebola virus outbreak dataset. It aims to understand how temporal clinical events, symptom profiles, patient demographics, and viral load metrics relate to clinical outcomes (recovery vs. death) during an Ebola outbreak.

---

## Research Question

**Does the timing of clinical milestones (onset, hospitalization, outcome), symptom presentation, viral load, and patient demographics influence the clinical outcome of Ebola virus disease during the outbreak?**

---

## Rationale

Ebola virus disease (EVD) exhibits diverse clinical progression and has a high fatality rate. In this project, we:

- Join multiple datasets to reconstruct patient-level records.
- Clean and derive variables such as symptom counts and date intervals.
- Explore outcome trends across age, gender, and time.
- Visualize viral load categories (via PCR Ct values), clinical timelines, and symptom patterns.

This analysis supports better understanding of disease progression and mortality trends.

---

## Repository Structure

```
ebola_eda_project/
├── codes/                   # Quarto documents
│   ├── data_processing.qmd      <- Main EDA and data wrangling workflow
│   └── presentation.qmd         <- Slide deck for results and summary
├── data/                   # Input data files
│   ├── ebola_cases.csv
│   ├── ebola_combined.csv
│   ├── ebola_hospitals.csv
│   └── ebola_patients.csv
├── outputs/                # Rendered HTML files
│   ├── data_processing.html
│   └── presentation.html
├── scss/
│   └── custom.scss         # Custom SCSS styling for the presentation
├── eda_in_R.Rproj          # RStudio project file
├── LICENSE
└── README.md
```


---

## Methods & Tools

- **Core R Packages**:
  - `tidyverse`
  - `lubridate`
  - `ggplot2`
  - `stringr`
  - `gt`
  - `quarto`

- **Processing Highlights**:
  - Merged multiple tables (patients, cases, hospitals) using identifiers
  - Parsed complex symptom strings into binary indicators
  - Created new variables like day intervals between clinical milestones
  - Cleaned and validated categorical demographic fields

- **Visualization**:
  - Univariate and bivariate EDA across gender, age, outcome, viral load
  - Timeline plots, heatmaps of symptom frequency, outcome faceting
  - Styled `gt` tables for clean clinical summaries

---

## Outputs

- `outputs/data_processing.html`: Full EDA notebook with inline plots, code, and commentary
- `outputs/presentation.html`: Quarto Reveal.js slides summarizing key insights and interpretation

---

## Skills Demonstrated

- Data cleaning and preprocessing of real-world–like clinical simulation datasets
- Advanced tidyverse-based EDA workflows
- Narrative construction using Quarto for both technical and public-facing communication
- Integration of exploratory plots and tables for simulation-based public health interpretation

---

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/shrivishalinirajaram/eda_in_R.git
   ```
2. Open the RStudio project: eda_in_R.Rproj
3. In your `R Console`
   ```bash
   install.packages(c("tidyverse", "gt", "lubridate", "stringr", "quarto"))
   ```
4. Render the documents:
   Run and knit `codes/data_processing.qmd`
   Run and knit `codes/presentation.qmd`

---

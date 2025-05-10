# MRSA Dual Therapy Duration Analysis

This project analyzes the relationship between dual therapy duration and patient outcomes in MRSA (Methicillin-resistant Staphylococcus aureus) infections.

## Authors
- John
- Yiran

## Overview

This analysis investigates whether the duration of dual therapy affects patient outcomes in MRSA infections. The study examines multiple outcomes including mortality, readmission, recurrence, and adverse effects.

## Research Question

Does the duration of dual therapy (≤10 days vs. >10 days) have a significant relationship with patient outcomes in MRSA infections?

## Data

The analysis uses MRSA patient data with the following key variables:
- `dual_therapy_duration`: Duration of dual therapy in days
- `patient_death`: Binary indicator of patient mortality
- `patient_readmission`: Binary indicator of patient readmission
- `patient_recurrence`: Binary indicator of infection recurrence
- `adverse_effect`: Binary indicator of adverse effects
- `composite_failure`: Combined outcome (death OR readmission)

## Methodology

The analysis employs:
- **Logistic Regression**: To examine continuous relationships between therapy duration and outcomes
- **Fisher's Exact Test**: To compare binary outcomes between therapy duration groups
- **Data Visualization**: Bar charts and scatter plots to visualize relationships

## Key Findings

### Patient Mortality
- Fisher's exact test p-value: 0.6776 (not significant)
- Logistic regression p-value: 0.2735 (not significant)
- Odds ratio: 0.55 (95% CI: 0.07 - 3.84)

### Patient Readmission
- Fisher's exact test p-value: 1.0 (not significant)
- Logistic regression p-value: 0.4532 (not significant)
- Odds ratio: 0.76 (95% CI: 0.09 - 5.83)

### Patient Recurrence
- Only one case observed; statistical analysis not possible

### Adverse Effects
- Fisher's exact test p-value: 0.09778 (marginally significant)
- Logistic regression p-value: 0.168 (not significant)
- Note: All adverse effects occurred in the ≤10 days group

### Composite Clinical Failure
- Fisher's exact test p-value: 0.7036 (not significant)
- Logistic regression p-value: 0.292 (not significant)
- Odds ratio: 0.64 (95% CI: 0.10 - 3.67)

## Conclusions

The analysis found **no significant evidence** that longer dual therapy duration (>10 days) leads to:
- Increased mortality
- Increased readmission rates
- Increased recurrence rates

However, the study limitations include:
- Small sample size
- Limited power to detect differences
- All adverse effects occurred in the shorter therapy duration group

## Repository Structure

```
.
├── README.md
├── mrsa_bacteria_project.Rmd                  # Complete R Markdown analysis file
├── mrsa_cleaned.csv         # Cleaned dataset (not included in repo)
├── mrsa_project.pdf         # Generated report
└── figures/                 # Output visualizations
    ├── mortality_bar.png
    ├── mortality_scatter.png
    ├── readmission_bar.png
    ├── readmission_scatter.png
    ├── recurrence_bar.png
    ├── recurrence_scatter.png
    ├── adverse_effects_bar.png
    ├── adverse_effects_scatter.png
    ├── composite_failure_bar.png
    └── composite_failure_scatter.png
```

## Requirements

- R (≥ 4.0.0)
- R packages:
  - `tidyverse`
  - `ggplot2`
  - `knitr`
  - `rmarkdown`

## Usage

1. Clone the repository:
```bash
git clone https://github.com/[username]/mrsa-therapy-analysis.git
```

2. Install required packages:
```r
install.packages(c("tidyverse", "ggplot2", "knitr", "rmarkdown"))
```

3. Place your cleaned MRSA dataset as `mrsa_cleaned.csv` in the project directory

4. Run the analysis:
```r
rmarkdown::render("josh.Rmd")
```

## Data Privacy

The dataset is not included in this repository to protect patient privacy. Researchers with access to the data can run the analysis using their own copy of the dataset.

## Citation

If you use this analysis in your research, please cite:

```
[Authors]. (2024). MRSA Dual Therapy Duration Analysis. GitHub repository. 
https://github.com/[username]/mrsa-therapy-analysis
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

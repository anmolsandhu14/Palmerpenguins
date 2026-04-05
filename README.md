# Palmer Penguins Mini Project

## Author

Anmol Sandhu

### Project Overview

This project investigates whether the relationship between flipper length and body mass differs across penguin species using the Palmer Penguins dataset.

### Research Question

Does the relationship between flipper length and body mass differ among Adelie, Chinstrap, and Gentoo penguins?

### Hypothesis

The relationship between flipper length and body mass differs among species, such that the slope of body mass on flipper length varies across Adelie, Chinstrap, and Gentoo penguins.

### Dataset

Source: palmerpenguins R package\

Original data collected by Dr. Kristen Gorman and the Palmer Station, Antarctica LTER.

Raw dataset: 344 rows x 8 columns (contains missing values)\

Processed dataset: 342 rows x 3 columns (no missing values)

### Directory Structure

-   `data/data_raw/`\
    Contains original dataset and raw data dictionary

-   `data/data_processed/`\
    Contains cleaned dataset and processed data dictionary

-   `docs/`\
    Contains manuscript, pre-registration, data management plan, and supporting files (`.bib`, `.csl`)

-   `scripts/`\
    Contains data processing and analysis scripts

-   `renv/`\
    Contains package management files for reproducibility

### Data Processing

Processing steps:

-   Selected variables: species, flipper_length_mm, and body_mass_g\
-   Removed observations with missing values in these variables\
-   Final processed dataset contains 342 observations and 3 variables

### Reproducibility

To reproduce the analysis:

1.  Open the RStudio project file (`Palmer_penguins.Rproj`)\
2.  Restore the project environment by running:

``` r
renv::restore()
```

3.  Open the manuscript file: `docs/draft_manuscript.Rmd`

4.  Knit the document to generate all results (figures and tables)

All outputs are generated directly from the processed dataset.

# Palmer Penguins Mini Project

## Author

Anmol Sandhu

## Research Question

Does the relationship between flipper length and body mass differ across penguin species?

## Hypothesis

The slope of body mass on flipper length differs among Adelie, Chinstrap, and Gentoo penguins.

## Dataset

Source: palmerpenguins R package\
Original data collected by Dr. Kristen Gorman and the Palmer Station, Antarctica LTER.

Raw dataset: 344 rows x 8 columns (contains missing values)\
Processed dataset: 342 rows x 3 columns (no missing values)

## Directory Structure

-   data/data_raw\
    Contains the original exported dataset and raw data dictionary.

-   data/data_processed\
    Contains cleaned dataset used for analysis and processed data dictionary.

-   docs\
    Contains the draft manuscript written in R Markdown.

-   Palmer_penguins.Rproj\
    RStudio project file for reproducibility.

## Data Processing

Processing steps: - Selected species, flipper_length_mm, and body_mass_g. - Removed rows with missing values in these variables.

## Reproducibility

To reproduce the analysis:

1.  Open the RStudio Project file.
2.  Load required libraries.
3.  Run the R Markdown file located in the docs directory.
4.  All results are generated from the processed dataset.

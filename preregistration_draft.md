# Draft Pre-registration

## Research Question
Does the relationship between flipper length and body mass differ across penguin species?

## Hypothesis
The relationship between flipper length and body mass differs among Adelie, Chinstrap, and Gentoo penguins. Penguins with longer flippers are expected to have greater body mass, but the strength of this relationship may vary among species.

## Data Source
Data are obtained from the publicly available Palmer Penguins dataset provided through the palmerpenguins R package.

## Variables
Response variable:
body_mass_g (body mass in grams)

Predictor variable:
flipper_length_mm (flipper length in millimeters)

Grouping variable:
species (Adelie, Chinstrap, Gentoo)

## Data Processing
The processed dataset will be created by:
- selecting the variables species, flipper_length_mm, and body_mass_g
- removing observations with missing values for these variables

## Analysis Plan
To evaluate whether the relationship between flipper length and body mass differs among species, a linear regression model will be fitted:

body_mass_g ~ flipper_length_mm * species

This model includes an interaction between flipper length and species. A significant interaction term will indicate that the slope relating flipper length to body mass differs across species.

A scatterplot of flipper length versus body mass colored by species will also be produced to visualize the relationship between variables.
# Draft Pre-registration

## Research Question
Does the relationship between flipper length and body mass differ across penguin species?

## Hypothesis
The relationship between flipper length and body mass differs among Adelie, Chinstrap, and Gentoo penguins.

## Variables
Predictor variable: flipper_length_mm  
Response variable: body_mass_g  
Grouping variable: species

## Data Source
Data were obtained from the palmerpenguins R package.

## Analysis Plan
A linear regression model will be used to test the interaction between flipper length and species:

body_mass_g ~ flipper_length_mm * species

A significant interaction term will indicate that the relationship between flipper length and body mass differs among species.
# Modelling IgA Antibody Levels in Celiac Disease
 
Statistical modelling project for the course *Applied Linear Models*. Using a clinical dataset on celiac disease, it models **IgA antibody levels** with linear regression in **R**, following the full applied workflow: exploration, model selection, diagnostics, prediction and simulation.
 
## Dataset
 
Clinical, demographic and immunological data from Wageningen University & Research on individuals evaluated for celiac disease. After data cleaning and selection of clinically relevant variables, the dataset includes:
 
- **Demographics:** age, gender.
- **Clinical conditions:** diabetes, diarrhoea type, abdominal pain, short stature classification.
- **Immunological markers:** IgA, IgG and IgM antibody levels.
- **Disease indicators:** Marsh classification (histological grading of intestinal damage) and disease diagnosis.
The response variable is **IgA**, log-transformed to correct its skewness.
 
## Objective
 
Study how IgA levels are associated with demographic variables, clinical conditions, immunological markers and disease severity, and build a linear regression model to predict them.
 
## Approach
 
### 1. Exploratory data analysis
- Distributions of IgA and log(IgA).
- Correlation analysis of the continuous variables.
- Boxplots for all categorical predictors.
### 2. Model selection
- Best subset selection with `regsubsets()`.
- Models compared with AIC, BIC, adjusted R², Mallows' Cp and 10-fold cross-validation to choose the number of predictors.
### 3. Model fitting
- Ordinary least squares regression of log(IgA) on age, gender, diabetes, short stature, IgM and Marsh classification.
### 4. Collinearity analysis
- Variance Inflation Factors (VIF and GVIF), accounting for categorical predictors with several levels.
### 5. Diagnostics
- Residuals vs fitted values, histograms and Q–Q plots of residuals, Shapiro–Wilk test.
- Leverage, standardized residuals and Cook's distance to identify and assess outliers and influential points.
### 6. Model comparison
- ANOVA on nested models, to test whether dropping predictors causes a significant loss of information.
### 7. Prediction
- Predictions and confidence intervals for new observations.
### 8. Simulation
- Simulated IgA values from the fitted model, using the estimated coefficients and residual variance, compared with the observed values.
## Repository contents
 
- R Markdown scripts for the analysis.
- The cleaned dataset.
- The final report (PDF) with all visualizations and results.
## Tech stack
 
R, R Markdown

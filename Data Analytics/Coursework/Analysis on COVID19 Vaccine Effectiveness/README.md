# courseProjects
# README

This repository contains code and analysis for the research questions related to COVID-19 vaccine effectiveness in developed and developing countries.

## Research Questions

The research questions addressed in this analysis are as follows:

1. What are the factors associated with COVID-19 vaccine effectiveness, such as vaccination coverage, vaccination rollout strategies, healthcare infrastructure, COVID-19 related factors, population demographics, and socioeconomic indicators, across different countries?
2. Based on the identified factors from Research question 1, can we predict the development status of a country (i.e. developed or developing)?
3. Is there a difference in COVID-19 vaccine effectiveness between developed and developing countries using the dataset derived from research question 2?

## Data

The primary data used for the analysis is sourced from the [Our World in Data COVID-19 dataset](https://github.com/owid/covid-19-data). The dataset provides information on COVID-19 cases, vaccination coverage, healthcare infrastructure, and socioeconomic indicators for different countries.

## Code Structure

The code in this repository is organized as follows:

- `Rq1-Factors-COVID-Vaccine-Effectiveness.Rmd`: This R Markdown file addresses Research Question 1 and focuses on identifying the factors associated with COVID-19 vaccine effectiveness. It includes data preprocessing, exploratory data analysis, correlation analysis, and regression analysis.

- `Rq2-Predict-Development-Status.Rmd`: This R Markdown file addresses Research Question 2 and aims to predict the development status (developed or developing) of a country based on the factors identified in Research Question 1. It includes data preprocessing, feature engineering, random forest classification, and model evaluation.

- `Rq3-Comparison-Developed-Developing.Rmd`: This R Markdown file addresses Research Question 3 and investigates the difference in COVID-19 vaccine effectiveness between developed and developing countries. It includes data preprocessing, statistical analysis using t-tests, and data visualization.

## Results

The analysis provides insights into the factors associated with COVID-19 vaccine effectiveness, predicts the development status of countries based on these factors, and compares the vaccine effectiveness between developed and developing countries. The results are detailed in each of the respective R Markdown files.

## Dependencies

The following R packages are required to run the code:

- `data.table`
- `dplyr`
- `ggplot2`
- `gridExtra`
- `corrplot`
- `randomForest`

These packages can be installed using the `install.packages()` function in R.

```R
install.packages(c("data.table", "dplyr", "ggplot2", "gridExtra", "corrplot", "randomForest"))
```

## Conclusion

The analysis sheds light on the factors associated with COVID-19 vaccine effectiveness, provides a model for predicting the development status of countries, and compares the vaccine effectiveness between developed and developing countries. These findings can contribute to a better understanding of the effectiveness of COVID-19 vaccines and help inform future vaccination strategies and policies.

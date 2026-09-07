# Data and R

R supports reproducible policy analysis by making data management, visualization, and statistical analysis transparent.

## 1. Start with the policy question

The analytical sequence is:

1. define the policy question
2. identify the unit of analysis
3. identify the outcome and explanatory variables
4. document the data source
5. clean and inspect the data
6. summarize and visualize
7. select an appropriate model or statistical test
8. interpret the result in policy language
9. save code, data documentation, and outputs reproducibly

## 2. Working with policy data

A sound workflow should document where the data came from, how variables are defined, how missing values are handled, and what transformations are made before analysis.

## 3. Visualization before modeling

Plots can help identify trends, outliers, structural breaks, and differences that should be understood before regression or other statistical modeling.

## 4. Energy-policy data strategy

The long-term goal is to build a small set of reusable comparative datasets rather than starting from zero for every paper or class.

Potential sources include:

- national energy regulators and ministries
- World Bank indicators
- International Energy Agency datasets where access permits
- Eurostat and European Commission data
- electricity-system operators
- climate and emissions datasets
- public investment and infrastructure data

For the Kenya–Portugal research program, useful variables may include renewable generation share, installed capacity, electricity access, prices, outage indicators, investment, emissions, grid capacity, storage, and selected governance or institutional indicators.

## 5. Data documentation

Every dataset should include a codebook describing:

- variable name
- definition
- unit
- source
- year or period
- geographic unit
- transformations
- missing-data decisions

## 6. Code standard

R code will be added only after it has been run successfully against a documented dataset and checked for reproducibility. Placeholder functions, model formulas, and untested examples are intentionally excluded.

## 7. Why this belongs in the portfolio

The R component is not separate from the substantive expertise. Building, cleaning, documenting, and analyzing energy-policy data is part of becoming a stronger energy-policy analyst. The repository should therefore accumulate validated scripts and datasets that support both teaching and dissertation research.
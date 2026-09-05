# Data and R

R supports reproducible policy analysis by making data management, visualization, and statistical analysis transparent.

## Basic workflow
```r
getwd()
list.files()
load("DataAnalysisPAData.rdata")
ls()
names(crime)
summary(crime)
```

## Policy workflow
1. Define the question.
2. Identify the unit of analysis.
3. Document the data source.
4. Clean and inspect the data.
5. Summarize and visualize before modeling.
6. Save code and outputs reproducibly.
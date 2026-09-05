# Regression Analysis

Regression estimates relationships between an outcome and one or more explanatory variables.

## Bivariate model
```r
model1 <- lm(outcome ~ predictor, data=data)
summary(model1)
```

## Multivariate model
```r
model2 <- lm(outcome ~ policy + income + demand, data=data)
summary(model2)
```

## Interpretation
Focus on coefficient magnitude, uncertainty, model fit, controls, and whether the design supports association, prediction, or causal claims.
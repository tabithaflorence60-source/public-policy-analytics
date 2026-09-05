# Regression Analysis

Regression estimates relationships between an outcome and one or more explanatory variables. In policy analysis, the method is useful only when the model is tied to a clear substantive question and interpreted with appropriate caution.

## 1. Bivariate regression

```r
model1 <- lm(outcome ~ predictor, data=data)
summary(model1)
```

The slope estimates the expected change in the outcome associated with a one-unit change in the predictor.

## 2. Multivariate regression

```r
model2 <- lm(outcome ~ policy + income + demand, data=data)
summary(model2)
```

Adding controls can help account for observed competing explanations, but it does not automatically create a causal design.

## 3. Interactions

Policy effects may differ across countries, income groups, technologies, or institutional settings.

```r
model3 <- lm(outcome ~ policy * country + investment + demand, data=data)
summary(model3)
```

Interaction terms are especially useful in comparative policy analysis because they allow the relationship between a policy variable and an outcome to vary across contexts.

## 4. Interpretation

A strong interpretation addresses:

- coefficient direction
- substantive magnitude
- confidence intervals and p-values
- model fit
- omitted-variable concerns
- whether the model supports association, prediction, or causal inference

## 5. Energy-policy applications

Potential questions include:

- Is renewable-energy investment associated with higher renewable generation shares?
- Are stronger governance indicators associated with lower outage frequency?
- Do policy incentives have different effects across institutional settings?
- How are electricity access and affordability associated with infrastructure investment?
- Does the relationship between renewable deployment and grid stability change as storage or transmission capacity increases?

## 6. Comparative example

A simple Kenya–Portugal panel might use country-year observations and variables such as renewable share, investment, electricity demand, prices, outages, and policy indicators.

```r
model <- lm(
  renewable_share ~ investment + demand + policy_index + country,
  data = energy
)
summary(model)
```

The statistical output should then be interpreted alongside institutional evidence on regulation, grid planning, public investment, and implementation.

## 7. Diagnostics

Regression assumptions should be checked before drawing policy conclusions.

```r
par(mfrow=c(2,2))
plot(model)
```

Important concerns include heteroscedasticity, influential observations, multicollinearity, autocorrelation, and model specification.

## 8. Research connection

Regression is one of the core tools for turning the energy-policy portfolio into an empirical research program. The aim is not to run increasingly complicated models, but to formulate better policy questions, build stronger datasets, and connect statistical patterns to governance mechanisms.
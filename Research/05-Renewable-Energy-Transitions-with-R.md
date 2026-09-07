# Analyzing Renewable-Energy Transitions with R

## A Kenya–Portugal Policy Application

### Research question

How can reproducible quantitative analysis strengthen comparative research on renewable-energy transitions without reducing governance to a set of numbers?

### Purpose

This project develops a practical analytical workflow that combines R-based data analysis with comparative policy and institutional research. The objective is to use quantitative evidence to identify patterns, test relationships, and sharpen policy questions, while qualitative and governance analysis explains how and why those patterns emerge.

### Comparative focus

**Kenya** — geothermal development, electricity access, investment, utility performance, renewable deployment, and institutional coordination.

**Portugal / EU** — renewable integration, island systems, EU climate policy, investment, regulation, and multilevel governance.

### Potential indicators

- renewable share of electricity generation
- installed renewable capacity by technology
- investment flows
- electricity prices and affordability
- grid reliability
- access indicators
- emissions intensity
- public and private financing
- policy and regulatory indicators
- macroeconomic controls

### Reproducible workflow

1. Define the policy question and unit of analysis.
2. Build a documented dataset from authoritative public sources.
3. Clean and transform data in R.
4. Produce descriptive trends and comparative visualizations.
5. Estimate simple and multivariate models where appropriate.
6. Conduct sensitivity and robustness checks.
7. Interpret quantitative results in institutional context.
8. Document limitations and competing explanations.
9. Publish scripts, metadata, and figures for replication.

### Example R structure

```r
# Import data
energy <- read.csv("Data/energy_transition_panel.csv")

# Inspect
summary(energy)

# Compare renewable outcomes
aggregate(renewable_share ~ country, data = energy, FUN = mean)

# Model relationship between investment, governance and outcomes
model <- lm(
  renewable_share ~ investment + governance_index + electricity_demand,
  data = energy
)

summary(model)
```

### Interpretation principle

A statistically significant relationship does not by itself establish a governance mechanism or causal effect. The quantitative analysis is used together with policy documents, institutional mapping, interviews, and case evidence.

### Research extensions

- panel-data models
- interrupted time-series analysis around policy reforms
- event-study designs where data permit
- investment-risk analysis
- scenario and sensitivity analysis
- comparative visualization of technology pathways

### Teaching value

The project can also serve as a graduate teaching module showing students how to move from a sustainability-policy question to a reproducible analytical workflow and then back to a defensible policy interpretation.

### Next development

The next version will create the first clean Kenya–Portugal dataset, an R script, a data dictionary, and two reproducible figures.
# Equity and Distribution

Policy analysis should examine not only average outcomes but also who receives benefits, who bears costs, and who participates in decision-making.

## Concepts
- distributional impacts
- access and affordability
- participation
- environmental justice
- procedural justice

```r
tab <- table(data$group, data$outcome)
prop.table(tab, 1)
chisq.test(tab)
```
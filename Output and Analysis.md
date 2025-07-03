## Machine Learning: Random Forest

### Analysis of churn risk level by age group(Boxplot)

![Churn Risk by Age Group](plots/churn_risk_level.png)

| Age Group |   Median Risk   |   IQR (Q1–Q3)   |     Whiskers & Outliers      |
|:---------:|:---------------:|:---------------:|:----------------------------:|
|   <25     |    Very high    |  Tight, high    | Few very low-risk outliers   |
|  25–40    | Mid (~0.45)     |  Very wide      | Spans almost the full [0–1]  |
|  40–55    | Lower (~0.35)   |  Moderate       | No extreme outliers          |
|  55–70    | Lower (~0.30)   | Moderate-wide   | A few at both extremes       |
|   70+     | Mid (~0.45)     |  Wide           | Some very high churners      |

**Insights**:

1. Under-25s are the most at-risk cohort. Almost everyone here is high‐risk—prioritize retention campaigns.
2. 25–40 and 70+ show the biggest churn‐risk spread, where it needs a further segment, combined with data from other departments. 
3. Middle‐aged groups (40–55, 55–70) are more predictable.

**Strategies**:
- For `<25`: cooperating with marketing data, we need further to analyze the marketing campaigns and design rentention campaigns.  
- For `25–40` & `70+`: design A/B test messaging, marketing drafts two headline/offer variants per cohort, analytics sets up cohort splits, monitors open/click/conversion lift.
- For `40–55` & `55–70`:they are relatively loyal users, review weekly health metrics 
- Re‐evaluate after retraining to see if patterns persist.


# HealthConnect-Week6-Data-analytics
HealthConnect Advanced Analytics &amp; Decision Support | AnalystLab Africa Experience Lab. This repository contains the advanced analysis, validated findings, refined KPIs, updated visualisations, evidence-based insights, business recommendations, and cross-track integration work developed during Week 6.
Week 6 — Integration, Advanced Development & Validation

Week 6 advanced the HealthConnect project beyond the Week 5 descriptive analysis. The focus was on statistical validation, deeper analytical investigation, feature prioritisation, dashboard improvement, and cross-track integration with Data Science.

What Changed Since Week 5

- Moved from descriptive group-by comparisons to statistically validated relationships using chi-square tests of independence, effect sizes (Cramer's V), and 95% confidence intervals using the Wilson method.
- Discovered a compounding interaction effect: patients with 3+ prior no-shows combined with a booking lead time of over 30 days show a disproportionately high no-show rate.
- Developed an objective feature-ranking approach using standardised logistic regression with statsmodels p-values to support feature prioritisation.
- Formally revised a Week 5 conclusion: "distance_to_clinic_km", which appeared weak in the Week 5 simple comparison, was statistically significant after controlling for other variables.
- Confirmed that "waiting_time_minutes" remains statistically insignificant.
- Rebuilt the dashboard around three new validated views: effect-size comparison, interaction heatmap, and feature ranking.

Cross-Track Integration

Track: Data Science

Two validated feature-ranking files were exported for the Data Science track:

- ""HealthConnect_Week6_Feature_Validation_for_DataScience.csv"" (cross_track_exports/HealthConnect_Week6_Feature_Validation_for_DataScience.csv)
- ""HealthConnect_Week6_Numeric_Feature_Ranking_for_DataScience.csv"" (cross_track_exports/HealthConnect_Week6_Numeric_Feature_Ranking_for_DataScience.csv)

These outputs provide the Data Science track with a statistically justified feature-priority list based on significance tests and effect sizes, rather than an unranked candidate list.

Integration Impact

The Data Science track can use the validated feature priorities to support Week 6 feature-refinement and modelling decisions using statistical evidence rather than relying solely on Week 5 visual inspection.

Key Findings

Finding| Evidence
Booking lead time remains the strongest driver| Cramer's V = 0.184; Chi-square test, p < 0.001
Previous no-show history remains the second-strongest driver| Cramer's V = 0.091; Chi-square test, p < 0.001
3+ prior no-shows + 30+ day lead time represents a compounded high-risk segment| Week 6 interaction analysis
"distance_to_clinic_km" is significant in the multivariate model| Logistic regression, p < 0.05
"waiting_time_minutes" remains not significant| Logistic regression, p > 0.05

Week 6 Files

Notebook

- ""HealthConnect_DataAnalytics_Week6_Advanced_Analysis.ipynb"" (notebooks/HealthConnect_DataAnalytics_Week6_Advanced_Analysis.ipynb)

Dashboard & Visualisations

- ""HealthConnect_Week6_Dashboard.png"" (dashboards/HealthConnect_Week6_Dashboard.png)
- ""HealthConnect_Week6_Interaction_Heatmap.png"" (dashboards/HealthConnect_Week6_Interaction_Heatmap.png)

Cross-Track Outputs

- ""HealthConnect_Week6_Feature_Validation_for_DataScience.csv"" (cross_track_exports/HealthConnect_Week6_Feature_Validation_for_DataScience.csv)
- ""HealthConnect_Week6_Numeric_Feature_Ranking_for_DataScience.csv"" (cross_track_exports/HealthConnect_Week6_Numeric_Feature_Ranking_for_DataScience.csv)

Project Documentation

- ""HealthConnect_Week6_Project_Summary.docx"" (reports/HealthConnect_Week6_Project_Summary.docx)

Key Analytical Contribution

Week 6 strengthened the HealthConnect analysis by moving from descriptive findings to statistically validated decision support. The analysis identified relationships that remained significant after validation, uncovered an interaction effect not visible in the separate Week 5 breakdowns, and provided the Data Science track with a statistically supported feature-priority list.


1. Design a controlled A/B test for the proposed mid-point reminder intervention.
2. Reconcile the Week 6 feature ranking with the Data Science track's finalised model.
3. Revisit the interaction analysis with additional data to strengthen confidence in the smallest sample cells.

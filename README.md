# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Business Context

A subscription-based digital product company launched a new onboarding and activation campaign to improve user conversion and engagement. Users were randomly assigned to either a Control group (existing onboarding experience) or a Treatment group (new onboarding experience).

The objective of this project was to evaluate whether the new onboarding campaign should be launched to all users.

---

## Dataset Description

The dataset contains user-level experiment data including:

* User information
* Experiment group assignment
* Region
* Device type
* Traffic source
* Plan type
* Landing page visits
* Trial starts
* Onboarding completion
* Paid conversion
* Revenue generated
* Support tickets
* Refund requests
* Engagement scores

Total Records: 1,408

Experiment Groups:

* Control: 693 users
* Treatment: 715 users

---

## North Star Metric Selected

**Paid Conversion Rate**

Formula:

Paid Conversion Rate = Converted Users ÷ Total Users

This metric was selected because it directly measures the percentage of users who become paying customers and aligns closely with the company's revenue objectives.

---

## KPI Tree Summary

The KPI Tree was designed around Paid Conversion Rate as the North Star Metric.

Primary KPI Drivers:

* Trial Start Rate
* Onboarding Completion Rate
* User Engagement
* Revenue Outcomes

Guardrail Metrics:

* Refund Rate
* Support Ticket Rate

The KPI Tree is included in:

* outputs/kpi_tree.png

---

## Experiment Analysis Approach

The analysis followed the following process:

1. Data quality validation
2. Missing value review
3. Duplicate user analysis
4. Binary field validation
5. Revenue validation
6. Experiment summary creation
7. Segment-level analysis
8. Hypothesis testing
9. Guardrail metric evaluation
10. Final recommendation development

---

## Data Quality Summary

Key findings:

* Dataset contains 1,408 records.
* Control and Treatment groups are reasonably balanced.
* 8 duplicate user IDs (16 duplicate rows) were identified.
* Missing values were found in device_type, traffic_source, and engagement_score.
* Binary fields were validated successfully.
* No negative revenue values were identified.

Overall, the dataset was suitable for analysis with minor data quality considerations documented.

---

## Experiment Results Summary

| Metric                     | Control | Treatment |
| -------------------------- | ------- | --------- |
| Paid Conversion Rate       | 3.17%   | 6.99%     |
| Landing Page Visit Rate    | 63.64%  | 72.59%    |
| Trial Start Rate           | 25.11%  | 29.09%    |
| Onboarding Completion Rate | 15.58%  | 21.26%    |
| Refund Rate                | 0.00%   | 0.42%     |
| Support Ticket Rate        | 21.93%  | 37.20%    |
| Average Engagement Score   | 57.03   | 62.93     |
| Average Days To Convert    | 8.86    | 6.40      |

The Treatment group outperformed the Control group across most primary business metrics.

---

## Hypothesis Testing Summary

A Two-Proportion Z-Test was conducted using Paid Conversion Rate as the primary metric.

Results:

* Z Statistic = -3.2519
* P Value = 0.000573
* Significance Level = 0.05

Since the p-value was below the significance threshold, the Null Hypothesis was rejected.

The analysis provides statistically significant evidence that the Treatment onboarding experience improves Paid Conversion Rate.

---

## Guardrail Metrics Considered

The following guardrail metrics were evaluated:

* Refund Rate
* Support Ticket Rate
* Average Days To Convert
* Engagement Score

While Refund Rate and Support Ticket Rate increased, the Treatment experience delivered meaningful improvements in conversion and engagement.

---

## Final Recommendation

**Launch the Treatment onboarding experience to all users.**

The recommendation is supported by:

* Significant improvement in Paid Conversion Rate
* Higher onboarding completion rates
* Faster conversion speed
* Stronger user engagement
* Positive segment-level performance

Support Ticket Rate should continue to be monitored following launch.

---

## Assumptions and Limitations

* Analysis is based on the provided experiment dataset.
* Duplicate users and minor missing values were documented but not removed from business analysis.
* Results reflect the observed experiment period only.
* Longer-term customer behavior may differ from short-term experiment outcomes.

---

## Screenshots Included

* screenshots/summary_metrics.png
* screenshots/hypothesis_test_output.png
* screenshots/kpi_tree_preview.png



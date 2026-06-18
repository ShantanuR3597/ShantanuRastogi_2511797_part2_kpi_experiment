# Hypothesis Test Notes

## Metric Being Tested

The primary metric selected for hypothesis testing is **Paid Conversion Rate**, defined as the percentage of users who convert into paying customers.

Formula:

Paid Conversion Rate = Converted Users / Total Users

This metric was selected because it directly aligns with the business objective of increasing revenue-generating customers and was chosen as the North Star Metric for the experiment.

---

## Null Hypothesis (H0)

There is no statistically significant difference in Paid Conversion Rate between the Control group and the Treatment group.

Control Conversion Rate = Treatment Conversion Rate

---

## Alternative Hypothesis (H1)

The Treatment group has a higher Paid Conversion Rate than the Control group.

Treatment Conversion Rate > Control Conversion Rate

---

## Test Type

One-tailed hypothesis test.

A one-tailed test is appropriate because the business objective is specifically to determine whether the new onboarding experience improves Paid Conversion Rate.

---

## Significance Level

Alpha (α) = 0.05

A significance level of 5% is used, which is the standard threshold for business experiments.

---

## Decision Rule

If the p-value is less than 0.05:

- Reject the Null Hypothesis
- Conclude that the Treatment group significantly improves Paid Conversion Rate

If the p-value is greater than or equal to 0.05:

- Fail to reject the Null Hypothesis
- Conclude that there is insufficient evidence that the Treatment group improves Paid Conversion Rate

---

## Business Interpretation

The purpose of this test is to determine whether the observed improvement in Paid Conversion Rate is likely due to the new onboarding campaign rather than random variation.

The results of this hypothesis test will be used as a key input when deciding whether the Treatment experience should be launched to all users.




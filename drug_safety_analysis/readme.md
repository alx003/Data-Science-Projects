# Drug Safety Analysis

## Overview

This project analyzes clinical trial safety data to evaluate whether a treatment drug is associated with significantly different adverse reactions compared to a placebo. The analysis focuses on adverse effects, their frequency, and demographic comparability between treatment groups using standard statistical hypothesis testing methods.

The dataset (`drug_safety.csv`) was obtained from **Hbiostat**, courtesy of the Vanderbilt University Department of Biostatistics.

---

## Research Questions

The project aims to answer the following questions:

1. **Do the proportions of adverse effects differ significantly between the Drug and Placebo groups?**
2. **Is the number of adverse effects independent of treatment assignment?**
3. **Are the Drug and Placebo groups comparable in age distribution?**

---

## Dataset Description

* **Source:** Hbiostat (Vanderbilt University Department of Biostatistics)
* **Observations:** Clinical trial participants
* **Treatment ratio:** Drug : Placebo = 2 : 1
* **Key variables used:**

  * `trx`: Treatment group (`Drug` or `Placebo`)
  * `adverse_effects`: Whether a participant experienced any adverse effect (`Yes` / `No`)
  * `num_effects`: Number of adverse effects experienced
  * `age`: Participant age

The dataset also includes demographic data, vital signs, and lab measurements.

---

## Methods

The following statistical methods were used:

### 1. Two-Sample Proportion Z-Test

* **Purpose:** Compare the proportion of participants experiencing adverse effects between Drug and Placebo groups.
* **Null hypothesis:** The proportions of adverse effects are equal between groups.
* **Alternative hypothesis:** The proportions of adverse effects differ between groups.

### 2. Chi-Square Test of Independence

* **Purpose:** Determine whether the number of adverse effects is independent of treatment assignment.
* **Null hypothesis:** Number of adverse effects and treatment group are independent.
* **Alternative hypothesis:** There is an association between number of adverse effects and treatment group.

### 3. Mann–Whitney U Test

* **Purpose:** Compare age distributions between Drug and Placebo groups.
* **Reason:** Age was found to be non-normally distributed (Shapiro–Wilk test).
* **Null hypothesis:** Age distributions are the same between groups.
* **Alternative hypothesis:** Age distributions differ between groups.

---

## Key Results

* **Adverse effect proportions:** No statistically significant difference between Drug and Placebo groups (p = 0.964).
* **Number of adverse effects:** No significant association with treatment group (p = 0.615).
* **Age comparison:** No significant difference in age distribution between groups (p = 0.257).

Overall, the Drug and Placebo groups appear comparable, and the treatment was not associated with a statistically significant increase in adverse reactions.

---

## Technologies Used

* **Python**
* **pandas** – data manipulation
* **seaborn / matplotlib** – data visualization
* **statsmodels** – proportion z-test
* **pingouin** – statistical hypothesis testing

---

## Conclusion

This project demonstrates the application of statistical hypothesis testing in a real-world clinical trial context. The analysis provides evidence that the drug does not significantly increase adverse reactions compared to a placebo and that the treatment and control groups are demographically comparable.

---

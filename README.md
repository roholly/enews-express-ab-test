# E-news Express: Landing Page A/B Test

**Domain:** Digital Media · Experimental Design · Business Statistics  
**Tools:** Python, SciPy, statsmodels  

---

## The Setup

E-news Express, an online news portal, was losing ground on new subscriber acquisition. The hypothesis was that the existing landing page wasn't compelling enough to convert visitors. A redesigned page with a new layout and more relevant content was built and tested against the original.

100 users were randomly split into two equal groups. The control group saw the old page. The treatment group saw the new one. Four questions were put to the data.

---

## The Questions

**1. Do users spend more time on the new page?**

Visually, yes. The median time on the new page was nearly two minutes higher. But a two-sample t-test told a different story. The p-value came back at 0.9999, nowhere near the 5% significance threshold. There is no statistical evidence that users spend more time on the new page.

**2. Does the new page convert more users?**

The control group converted at 42%. The treatment group converted at 66%. A two-proportions z-test returned a p-value of 0.016, well below the threshold. The new page converts significantly better.

**3. Does preferred language affect conversion?**

The sample was roughly split across English, Spanish, and French users. A chi-square test of independence returned a p-value of 0.985. Language has no statistically significant relationship with whether a user converts.

**4. Does preferred language affect time spent on the new page?**

English users averaged 6.7 minutes, French 6.2, Spanish 5.8. One-way ANOVA, after confirming normality (Shapiro-Wilk) and equal variances (Levene's test), returned a p-value of 0.432. No statistically significant difference in time spent across language groups.

---

## The Interesting Part

The new page converts 57% more users than the old one, but there is no evidence users spend more time on it. That combination is worth paying attention to. It suggests the new design may be more efficient at driving a decision rather than simply more engaging. Users are converting without necessarily lingering longer, which is a meaningfully different outcome than the original hypothesis assumed.

---

## Recommendations

Proceed with the new landing page. To push conversion further, the analysis suggests investigating what specific content and formats drive subscription decisions, including article length, news category, writing style, and time of day. Demographic data on converting users would also help sharpen the content strategy.

On the journalism side: exclusive content, reputable bylines, and a clear editorial identity tend to distinguish news subscriptions worth paying for from the ones that don't survive.

---

## What This Demonstrates

- Hypothesis formulation and appropriate test selection for each question type
- Two-sample t-test, two-proportions z-test, chi-square test of independence, and one-way ANOVA applied in sequence
- Assumption testing before drawing conclusions (normality, variance equality)
- Interpreting results that don't confirm the original hypothesis, and finding what the data actually says

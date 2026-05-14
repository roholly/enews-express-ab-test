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

Visually, yes. The median time on the new page was nearly two minutes higher. A two-sample t-test confirmed it. With the treatment group correctly specified first and the alternative set to 'greater', the p-value came back at 0.0001, well below the 5% threshold. Users spend significantly more time on the new page.

**2. Does the new page convert more users?**

The control group converted at 42%. The treatment group converted at 66%. A two-proportions z-test returned a p-value of 0.016, well below the threshold. The new page converts significantly better.

**3. Does preferred language affect conversion?**

The sample was roughly split across English, Spanish, and French users. A chi-square test of independence returned a p-value of 0.985. Language has no statistically significant relationship with whether a user converts.

**4. Does preferred language affect time spent on the new page?**

English users averaged 6.7 minutes, French 6.2, Spanish 5.8. One-way ANOVA, after confirming normality (Shapiro-Wilk) and equal variances (Levene's test), returned a p-value of 0.432. No statistically significant difference in time spent across language groups.

---

## The Interesting Part

The new page wins on both dimensions that matter: users spend significantly more time on it and convert at a significantly higher rate. What's worth noting is that the visual analysis suggested both findings before the tests confirmed them. The median time difference was nearly two minutes and the conversion gap was 24 percentage points. The statistics did what they're supposed to do — confirm what the data was already showing.

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

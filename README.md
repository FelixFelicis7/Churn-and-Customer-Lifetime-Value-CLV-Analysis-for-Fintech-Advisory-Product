# Project Background

FinAdvisory is a fintech company that provides digital subscription-based investment advisory services to individuals through its monthly and annual plans. Until recently, much of this data had been underutilized in shaping customer retention and revenue strategy.

This project delivers a comprehensive analysis of customer churn and lifetime value (CLV) across subscription types and age cohorts over the 2020–2022 period. By integrating subscription records with demographic insights, the analysis identifies key trends in customer attrition and value contribution, ultimately enabling FinAdvisory to optimize its customer success, marketing, and financial planning strategies.

Insights and recommendations are provided across the following key areas:

- Churn Trends Analysis: Evaluation of churn behavior across monthly and annual subscribers, including changes over time, average customer lifetime, and segment-level churn risk.

- Segment-Level Insights: Analysis of churn performance by age group, highlighting high-risk and high-value customer segments.

- Customer Lifetime Value (CLV) Forecasting: Estimation of CLV by age and plan type, identifying which segments drive the most revenue and which are most at risk of early churn.

An interactive Tableau dashboard can be downloaded here.<br/>

# Data Structure & Initial Checks

FinAdvisory's data structure as seen below consists of four tables: subscriptions, cases, customers and products with 310,064 records. <br/><br/>





# Overview
1. Background and Overview
2. Data Structure Overview
3. Executive Summary
4. Insights Deep Live
5. Recommendations



This project delivers a comprehensive churn-and-lifetime-value analysis for two fintech advisory subscriptions—annual and monthly—over the 2020–2022 period. By integrating customer sign-up and cancellation dates with demographic attributes, we calculate key metrics - churn rate, average lifetime, and churn-risk levels—across subscription types and age cohorts. Those metrics feed into segment-specific Customer Lifetime Value (CLV) projections, empowering marketing managers to design tailored campaigns (e.g. high-CLV/low-churn vs. high-CLV/high-churn cohorts) and product managers to prioritize feature development and subscription enhancements based on observed churn drivers.

#### About Dataset
This analysis uses four relational tables covering **January 1, 2020 – December 31, 2022**, with **~310 K subscription records**. It captures customer behavior, product details, and support interactions for two fintech advisory subscriptions (annual & monthly).

| Table           | Rows     | Purpose                                  | Key Fields                                                            |
| --------------- | -------  | ---------------------------------------- | --------------------------------------------------------------------- |
| customers       | ~50 K    | Profiles and demographics                | `customer_id`, `signup_date`, `age`, `gender`, `gender`               |
| subscriptions   | ~310 K   | Sign-up/cancellation history             | `subscription_id`,  `product_type`, `signup_date`, `cancellation_date`|
| cases           | ~200 K   | Call-center interactions                 | `case_id`, `customer_id`, `contact_time`, `contact_reason`            |
| pricing         | 2        | List prices & discount rules             | `product_type`, `price`                                               |

#### Business Questions and Objectives

1.Churn Analysis

- Overall & Trend:
  - What is the overall and churn rate for annual vs. monthly subscribers?
  - How have monthly vs. annual subscription churn rates evolved from Jan 2020–Dec 2021?
- Segment Differences:
  - Which age cohorts(e.g.'25-40','40-55',etc.) exhibit the highest churn risk?
- Tenure
  - What is the average time-to-churn (mean & median customer lifetime) in each age × product segment?
- Risk
  - How can we define low / medium / high churn-risk levels, and what is the distribution of those levels across age groups? 

2. Customer Lifetime Value (CLV)
- Value by Segment
  -What is the CLV for each age group and subscription type?
- Value & Risk Matrix
  -Which cohorts combine high CLV with high churn risk, and which are low-risk/low-value?

3. Revenue Forecasting

- Assuming steady new-customer growth, how will historical churn trends and CLV projections drive 2022 revenue for annual vs. monthly plans?
- Under a 5–10% reduction in churn among high-risk cohorts, what incremental revenue uplift could we expect in 2022?

#### Key Insigts

High-risk cohorts: e.g. monthly subscribers aged 18–25 churn at 45% vs. 22% overall

High-value at risk: 35–44-year-olds on annual plans have the highest CLV yet moderate churn risk

Revenue drivers: a 5% reduction in monthly churn yields a $XM lift in 2022

Staffing hotspots: peak call volume between 10 AM–12 PM on weekdays

#### Strategic Recommendations To Stakeholders

1. Marketing & Growth
- Tailored campaigns for “high-CLV/high-risk” cohorts (e.g. exclusive webinars)
- Referral bonuses for low-risk/high-CLV segments

2. Product & Customer Success
- Feature prioritization: invest in in-app guidance where churn spikes
- Proactive outreach: automated check-ins for cohorts at 80% probability of churn

3 Finance & Operations
- Pricing experiments: test annual discounts vs. monthly promotions to optimize CLV
- Staffing plan: align care-team headcount with forecasted case-volume heatmap

#### Limitations & Next Steps
- Data gaps: e.g. no in-product usage logs
- Model refinements: incorporate NLP on case topics
- Extended analyses: lifetime value by channel-of-acquisition



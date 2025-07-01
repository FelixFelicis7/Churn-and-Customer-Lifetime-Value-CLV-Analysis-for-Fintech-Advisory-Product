# Churn-and-Customer-Lifetime-Value-CLV-Analysis-for-Fintech-Advisory-Product

# Overview

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


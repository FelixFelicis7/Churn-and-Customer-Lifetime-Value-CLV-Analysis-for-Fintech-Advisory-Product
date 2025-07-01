# Churn-and-Customer-Lifetime-Value-CLV-Analysis-for-Fintech-Advisory-Product

# Overview

This project delivers a comprehensive churn-and-lifetime-value analysis for two fintech advisory subscriptions—annual and monthly—over the 2020–2022 period. By integrating customer sign-up and cancellation dates with demographic attributes, we calculate key metrics - churn rate, average lifetime, and churn-risk levels—across subscription types and age cohorts. Those metrics feed into segment-specific Customer Lifetime Value (CLV) projections, empowering marketing managers to design tailored campaigns (e.g. high-CLV/low-churn vs. high-CLV/high-churn cohorts) and product managers to prioritize feature development and subscription enhancements based on observed churn drivers.

# About Dataset

This analysis uses four relational tables covering January 1, 2020 – December 31, 2022, with a total of ∼310 K subscription records. It captures customer behavior, product details, and support interactions for two fintech advisory subscriptions (annual & monthly).

Table	Rows	Purpose
customers	~50 K	Profiles and demographics
subscriptions	~310 K	Sign-up/cancellation history & pricing
cases	~200 K	Call-center interactions
pricing	2	List prices & discount rules

1. customers

PK: customer_id

Fields:

signup_date (DATE)

date_of_birth (DATE) → used to compute age

gender (ENUM)

region (VARCHAR)

2. subscriptions

PK: subscription_id

FK: customer_id

Fields:

product_type (ENUM: “Annual” / “Monthly”)

signup_date (DATE)

cancellation_date (DATE or NULL)

price (DECIMAL)

3. cases

PK: case_id

FK: customer_id

Fields:

contact_time (DATETIME)

contact_reason (VARCHAR)

resolution_time_hrs (FLOAT)

4. pricing

Fields:

product_type (ENUM: “Annual” / “Monthly”)

list_price (DECIMAL)

discount_eligible (BOOLEAN)

Additional notes:

A NULL cancellation_date indicates an active subscription as of 2022-12-31.

Call-center logs are event-level; each row is one interaction.

Age segments are derived from date_of_birth at the time of each subscription event.

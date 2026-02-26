# Practical Application Assignment 11.1: What Drives the Price of a Car?

## Project Overview

This project analyzes a dataset of 426,000 used cars to understand the key factors that influence the car pricing. The goal is to provide actionable insights and recommendations to a used car dealers to help fine‑tune inventory for better pricing.

## Contents
``prompt_II.ipynb`` – main analysis notebook (CRISP‑DM: business understanding → data understanding → preparation → modeling → evaluation → findings).

``vehicles.csv`` – used car dataset provided with the assignment.

``README.md`` – this summary.

``prompt_II.ipynb`` - the jupyter notebook []()https://github.com/gundaja/what_drives_the_price_of_a_car/blob/main/prompt_II.ipynb

## Summary of Findings

**Business & Data Understanding**

The goal was to figure out what factors have the biggest impact on used car prices so the dealership can better manage its inventory. We turned this into a supervised learning project using multivariate regression to measure how both customer traits (like age, income, and travel distance) and car features (like transmission, body style, and engine type) affect price.

**Data Cleaning & Outliers**

To ensure a high-quality model, we performed extensive data preparation:

Outlier Mitigation: We removed "bait" listings (prices too low) and extreme luxury outliers (prices too high) that do not reflect the standard market.

Integrity Checks: We addressed missing values in the odometer and categorical columns (fuel, title status) to prevent biased predictions.

Feature Engineering: We transformed "Year" into "Vehicle Age" to more accurately capture the rate of depreciation over time.

**Key Price Drivers**

Our regression models (Ridge and Lasso) identified the following as the most significant predictors of value:

Odometer & Age: Mileage and age remain the strongest negative drivers of price, following a predictable depreciation curve.

Vehicle Type (Demand): There is high demand for 4-door vans and SUVs, which maintain higher resale value compared to sports cars or smaller sedans.

Mechanical Features: Automatic transmissions and specific engine configurations (cylinders) are preferred by the broader customer base, commanding a price premium.

## Recommendations for the Dealership

Inventory Focus: Prioritize stocking 4-door vehicles with moderate mileage (under 80,000 miles), as these represent the "sweet spot" for value retention.

Strategic Pricing: Use the identified model coefficients to set baseline prices for trade-ins, ensuring you don't overpay for features that consumers currently undervalue (like specific paint colors).

Market Opportunity: Use the outlier detection logic to identify undervalued vehicles in the market that are priced "too low" relative to their mechanical features.

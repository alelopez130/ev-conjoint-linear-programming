# Smooth Ride EV: Conjoint Analysis & Production Optimization

A quantitative business modeling project combining conjoint analysis and linear programming to guide a fictional EV manufacturer's (Smooth Ride) market entry into the UK electric vehicle industry. Completed as an individual assignment at Hult International Business School.

## Overview
Smooth Ride is entering the UK EV market with Basic and Premium models. This project models (1) consumer willingness-to-pay across vehicle attributes using conjoint analysis, and (2) the profit-maximizing production mix between Basic and Premium units under varying resource and capacity constraints using linear programming.

## Part 1: Conjoint Analysis
- **Design:** 5 attributes (Battery Range, Charging Speed, Vehicle Size, Acceleration, Price) generating 288 possible profiles, reduced to a 36-profile fractional design with orthogonal (uncorrelated) attribute levels.
- **Method:** Regression on preference scores with dummy-coded attribute levels (R² = 0.80).
- **Key findings:**
  - Battery Range (39.9%) and Price (39.0%) are the two dominant drivers of customer preference — nearly tied in importance.
  - Product A (high price, large battery) outperforms Product B on total utility (6.44 vs. 4.47), showing customers will pay a premium for sufficient range.
  - Vehicle Size and Acceleration matter considerably less, confirming genuine spec-vs-cost trade-offs among customers.
- **Limitations discussed:** binary attribute levels obscuring nuance, multicollinearity risk (e.g. price vs. battery size), the additive-utility assumption, and the static nature of a one-time preference snapshot.

## Part 2: Production Optimization (Linear Programming)
Objective: maximize π = 1·B + (1+α)·P, subject to a combined capacity constraint and a resource constraint (Basic = 2 resources/unit, Premium = 4 resources/unit), where α represents a variable profit multiplier on Premium units (supply chain, commodity pricing, or competitive pressure).

Scenarios modeled:
| Scenario | Capacity | Resources | Key Result |
|---|---|---|---|
| Base case | 10 | 20 | Tipping point at α = 1; below it, all-Basic is optimal (£10 profit); above it, all-Premium (up to £20 at α = 3) |
| Extra resources | 10 | 25 | Mixed production (8 Basic / 2 Premium) becomes optimal pre-tipping point; max profit rises to £24 |
| Reduced capacity | 8 | 20 | Tipping point unchanged at α = 1, but capacity cuts hurt Basic-focused profit most (£8 vs. £10) |

**Key insight:** The α = 1 tipping point is the critical variable to monitor — capacity investment is most valuable specifically when market conditions favor Premium production.

## Recommendations to Leadership
- Treat the linear programming and conjoint models as decision-support compasses, not static rules — monitor α in real time and reallocate resources when it crosses 1.
- Pair the LP model with demand forecasting and scenario planning, since the model assumes all production can be sold.
- Explore a mid-tier vehicle model, since Battery and Price are nearly equally important to customers — suggesting an underserved, price-sensitive-but-range-conscious segment.

## Repository Contents
- `Business_Modeling_A1.docx` — full written report with methodology, tables, and analysis
- `DatasetBMO.xlsx` — underlying data and calculations (raw conjoint data, regression output, conjoint utility analysis, and optimization sensitivity tables for all three resource/capacity scenarios)

## Tools
Excel (regression, sensitivity analysis, linear programming), Microsoft Word

## Author
Alejandro Lopez Macrobio

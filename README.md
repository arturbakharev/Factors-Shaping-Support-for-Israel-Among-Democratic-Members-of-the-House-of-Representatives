# Factors Shaping Support for Israel Among Democratic Members of the U.S. House of Representatives

A data-driven Mater's Thesis analyzing legislative behavior, voting dynamics, and external policy factors in the U.S. House of Representatives.

## Project Overview
This repository contains the analytical pipeline, statistical models, and econometric methodology for my Master's Thesis. The project models how various behavioral, political, financial, and social vectors influence voting patterns and digital stances on critical foreign policy legislation over consecutive timeframes (November to April)[cite: 6].

## Key Technical & Methodology Highlights
* **Rare Event Modeling (Firth Penalization):** Utilized Firth Penalized Logistic Regression (`logistf`) for vote transition modeling to robustly handle rare events and prevent complete separation issues common in standard logistic models.
* **Dynamic Sentiment & Vote Transitions:** Modeled both quantitative roll-call votes (Yea/Nay) and continuous digital stance scores across multiple legislative periods (V1 to V3) using transitional linear models.
* **Feature Engineering for Heavy-Tailed Data:** Applied `log1p` transformations to non-linear variables, specifically normalizing local protest surges (Pro-Israel vs. Pro-Palestine) to accurately measure their impact on legislative behavior.
* **Causal Inference & Rigorous Controls:** Designed a robust statistical framework isolating key independent variables while applying strict controls for district demographics (Jewish Population %, Cook PVI), campaign finance (AIPAC Contributions), and representative identity markers.
* **Publication-Ready Data Visualization:** Engineered complex, presentation-ready visualizations using `ggplot2` (e.g., boxplots with underlying jittered data distributions and statistical significance markers).

## Tech Stack & Libraries
* **Language:** R
* **Data Wrangling:** `dplyr`, `readr`
* **Econometrics & Statistics:** `logistf` (Firth's penalized likelihood), base R `lm` and `t.test`
* **Reporting & Visualization:** `modelsummary`, `ggplot2`

## Repository Structure
* `Analysis.Rmd`: The core R Markdown notebook containing data transformations, regression models, and visualization logic.
* `data.csv`: Panel dataset containing roll-call votes, PAC contributions, and district demographics for each representative.

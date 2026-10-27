# Housing Cost Overburden in the EU-27 (2014–2024)

**Country and Household Differences, 2014–2024**

**Author:** Adil Amin\
**Report Type:** Independent Research Report\
**Report Date:** 17 October 2026

## Project Overview

This project examines housing cost overburden across the 27 European Union member countries from 2014 to 2024. Using Eurostat data from the European Union Statistics on Income and Living Conditions (EU-SILC), the study investigates changes in national housing cost overburden rates, differences between countries, and disparities across selected household types.

Housing cost overburden is defined as the percentage of people living in households where total housing costs exceed 40% of disposable household income, with both costs and income measured net of housing allowances.

The research combines descriptive statistics, comparative visualisations, and panel-data regression models to assess changes over time. Its purpose is to provide a transparent, evidence-based account of measured housing affordability across the EU-27, without attributing the observed changes to specific policies or establishing causality.

## Research Objectives

1. Examine changes in the unweighted average national housing cost overburden rate between 2014 and 2024.
2. Compare housing cost overburden rates across the 27 EU countries and identify national differences in 2024.
3. Analyse country-level trends, with particular attention to Austria, Germany, France, Italy, and Spain.
4. Investigate differences in housing cost overburden by household composition in five selected countries in 2024.
5. Evaluate the relationship between calendar time and housing cost overburden using pooled and fixed-effects regression models.

## Data Sources

The study uses two official Eurostat EU-SILC datasets:

- **Housing Cost Overburden Rate:** [`tespm140`](https://ec.europa.eu/eurostat/databrowser/view/tespm140/default/table?lang=en)
- **Housing Cost Overburden Rate by Household Type:** [`ilc_lvho07e`](https://ec.europa.eu/eurostat/databrowser/view/ilc_lvho07e/default/table?lang=en)

**Study Period:** 2014–2024\
**Geographical Coverage:** 27 European Union countries\
**Main Country-Year Observations:** 296\
**Household Comparison:** 15 observations across five countries and three household categories in 2024

The main dataset contains 296 of the 297 possible country-year observations. **France's 2021 observation is missing and was not imputed.** The analysis uses the supplied Eurostat CSV snapshots rather than newly downloaded or revised data.

## Methodology

The statistical analysis uses the Eurostat CSV extracts and R analysis scripts identified in the original project materials.

The primary analytical techniques include:

- Data cleaning, filtering, and validation
- Descriptive statistics and unweighted cross-country comparisons
- Annual trend analysis and country-level comparisons
- Country-year heatmap visualisation
- Household composition comparisons for 2024
- Pooled Ordinary Least Squares (OLS) regression
- Country fixed-effects regression with country-clustered standard errors
- Country and year fixed-effects regression
- Regression diagnostics and sensitivity analyses

The report presents five main research figures, an additional regression diagnostic panel, and statistical summary tables. National averages are **unweighted averages of available country rates**, not population-weighted EU aggregates.

## Key Research Findings

| Indicator | 2014 | 2024 |
| --- | ---: | ---: |
| Average national housing cost overburden rate | 10.55% | 7.80% |
| Median national housing cost overburden rate | 9.0% | 6.7% |
| Standard deviation across national rates | 7.81 pp | 4.96 pp |

**Major Findings:**

- The unweighted average national housing cost overburden rate declined by approximately **2.76 percentage points** between 2014 and 2024.
- **21 countries** recorded lower rates in 2024 than in 2014, while **six countries** recorded increases.
- **Greece** had the highest overburden rate in 2024 at **28.9%**, while **Cyprus** had the lowest at **2.4%**.
- Greece recorded the largest endpoint decline, from **44.9% in 2014** to **28.9% in 2024**, a decrease of **16.0 percentage points**.
- Among the six countries with increases, **Malta** recorded the largest rise at **4.3 percentage points**.
- In Austria, Germany, France, Italy, and Spain, people in **one-adult households** had higher overburden rates than those in households with two adults and two dependent children in 2024.
- The country fixed-effects model estimated an annual decline of **0.302 percentage points** (95% confidence interval: **−0.484 to −0.120**; **p = 0.0022**).
- The estimated negative trend remained in the reported sensitivity analyses excluding Greece, excluding Germany, and using a balanced 26-country panel without France.

The findings indicate a broad but uneven reduction in measured housing cost overburden. They do not establish the causes of these changes or demonstrate uniform improvements in every dimension of housing affordability.

## Project Structure

The research report identifies the following project components:

- `tespm140.csv`: Archived Eurostat national housing cost overburden data.
- `ilc_lvho07e.csv`: Archived Eurostat housing cost overburden data by household type.
- `housing_clean.csv`: Cleaned country-year analysis dataset referenced in the report.
- **R analysis scripts:** Original scripts for processing the source data and producing statistical analysis outputs.
- **Research figures and statistical tables:** Descriptive visualisations, regression results, diagnostics, and sensitivity summaries.
- **Final research report (PDF):** Research write-up presenting the methodology, results, discussion, limitations, references, and reproducibility information.

The supplied report does not specify a complete repository directory structure, so no additional folder names are assumed here.

## Reproducibility

The analysis is based on retained Eurostat CSV snapshots and R scripts identified in the original project materials. The report states that its presentation preserves previously reported numerical results and visualisations; it does **not** claim that the analysis was independently rerun from the raw data while preparing the report.

To reproduce the statistical analysis using the original project materials:

1. Use the archived `tespm140.csv` and `ilc_lvho07e.csv` source files rather than replacing them with updated Eurostat downloads.
2. Open and review the corresponding original R analysis scripts.
3. Apply the report's EU-27 country selection and the 2014–2024 period.
4. Preserve the missing France 2021 observation without interpolation or imputation.
5. Run the scripts to regenerate and compare the cleaned dataset, descriptive summaries, figures, regression models, and sensitivity results against the report.

**Statistical Software:** R\
**Referenced Regression Package:** `fixest`

The report does not specify an R version, a complete package list, or a package lockfile. The original source CSV download date is also not recorded. These details should be checked against the original project files before claiming fully automated reproducibility.

## Research Limitations

This study uses aggregate observational data and cannot identify the causal effects of policies, economic conditions, or household composition on housing cost overburden.

National measurement breaks, including documented changes affecting Germany in 2020 and 2023, complicate comparisons across years. The main panel also lacks France's 2021 value, while the archived CSV files do not include observation-status flags for a complete record-level quality assessment.

The unweighted national average does not represent a population-weighted EU-wide rate. The household comparison covers only five countries, three household categories, and one year. Survey standard errors, household microdata, and key explanatory factors such as income, tenure, and location are not available in the supplied analysis.

## Conclusion

The study finds that measured housing cost overburden generally declined across the EU-27 between 2014 and 2024, with the average national rate falling by approximately 2.76 percentage points. However, substantial differences remained between countries and household types, and six countries experienced higher endpoint rates.

Panel-data models support a negative association between calendar time and housing cost overburden, but the results are descriptive rather than causal. The project documents long-term trends, persistent inequalities, and important comparability limitations using official European statistical data.

## Author

**Adil Amin**\
Independent Research Report

**Data Source:** Eurostat (EU-SILC)\
**Research Period:** 2014–2024

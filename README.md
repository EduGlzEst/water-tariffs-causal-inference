# Causal Inference: Impact of Differentiated Water Tariffs in Mexico City (2018-2023)

## 📌 Project Overview
This project evaluates the causal impact of differentiated water tariffs on urban water consumption in Mexico City (CDMX)[cite: 1]. Despite an apparent abundance in coverage (98%), CDMX faces severe water scarcity and unequal distribution[cite: 1]. The local water system (SACMEX) implements a tiered tariff structure based on a socioeconomic Development Index by neighborhood block (manzana)[cite: 1]. 

This analysis aims to determine if this pricing structure effectively promotes efficient water usage across different income levels while maintaining vertical equity[cite: 1].

## ⚙️ Methodology
To isolate the causal effect of tariffs from underlying socioeconomic factors, an observational causal inference design was implemented:
*   **Method:** Propensity Score Matching (PSM) using Nearest Neighbor[cite: 1].
*   **Model Specification:** 
    $$Y_{(i)}=\alpha+\gamma D_{(i)}+\beta X_{(i)}+\epsilon_{(i)}$$[cite: 1]
    $$P(D_{(i)}=1|X_{(i)})=F(X_{(i)}^{\prime}\beta)$$[cite: 1]
*   **Control Variables (Covariates):** Population (2010), block area, average infrastructure leaks, infrastructure length, and network coverage per capita[cite: 1].
*   **Balance:** Post-matching standardized differences were reduced significantly (e.g., Population difference dropped from 0.15 to 0.02), ensuring robust comparability between treatment and control groups[cite: 1].

## 📊 Key Findings
The empirical results reveal complex patterns and significant asymmetries in the effectiveness of the current tariff structure[cite: 1]:
*   **High vs. Medium Tariffs:** High-category blocks consume consistently more water, averaging 5,418.9 m³ more than medium-category blocks (statistically significant at p<0.01)[cite: 1].
*   **Medium vs. Low Tariffs:** Medium-category blocks consume 951.1 m³ less than low-category blocks (p<0.05)[cite: 1].
*   **Policy Implications:** The disparity suggests the current structure is not effectively moderating consumption in high-income areas, though it shows greater effectiveness in middle-income sectors[cite: 1].

## 📂 Repository Structure
*   `data/`: (Placeholder) Processed datasets (anonymized).
*   `src/`: (Coming soon) Source code for data preprocessing, matching algorithms, and econometric modeling.
*   `docs/`: Contains the full research paper detailing the theoretical framework and extended findings.

# Causal Inference: Impact of Differentiated Water Tariffs in Mexico City (2018-2023)

## 📌 Project Overview
This project evaluates the causal impact of differentiated water tariffs on urban water consumption in Mexico City (CDMX). Despite an apparent abundance in coverage (98%), CDMX faces severe water scarcity and unequal distribution. The local water system (SACMEX) implements a tiered tariff structure based on a socioeconomic Development Index by neighborhood block (manzana). 

This analysis aims to determine if this pricing structure effectively promotes efficient water usage across different income levels while maintaining vertical equity.

## ⚙️ Methodology
To isolate the causal effect of tariffs from underlying socioeconomic factors, an observational causal inference design was implemented:
*   **Method:** Propensity Score Matching (PSM) using Nearest Neighbor.

  <img width="1214" height="816" alt="image" src="https://github.com/user-attachments/assets/81ab179f-316c-420d-a9c1-f59cbf799fe8" />

*   **Model Specification:** 
    $$Y_{(i)}=\alpha+\gamma D_{(i)}+\beta X_{(i)}+\epsilon_{(i)}$$.
    $$P(D_{(i)}=1|X_{(i)})=F(X_{(i)}^{\prime}\beta)$$[cite: 1]
*   **Control Variables (Covariates):** Population (2010), block area, average infrastructure leaks, infrastructure length, and network coverage per capita.
*   **Balance:** Post-matching standardized differences were reduced significantly (e.g., Population difference dropped from 0.15 to 0.02), ensuring robust comparability between treatment and control groups.
*   ### Covariate Balance (Post-Matching)
<img width="1568" height="894" alt="Captura de pantalla 2026-08-29 143031" src="https://github.com/user-attachments/assets/e6a1ceea-8d31-4a00-b0c8-f6ee4bbe15b6" />



## 📊 Key Findings
The empirical results reveal complex patterns and significant asymmetries in the effectiveness of the current tariff structure:
*   **High vs. Medium Tariffs:** High-category blocks consume consistently more water, averaging 5,418.9 m³ more than medium-category blocks (statistically significant at p<0.01).
*   **Medium vs. Low Tariffs:** Medium-category blocks consume 951.1 m³ less than low-category blocks (p<0.05).
*   **Policy Implications:** The disparity suggests the current structure is not effectively moderating consumption in high-income areas, though it shows greater effectiveness in middle-income sectors.

## 📂 Repository Structure
*   `data/`: (Placeholder) Processed datasets (anonymized).
*   `src/`: (Coming soon) Source code for data preprocessing, matching algorithms, and econometric modeling.
*   `docs/`: Contains the full research paper detailing the theoretical framework and extended findings.

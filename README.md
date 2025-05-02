## Workflows for undertaking the terrestrial Ecosystem Protection Level (EPL) assessment

### **National Biodiversity Assessment - South Africa**

*South African National Biodiversity Institute (SANBI)*

February 2025

#### Summary

*This Repository contains a workflow that results in the 2025 Ecosystem Protection Level indicators for Terrestrial Ecosystems of South Africa. The terrestrial ecosystem map (vegetation), land cover change data and protected areas time series data were prepared in ARCGIS PRO and imported to R. The three layers were aligned and stacked and then cross tabulated (using the terra package). This analysis is focused on producing statistics on protected areas coverage for South Africa and includes steps to mask out ecosystem extent that extends into Eswatini and Lesotho. The results were summarised in R (using tidyverse package) and Ecosystem Protection Level was calculated for each type.*

``` mermaid
flowchart LR; 
A[Land cover change data ARCGIS] --> B[cross tabulation R-terr] --> C(Summary R-tidy) --> D[Terrestrial EPL 2025 results]; 
E[Protected areas time series ARCGIS] --> B; 
F[Vegetation map ARCGIS] --> B; 
```

The details of the workflow can be found in the Quarto document [Terr_EPL.qmd](Terr_EPL.qmd).

The overall results table can be found here: [outputs/results_df_EPL_veg.csv](outputs/results_df_EPL_veg.csv)

Biome level summaries: [outputs/results_df_EPL_biome.csv](outputs/results_df_EPL_biome.csv)

National PA statistics can be extracted from the cross-tabulation results: [outputs/sa_pa_rall.csv](outputs/sa_pa_rall.csv)

2024_Q4 overall PA extent per biome split into natural and non natural extent: [outputs/results_df_pa2023_natnotnat_biome.csv](outputs/results_df_pa2023_natnotnat_biome.csv)

PA extent over time per biome (including natural and non natural portions of PAs): [outputs/results_df_pa_9023_biome.csv](outputs/results_df_pa_9023_biome.csv)

Proportional PA extent over time per biome (including natural and non natural portions of PAs): [outputs/results_df_prp_pa_9023_biome.csv](outputs/results_df_prp_pa_9023_biome.csv)

#### Additional analysis to incorporate the negative impact of invasive alien plants within Protected Areas in the calculation of EPL for 2023.

Terrestrial Ecosystem Protection Level was calculated with the inclusion of additional steps to utilise combined invasive alien plant data. This assessment is for 2023 only and highlights ecosystem types for which protection within the PA network is compromised by dense invasive alien plant occurrence.

``` mermaid
flowchart LR;  
A[Land cover 2023 with invasives ARCGIS] --> B[cross tabulation R-terr] --> C(Summary R-tidy) --> D[Terrestrial EPL 2023 adjusted results];  
E[Protected areas time series ARCGIS] --> B;  
F[Vegetation map ARCGIS] --> B; 
```

Details of the workflow can be found in this quarto document [Terr_EPL_with_inv.qmd](Terr_EPL_with_inv.qmd)

The overall results can be found here: [outputs/results_df_EPL_2023_invasives.csv](outputs/results_df_EPL_2023_invasives.csv)

Biome level summary results can be found here: [outputs/results_df_EPL_2023_biome_invasives.csv](outputs/results_df_EPL_2023_biome_invasives.csv)

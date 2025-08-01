# Highway Don't Care (About Birds): Traffic Noise Impact on Bird Populations Along I-95
#### Summer 2025 Capstone Project 
#### Team Members:  Laura Lubben, Martha Laguna, Jack Lucas Chang & Sooneui Kim<br>

### Project Overview <br>
This capstone project investigates how traffic noise along Interstate 95 affects bird populations, using citizen science bird observation data and traffic datasets. We developed predictive models and spatial analysis tools to quantify correlations and assess impacts.

This project aims to develop a predictive analytics framework to investigate the relationship between traffic noise along the Interstate 95 corridor and bird observation patterns in adjacent habitats. By integrating citizen science data from eBird with traffic monitoring datasets, this study employs statistical modeling to quantify how highway noise levels correlates with bird observation counts. The research addresses a critical conservation challenge as North America has lost over 3 billion birds since 1969, with traffic noise identified as a significant environmental stressor that interferes with avian communication, disrupts migratory behaviors, and increases physiological stress. Through gradient boosting models, this project will identify noise impact zones and quantity threshold levels where bird observations decline significantly. 

### Research Questions
1. How do bird observations correlate with traffic noise along I-95?
2. What role does traffic volume and vehicle type play?
3. Can we predict bird population changes under different noise scenarios?

### Methodology & Technical Approach
- **Data Sources:** eBird (2020–2023), FHWA HPMS
- **Noise Modeling:** `Noise (dB) = 55 + 10×log₁₀(volume) + vehicle_mix_adjustment`
- **ML Models:** XGBoost, Random Forest, LightGBM
- **Spatial Analysis:** Custom polygon filters within 5 miles of highway

### Key Findings
- Minimal linear correlation between noise and bird counts (r ≈ -0.007)
- Temporal features (season, time-of-day) had higher predictive value
- Station-specific modeling showed localized improvements
- Observer bias significantly affected data quality

### Geographic Scope
- Virginia: Richmond to Fredericksburg (40+ miles)
- Maine: 194 miles along I-95/I-295
- ~950,000 bird observations analyzed

### Repository Contents
- `data/`: Scripts to preprocess bird and traffic data
- `notebooks/`: EDA, ETL, modeling, and feature analysis Jupyter notebooks
- `docs/`: Final report and presentation slides

### Model Performance Summary
| Model        | R² (Test) | RMSE (Test) |
|--------------|-----------|-------------|
| Baseline     | 0.0775    | 1.2592      |
| XGBoost      | 0.0882    | 1.2507      |
| LightGBM     | 0.1058    | 1.2385      |

*Weighted station sampling improved performance to R² ≈ 0.3852.*

### Future Work
- Deploy automated noise + bird audio monitoring systems
- Integrate generative AI for image/audio classification
- Build tools for transportation agencies to assess noise impact

### Resources
- [Final Report (PDF)](docs/final_report.pdf)
- [Interactive Map](#)
- [Project Presentation (Slides)](docs/presentation_slides.pdf)


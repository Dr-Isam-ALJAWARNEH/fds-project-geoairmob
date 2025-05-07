# Urban Mobility and Air Quality in UAE Cities: A Satellite-Driven Comparative Analysis

**GeoAirMob** is a collaborative research project conducted by undergraduate students from the University of Sharjah. It explores how human mobility patterns influence air quality in major UAE cities—**Dubai, Abu Dhabi, Sharjah, and Al Ain**—through the integration of satellite data, ground sensors, and mobility reports.

The Project report was compiled in overleaf using LaTeX editor
https://www.overleaf.com/3174811687jpmdzbnjqqbc#724546

---

This project follows a two-phase methodology developed in Python, combining data engineering, spatial modeling, and machine learning.

### Phase 1: Retrospective Analysis (2020–2022)

- Integrated historical data from:
  - **Google Community Mobility Reports**
  - **OpenAQ air quality measurements**
  - **Sentinel-5P satellite imagery**
- Standardized spatial resolution using **5-character geohash zones**
- Engineered features like mobility change rates and log-population density
- Applied **K-Means clustering** to detect pollution hotspots
- Built **Ordinary Least Squares (OLS)** regression models to quantify linear mobility–pollution relationships
- Designed three **synthetic mobility scenarios**:
  - Proportional shifts  
  - Spatial perturbations  
  - Population-weighted variations  
- Trained a **Gradient Boosting Regressor** (`n_estimators=100`, `max_depth=3`, `learning_rate=0.1`)  
- Selected the model with the best performance


### Phase 2: Forecast Scenario (2023–2025)
- Forecast Data Integration
We integrated Ericsson mobility forecast data with projected Sentinel-5P satellite rasters for the years 2023–2025. The data was spatially aligned by joining forecast values to the same geohash zones used in Phase 1, ensuring consistency across the temporal-spatial framework.

-Mapping and Geospatial Join
- Forecast mobility and pollution data were mapped to the Phase 1 geohash grid.
- This allowed for a unified view of both observed and predicted trends across urban and rural zones.
  
-Change Quantification
We quantified changes in pollution and mobility indicators using:
- **MAD**: Median Absolute Deviation
- **MAXD**: Maximum Difference across years
- **σ (Standard Deviation)**: To assess variability and signal stabilit
  
- Visual Analytics
We employed the following to interpret the results:
- **Time Series Plots**: Show mobility and pollutant trends by geohash
- **Raster Maps**: Forecasted pollution concentrations
- **σ-Spread Maps**: Spatial variability indicators
- **Cluster Overlays**: Future hotspot predictions
- 
-Risk Evaluation
We evaluated geohash zones for:
- **Mobility Growth**
- **Pollution Increase**
- **Volatility (σ)**
Zones exhibiting high combined values were flagged as **high-risk areas**, guiding future policy and intervention strategies.

---

## Key Outcomes

- Generated fine-grained **air quality risk maps**
- Identified **high-risk mobility zones** for policy and planning
- Created a reproducible, scalable modeling pipeline

---

## Repository Structure

- **`GEOCODE.ipynb`**: Complete code
- **`Datasets`**: Contains all the datasets used in work  
- **`Final_Report`**: Contains the full research paper  
- **`Presentation/Slides`**: Final presentation assets  
- **`Project_Figures`**: Plots and visual outputs from both phases  
- **`Related Works`**: Sources used for literature review  
- **`README.md`**: Project overview and documentation  
- **`Report_Writing_Progress(.docx files)`**: Report sections (Introduction, Methodology, Results, etc.)  
- **`Statement of Contribution.docx`**: Contains detailed roles and responsibilities of each team member

---

## Authors

- **Manal Ali Ahmed Alteneiji** — U23103284  
- **Hawra Mohammed S Al Sinan** — U22106610  
- **Mariam Khalid Ali Yousif Alali** — U23102355  
- **Asma Hassan Alhammadi** — U23200052

---

## License & Acknowledgments

This project is an academic submission under the **Department of Computing and Informatics**, University of Sharjah. All datasets used are open-source and credited accordingly.

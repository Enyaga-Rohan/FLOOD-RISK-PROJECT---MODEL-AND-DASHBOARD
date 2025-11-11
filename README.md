
FLOOD RISK PREDICTION IN NAIROBI USING MACHINE LEARNING AND ENVIRONMENTAL DATA”



 
 		INTRODUCTION/BACKGROUND
Flooding is a major natural hazard worldwide, worsened by climate change through more frequent and intense rainfall. 
Nairobi, Kenya, faces recurring flooding as well and this disrupts transport, damage property, and threaten public health. Heavy rainfall, low-lying areas, and expanding built-up regions make accurate flood prediction essential.

OBJECTIVES
The project aims to achieve the below objectives
•	To build a predictive model that estimates flood probability based on environmental and terrain data.
•	To provide a visual, interactive dashboard for easy interpretation.

DATA
I used the below datasets that combine meteorological, topographical, and remote-sensing observations to produce a rich set of features that describe rainfall patterns, terrain characteristics, vegetation cover, urbanization, and historical water presence
1.	CHIRPS Daily Rainfall Data (UCSB-CHG/CHIRPS/DAILY)
2.	SRTM Elevation Data (USGS/SRTMGL1_003)
3.	Sentinel-2 Satellite Imagery (COPERNICUS/S2_SR_HARMONIZED)
4.	Global Surface Water (JRC/GSW1_4)
 
All datasets used in this study are freely available for academic and research purposes through Google Earth Engine (GEE). CHIRPS rainfall data, SRTM elevation data, Sentinel-2 imagery, and the JRC Global Surface Water dataset are publicly hosted on GEE, allowing reproducible analysis without proprietary restrictions.

5. Methodology
•	Modeling approach:
o	Random Forest Classifier used for prediction.
o	Stratified cross-validation to evaluate performance (ROC-AUC).
•	Feature importance:
o	Built-up areas and vegetation coverage are most influential.
•	Dashboard:
o	Streamlit interface for inputting environmental variables and displaying flood probability with a map visualization.

6. Results (Preliminary)
•	Model performance (e.g., mean ROC-AUC Mean ROC-AUC: 0.78)
•	Feature importance summary
 
7. Discussion / Interpretation
•	What the model tells us:
o	Urbanization (NDBI) has the largest impact.
o	Vegetation (NDVI) also significantly reduces flood risk.
o	Rainfall features have moderate influence in this dataset.
o	
•	Limitations:
o	Model performance may vary with more diverse rainfall data.
o	Spatial coverage of NDVI/NDBI may limit predictions outside Nairobi.
o	Lack of soil data: The model does not account for soil type or permeability, which can influence water runoff and flood risk
8. Conclusion / Next Steps
•	Summary of findings
Urbanization increases flood risk, vegetation reduces it, and rainfall moderately influences flood probability in Nairobi.
The Streamlit dashboard allows users to input environmental and rainfall data for Nairobi to visualize flood probability, risk level, and location on a map, enabling quick, interactive flood risk assessment.
•	Recommendations or future improvements:
o	Include more rainfall events, soil data, or river proximity.
o	Extend dashboard to other regions 
Data Sources and Tools
•	Rainfall: CHIRPS daily precipitation data (UCSB-CHG/CHIRPS/DAILY), Google Earth Engine, free for academic use.
•	Terrain: SRTM (USGS/SRTMGL1_003) for elevation and slope.
•	Vegetation: NDVI from Sentinel-2 imagery (COPERNICUS/S2_SR_HARMONIZED).
•	Urbanization: NDBI from Sentinel-2 imagery.
•	Surface Water / Flood Labels: JRC Global Surface Water (JRC/GSW1_4).
•	Software & Tools: Python libraries (scikit-learn, pandas, matplotlib, seaborn, joblib, streamlit, pyngrok) and Google Earth Engine for data processing.
Datasets used in this project are accessed via Google Earth Engine (GEE). Users may need to sign in or authenticate with a GEE account to fully interact with the underlying data. GEE is free for academic purposes

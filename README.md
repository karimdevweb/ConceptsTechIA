
Urban Heat Island Analysis – Paris Neighborhoods
1. Project Objectives

The objective of this project is to analyze urban heat exposure across Paris neighborhoods and to identify homogeneous neighborhood typologies using unsupervised machine learning techniques.

- By clustering neighborhoods based on climatic, environmental, and urban infrastructure indicators, the project aims to:

- Detect neighborhoods that are more exposed to urban heat islands

- Understand which urban features contribute to higher or lower heat exposure

- Support data-driven urban climate adaptation strategies at the neighborhood scale

------------------

2. Data Sources

link to weather_data.csv : https://drive.google.com/drive/folders/1nmSjigS-GVTZ47OLcW0Zb3-XfTUOM5R_?usp=sharing
link to data_final.csv : https://drive.google.com/drive/folders/1nmSjigS-GVTZ47OLcW0Zb3-XfTUOM5R_?usp=sharing
link to tableau_installation_publique.csv : https://drive.google.com/drive/folders/1nmSjigS-GVTZ47OLcW0Zb3-XfTUOM5R_?usp=sharing

à télécharger et à mettre dans le dossier "Data" à la racine du projet


Several datasets were combined and aggregated at the Paris neighborhood level.
All datasets are aligned using a common neighborhood identifier.

| Dataset                           | Description                                                                      |
| --------------------------------- | -------------------------------------------------------------------------------- |
| Weather data (2021–2024)          | Temperature-related indicators aggregated by neighborhood                        |
| Heat Stress / Heat Exposure Index | Composite index measuring urban heat exposure                                    |
| Tree dataset                      | Tree count and tree density per neighborhood                                     |
| Public equipment dataset          | Urban equipment influencing local climate                                        |
| Public installations dataset      | Public installations such as fountains                                           |
| Paris neighborhoods spatial data  | GeoJSON file containing the geometry of Paris neighborhoods (≈ 80 neighborhoods) |

-----------------

3. Project Structure


ENV/

│
├── Data/
│   ├── ..........           # Original datasets (CSV, GeoJSON)
│   ├── ..........           # Cleaned and processed datasets
│   └── data_final.csv       # Final dataset used for modeling
│

├── used_lib/
│   └── requirements.txt     # Python dependencies
|

|── Ml_Flow 
│    └── paris_neighborhood_models.pkl
|

├── Import_and_EDA_Final.ipynb
├── ML_Notebook.ipynb
└── README.md

-----------------

4. Data Preparation & Exploratory Analysis

Notebook: Import_and_EDA_Final.ipynb

This notebook focuses on:

Importing all raw datasets

Cleaning and harmonizing data across sources

Performing exploratory data analysis (EDA)

Aggregating variables at the neighborhood level

Exporting a clean and consolidated dataset:
data_final.csv

---------------

5. Unsupervised Machine Learning Models

Notebook: ML_Notebook.ipynb

This notebook applies unsupervised learning techniques to identify neighborhood clusters:

K-Means clustering

Model selection using silhouette score and inertia

Final clustering and spatial visualization

DBSCAN

Density-based clustering for comparison

Identification of noise and spatial inconsistencies

Gaussian Mixture Models (GMM)

Probabilistic clustering

Comparison with K-Means results

Results are analyzed both in PCA-reduced feature space and through spatial maps of Paris neighborhoods.

-------------------


6. Key Outcomes

Identification of neighborhood clusters with similar heat exposure profiles

Clear spatial patterns related to urban heat islands

Comparison of multiple clustering approaches to assess robustness and interpretability

Actionable neighborhood typologies for urban climate analysis

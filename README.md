# Gun Violence Spatio-Temporal Cluster and Hotspot Analysis, Prediction, and Risk Classification

This project investigates the complex patterns of gun violence by analyzing both where (spatial) and when (temporal) incidents occur, using clustering to reveal underlying groupings and hotspots to pinpoint high-risk areas. It aims to identify distinct spatial and temporal clusters, understand the factors that may contribute to gun violence within these clusters, develop predictive models to forecast future incidents, and classify areas based on risk levels. The insights gained from cluster analysis and predictive modeling can inform data-driven strategies for violence reduction.

## Project Overview

Gun violence is a complex societal issue with devastating consequences. Understanding the underlying patterns and risk factors associated with gun violence is crucial for developing effective prevention and intervention strategies. This project employs spatial and temporal clustering, hotspot analysis, and machine learning techniques to analyze a dataset of gun violence incidents provided by the Chicago Police Department. By identifying distinct clusters and hotspots, we aim to uncover the geographic distribution (spatial patterns) and timing (temporal patterns) of these events. The project also incorporates a risk level classification component to categorize areas based on the predicted number of incidents, leveraging insights gained from cluster analysis.

## Dataset

The dataset used in this project is "Violence_Reduction_-_Victims_of_Homicides_and_Non-Fatal_Shootings.csv". This dataset contains information about individual victims of homicides and non-fatal shootings. It includes the following types of data (the exact columns may vary):

*   **Incident Details:** Date and time of the incident, type of incident (homicide, non-fatal shooting), location (latitude and longitude, potentially a location description like neighborhood or zip code), and possibly other details about the circumstances.
*   **Victim Demographics:** Age, sex, and race/ethnicity of the victim. *It is essential to handle this demographic data with extreme care due to ethical concerns and potential biases.*
*   **Incident Characteristics:** Information about the incident itself, such as whether it was domestic-related, involved juveniles, or involved a gunshot wound.

*(Note: The specific columns in the dataset may vary.  Refer to the data dictionary or data source for complete details.)*

## Methodology

The project employs a combination of techniques:

1.  **Spatial Analysis & Clustering:**
    * Kernel Density Estimation (KDE) is used to identify hotspots of gun violence.
    * K-means clustering is applied to identify spatial clusters of gun violence incidents, revealing underlying geographical patterns.
    * Spatial autocorrelation analysis may also be used to assess the clustering of incidents.

2.  **Temporal Analysis & Clustering:**
    * Temporal clustering (k-means) is used to identify distinct time periods with similar incident patterns (e.g., high-risk hours, days of the week, months).
    * Recurrent Neural Networks (RNNs), specifically LSTMs or GRUs, are used to model the time series data and forecast future incidents. ARIMA models may be used as a baseline for comparison.

3.  **Risk Factor Analysis:**
    * Regression models are used to explore potential correlations between various factors (including demographics, socioeconomic indicators, and incident characteristics) and gun violence.
    * *It is crucial to emphasize that these are correlations, not causal relationships, and that demographic data is used with extreme caution due to ethical concerns.*
    * The results of the clustering analysis will be used as features to improve the accuracy of the regression models.

4.  **Risk Level Classification:**
    * Areas are classified into risk categories (e.g., High, Medium, Low) based on the predicted number of incidents and/or the clustering data.
    * This classification can be based on thresholds defined by the user (e.g., based on the distribution of incidents) or derived from the inherent risk levels of the determined       
      clusters.

## Key Findings (To be populated after analysis)

* **Spatial Clustering:**
    * K-means clustering revealed three distinct spatial clusters of gun violence incidents, with Cluster 1 concentrated in the north_west region, Cluster 2 in the north_east, and 
      Cluster 3 in the south_east area.
    * Cluster 1 exhibited high incident density and was associated with areas of lower socioeconomic status.

* **Hotspot Analysis:**
    * Kernel Density Estimation identified several high-intensity hotspots, particularly in the vicinity of 'North Lawndale'.
    * Hotspots were found to be concentrated within the spatial clusters, indicating a strong correlation between cluster membership and high-risk areas.

* **Temporal Clustering:**
    * Temporal clustering revealed three distinct time periods: Cluster 1 (evening hours), Cluster 2 (weekends), and Cluster 3 (summer months).
    * Cluster 1 showed a peak in incidents between 8 PM and 12 AM, suggesting a correlation with nighttime activity.

## Model Performance (To be populated after model training)

 * The XGBoost model achieved an accuracy of 100% in predicting gun violence risk levels.
 * Spatial cluster membership and temporal cluster membership were significant predictors of risk.

## Ethical Considerations

This project acknowledges the sensitive nature of data related to gun violence and demographics. *Extreme care has been taken to avoid making generalizations or inferences that could reinforce harmful stereotypes.* The use of demographic data is limited to exploring potential correlations, not establishing causation. Transparency about the limitations of the data and potential biases is a priority.

## Getting Started

1.  Clone the repository: `git clone https://github.com/vipin-kallidumbil/Gun-Violence-Analysis-Spatio-Temporal-Patterns-and-Risk-Factors.git`
2.  Install the required libraries: `pip install -r requirements.txt`
3.  Run the code: `Gun Violence_Spatio-Temporal Analysis Prediction and Risk Classification.ipynb`

## Requirements

*   Python 3.x
*   Pandas
*   NumPy
*   Scikit-learn
*   TensorFlow/Keras (for Neural Network)
*   Folium (for mapping)
*   XGboost
*   imblearn
*   missingno (for visualizing missing data)
*   statsmodels
*   math
*   Other libraries as needed (list them in `requirements.txt`)


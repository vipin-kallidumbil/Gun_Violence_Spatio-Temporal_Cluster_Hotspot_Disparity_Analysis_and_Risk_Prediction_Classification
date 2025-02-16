# Gun Violence: Spatio-Temporal Analysis, Prediction, and Risk Classification

This project investigates the complex patterns of gun violence by analyzing both *where* (spatial) and *when* (temporal) incidents occur.  It aims to identify high-risk areas and time periods, understand the factors that may contribute to gun violence, develop predictive models to forecast future incidents, and classify areas based on risk levels. The insights gained can inform data-driven strategies for violence reduction.

## Project Overview

Gun violence is a complex societal issue with devastating consequences.  Understanding the patterns and risk factors associated with gun violence is crucial for developing effective prevention and intervention strategies. This project uses machine learning and statistical techniques to analyze a dataset of gun violence incidents, focusing on both the geographic distribution (spatial patterns) and the timing (temporal patterns) of these events.  It also incorporates a risk level classification component to categorize areas based on the predicted number of incidents.

## Dataset

The dataset used in this project is "Violence_Reduction_-_Victims_of_Homicides_and_Non-Fatal_Shootings.csv". This dataset contains information about individual victims of homicides and non-fatal shootings. It includes the following types of data (the exact columns may vary):

*   **Incident Details:** Date and time of the incident, type of incident (homicide, non-fatal shooting), location (latitude and longitude, potentially a location description like neighborhood or zip code), and possibly other details about the circumstances.
*   **Victim Demographics:** Age, sex, and race/ethnicity of the victim. *It is essential to handle this demographic data with extreme care due to ethical concerns and potential biases.*
*   **Incident Characteristics:** Information about the incident itself, such as whether it was domestic-related, involved juveniles, or involved a gunshot wound.

*(Note: The specific columns in the dataset may vary.  Refer to the data dictionary or data source for complete details.)*

## Methodology

The project employs a combination of techniques:

1.  **Spatial Analysis:** Kernel Density Estimation (KDE) is used to identify hotspots of gun violence. Spatial autocorrelation analysis may also be used to assess the clustering of incidents.

2.  **Temporal Analysis:** Recurrent Neural Networks (RNNs), specifically LSTMs or GRUs, are used to model the time series data and forecast future incidents. ARIMA models may be used as a baseline for comparison.

3.  **Risk Factor Analysis:** Regression models are used to explore potential correlations between various factors (including demographics, socioeconomic indicators, and incident characteristics) and gun violence. *It is crucial to emphasize that these are correlations, not causal relationships, and that demographic data is used with extreme caution due to ethical concerns.*

4.  **Risk Level Classification:**  Areas are classified into risk categories (e.g., High, Medium, Low) based on the predicted number of incidents.  This classification can be based on thresholds defined by the user (e.g., based on the distribution of incidents).

## Key Findings (To be populated after analysis)

*(This section will be filled in with the key insights and findings from the analysis, including any significant trends, hotspots, risk factors, and risk level classifications identified.)*

## Model Performance (To be populated after model training)

*(This section will include the performance metrics for the predictive models, such as Mean Absolute Error (MAE) or Root Mean Squared Error (RMSE) for the time series forecasting, and accuracy, precision, recall, and F1-score for the classification model.)*

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
*   TensorFlow/PyTorch (for RNNs)
*   Other libraries as needed (list them in `requirements.txt`)


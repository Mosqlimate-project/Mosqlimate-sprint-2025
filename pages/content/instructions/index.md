---
title: "Instructions - 3rd IMDC"
description: ""
---

The Infodengue–Mosqlimate Dengue Challenge (IMDC) is an international collaborative initiative focused on developing predictive models for dengue outbreaks in Brazil. Researchers and teams from different fields such as epidemiology, data science, statistics, and mathematical modeling are invited to participate by submitting forecasts based on open datasets provided by the organizers.
**In 2026, the challenge introduces two new components:**
* forecasting dengue cases for a selected set of cities identified through dengue risk criteria, and
* the inclusion of chikungunya data to support the development of forecasting models for this disease.

### 1. Team registration
Participants must form a research team and register for the challenge through the [registration section](../registration/) of the website. Teams may include researchers from different institutions and countries.

### 2. Data access
The training datasets will be available for download on an FTP server provided by the Mosqlimate platform. More information can be found in the [Data](../data/) section. The dataset used in the challenge includes primarily:
* dengue and chikungunya epidemiological data
* climate data
* demographic data

These data will be used to train and validate forecasting models. Participants are also welcome to explore the Mosqlimate data API to retrieve specific subsets of data. **Additional data sources may be used, provided they are shared with other participants through the organizers. Any additional datasets must be open-access, regularly updatable, and available for all Brazilian states**.

### 3. Model development and forecast submission
Each team develops its own forecasting model using different methodological approaches, such as:
* statistical models;
* mechanistic or epidemiological models;
* machine learning or artificial intelligence techniques.

You can take a look at the list of models submitted in previous years [here](https://mosqlimate.org/models?page=1).

Forecasts must be submitted in a standardized format through the [official challenge repository on GitHub](https://github.com/Mosqlimate-project/imdc_template_2026). This process ensures that all forecasts can be evaluated consistently.
The challenge includes four validation targets and one final forecast target. Each target corresponds to a dengue season in Brazil, defined from epidemiological week (EW) 41 of one year to EW 40 of the following year.
During the validation phase, participants generate retrospective forecasts using historical data available up to a given time point. This allows model performance to be evaluated under realistic forecasting conditions.
The validation targets are:

![](val_tests.png#center)

* Validation test 1: Predict the weekly number of dengue and chikungunya cases for the 2022–2023 season (EW41 2022 – EW40 2023), using data from EW01 2010 to EW25 2022.
* Validation test 2: Predict the weekly number of dengue and chikungunya cases for the 2023–2024 season (EW41 2023 – EW40 2024), using data from EW01 2010 to EW25 2023.
* Validation test 3: Predict the weekly number of dengue and chikungunya cases for the 2024–2025 season (EW41 2024 – EW40 2025), using data from EW01 2010 to EW25 2024.
* Validation test 4: Predict the weekly number of dengue and chikungunya cases for the 2025–2026 season (EW41 2025 – EW40 2026), using data from EW01 2010 to EW25 2025.

Finally, the forecast target focuses on predicting the weekly number of dengue cases for the 2026–2027 season (EW41 2026 – EW40 2027) using all data available from EW01 2010 to EW25 2026.

#### Geographic scope
 Submitted models must generate forecasts for the following geographic units:
**Dengue**

All Brazilian states and the following cities:
* Teixeira de Freitas (BA) - geocode: 2931350
* Vitória da Conquista (BA) - geocode: 2933307
* Brejo Santo (CE) - geocode: 2302503
* Coronel Fabriciano (MG) - geocode: 3119401
* São José do Rio Preto (SP) - geocode: 3549805
* Presidente Prudente (SP) - geocode: 3541406
* Rio Branco (AC) - geocode: 1200401
* Cruzeiro do Sul (AC) - geocode: 1200203
* Paraíso do Tocantins (TO) - geocode: 1716109
* Londrina (PR) - geocode: 4113700
* Cambé (PR) - geocode: 4103701
* Cascavel (PR) - geocode: 4104808
* Aparecida de Goiânia (GO) - geocode: 5201405
* Campo Novo do Parecis (MT) - geocode: 5102637
* Novo Gama (GO) - geocode: 5215231

The figure below shows the time series of dengue cases for the selected cities: 
![](cities_dengue.png#center)

**Chikungunya**

All Brazilian states and the following cities:
* Teresina (PI) - geocode: 2211001
* Teixeira de Freitas (BA) - geocode: 2931350
* Montes Claros (MG) - geocode: 3143302
* Coronel Fabriciano (MG) - geocode: 3119401
* Palmas (TO) - geocode: 1721000
* Paraíso do Tocantins (TO) - geocode: 1716109
* Cascavel (PR) - geocode: 4104808
* Xanxerê (SC) - geocode: 4219507
* Cuiabá (MT) - geocode: 5103403
* Campo Novo do Parecis (MT) - geocode: 5102637

The figure below shows the time series of chikungunya cases for the selected cities: 
![](cities_chik.png#center)

Please note that forecasts for both **dengue** and **chikungunya** were requested for the cities listed below: 
* Teixeira de Freitas (BA) - geocode: 2931350
* Coronel Fabriciano (MG) - geocode: 3119401
* Paraíso do Tocantins (TO) - geocode: 1716109
* Cascavel (PR) - geocode: 4104808
* Campo Novo do Parecis (MT) - geocode: 5102637

The figure below shows the time series of chikungunya and dengue cases for the selected cities: 
![](cities_dengue_chik.png#center)


<div style="border: 1px solid #FF0000; padding: 10px; background-color: #f9f9f9;">
<strong>Note:</strong> To participate in the challenge and be included in the reports, you must submit dengue forecasts for all validation periods and states, except for ES (which is not mandatory).

Dengue forecasts for ES, state-level chikungunya, and municipal-level dengue and chikungunya are **optional** parts of the challenge. However, for each additional state or city for which forecasts are submitted, they must cover all validation intervals.
</div>

#### Forecast outputs

Models should generate the following outputs:

1. Validation forecasts: predicted curves of dengue and chikungunya cases including
    * median estimate
    * 50%, 80%, 90%, and 95% predictive intervals.
2. Forecast target: predicted curves of dengue cases including
    * median estimate
    * 50%, 80%, 90%, and 95% predictive intervals.

The median estimate must correspond to the 50th percentile (0.5 quantile) of the predictive distribution. Predictive intervals should be defined using the appropriate lower and upper quantiles: the 50% interval corresponds to the 25th and 75th percentiles, the 80% interval to the 10th and 90th percentiles, the 90% interval to the 5th and 95th percentiles, and the 95% interval to the 2.5th and 97.5th percentiles.


### 5. Model evaluation
Models will be compared using predefined performance metrics. The evaluation includes:
* retrospective validation using historical data
* comparison across different forecasting methodologies

The following metric will be computed:
* Weighted Interval Score (WIS)
Interval predictions will be evaluated on a weekly basis


### 6. Ensemble model construction
An important component of the IMDC is the creation of an ensemble model, which combines forecasts from multiple teams. This collective model typically provides more robust and accurate predictions of dengue outbreaks.

### 7. Dissemination of Results
Results from the challenge will be presented through:
* scientific webinars
* project workshops
* technical reports and scientific publications.

### 8. Calendar

<img src="../calendar_imdc.png" style="display: block; margin: 0 auto;" />

Important dates: 
* **April 1, 2026** – Challenge launch and opening of team registrations
* **May 15, 2026** – Deadline for team registration
* **July 1, 2026** – Submission deadline for validation round results
* **July 31, 2026** – Webinar: Presentation of validation round results
* **September 10, 2026** – Submission deadline for 2026–2027 forecasts
* **September 22, 2026** – Internal webinar for teams to present model methodologies
* **October 15, 2026** – International webinar: Technical results of IMDC 2026
* **October 30, 2026** – International webinar: IMDC 2026 results for the general audience

### Previous editions: 

* [Instructions - IMDC 2025](2025/)

* [Intructions - IMDC 2024](2024/)
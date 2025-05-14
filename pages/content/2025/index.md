---
title: ""
description: ""
date: ""
---

This initiative is led by the Mosqlimate and Infodengue in collaboration with the Harmonize and IDExtremes projects.


## **Challenge**

The year 2024 has seen an exceptional number of reported dengue fever cases globally. In Brazil, besides the high incidence, the disease has spread to areas in the south or at altitudes where epidemics were not previously recorded, or where the incidence rate has far exceeded that of previous years. In the beginning of 2025, the dengue season was not expected to be as intense as in 2024 for most of the country, but we continue to see strong transmission throughout the country. 

The objective of this sprint is to promote, in a standardized way, the training of predictive models and to develop high-quality ensemble forecast models for dengue in Brazil.

The challenge involves three testing targets and one “true” forecast target. The period of interest spans from the epidemiological week (EW) 41 of one year to EW 40 of the following year, aligning with the typical dengue season in Brazil.

1. **Validation test 1.** Predict the weekly number of dengue cases by state (UF) in the 2022-2023 season [EW 41 2022- EW40 2023], using data covering the period from EW 01 2010 to EW 25 2022;
2. **Validation test 2.** Predict the weekly number of dengue cases by state (UF) in the 2023-2024 season [EW 41 2023- EW40 2024], using data covering the period from EW 01 2010 to EW 25 2023;

3. **Validation test 3:** Predict the weekly number of dengue cases by state (UF) in the 2024-2025 season [EW 41 2024- EW40 2025], using data covering the period from EW 01 2010 to EW 25 2024;
4. **Forecast.** Predict the weekly number of dengue cases in Brazil, and by state (UF), in the 2025-2026 season [EW 41 2025- EW40 2026], using data covering the period from EW 01 2010 to EW 25 2025;

Afterward, the best-performing models in the first 3 validation runs will be included in an ensemble forecast model for 2026, built by the organizers.

**Outcome variables**

Predictions should be made for all 27 Brazilian federative units. If, for some reason, a forecast cannot be generated for a specific state, the sprint organization will decide how to proceed and will communicate the appropriate guidelines to the participants.

**The models should generate the following outcome:**

1. **For the validation test:** Curve of dengue cases for seasons 2022-23, 2023-2024, and 2024–2025, by Epidemiological week (EW)  41 to 40, including median estimate and 50%, 80%, 90%, and 95% predictive intervals.
2. **For forecast:** Curve of dengue cases for season 2025-2026, by EW 41 to 40, including median estimate and 50%, 80%, 90%, and 95% predictive intervals.


## **Data**

The training datasets will be available for download as tar.gz files on an FTP server created by the Mosqlimate platform<sup>[^1]</sup>, along with a variable dictionary. Instructions to access this data are available [here](../data/).  Participants are welcome to peruse the [Mosqlimate data API](https://api.mosqlimate.org/datastore/) for specific subsets of data. Participants can use other data sources as long as they share them with other participants through the organizers. The data used must be open-access and updatable. It must also be available for all the Brazilian states.

List of available datasets these can be updated at any time:

|Type|Variables|Source|
| ------- | ------ | ------- |
|Epidemiological data|</p><p>Number of probable<sup>[^2]</sup> dengue cases per week per municipality ;</p>|From SINAN (aggregated by Infodengue and available in the [Mosqlimate API](https://api.mosqlimate.org/datastore/)). |
|Demographic data|Population per municipality (2001-2024);|Source: [SVS](http://tabnet.datasus.gov.br/cgi/deftohtm.exe?ibge/cnv/popsvs2024br.def). |
|Climate data|<p>Weekly temperature, humidity, precipitation,</p><p>El Niño/Southern Oscillation (ENSO), Pacific Decadal Oscillation (PDO),  Indian Ocean Dipole (IOD) </p>|From ERA5, aggregated by week and available in the [Mosqlimate API](https://api.mosqlimate.org/datastore/).|
|Climate forecast data|Monthly temperature, humidity, and precipitation|[Copernicus](https://cds.climate.copernicus.eu/datasets/seasonal-monthly-single-levels?tab=overview).|
|Environment data |Municipality main climate and biome |<p></p><p>[Koppen climate classification](https://koppenbrasil.github.io/);</p><p>[Biome type](https://www.embrapa.br/busca-de-publicacoes/-/publicacao/1144751/metodo-para-determinar-o-bioma-predominante-nos-municipios-brasileiros).</p>|


## **Forecast Evaluation**
For the evaluation, the *logarithmic score*, *CRPS,* and the *weighted interval score* will be computed. The calculation of the interval predictions will be done on a per-week basis. See references 1-5 for more information about the methodology applied in the sprint. 

## **Expected Outputs:**
- **A technical note** will be published by Infodengue, *in Portuguese*, with the results of the ensemble models. All participants of the sprint will be acknowledged. All groups that contributed models that meet the minimum quality criteria will be part of the publication.

- In the second semester of 2026, there will be an award for the model(s) that made the most useful forecast(s), with a date to be announced later.

- The forecasting exercise will be replicated in the following year if funding is available.
## **Important Dates:**

1. Release of Call for participation — May 15th, 2025
2. Forecast submission deadline (validation datasets) — June 30th, 2025
3. Webinar (Results of the validation round) — July 30th, 2025
4. 2nd Forecast submission deadline (2026 forecasts) - September 23rd, 2025
5. Presentation of the ensemble model - October 15th, 2025

## **How to participate in the Sprint**


To participate, you must fill out the [registration form](https://forms.gle/22FFzBZT4Jf5oqzt9) between  2025/05/15 and 2025/06/15. Before that, we recommend that you access the event website with detailed instructions and guidelines. 

We will maintain two communication channels for interaction between participants and the organization team to promote quick communication about any aspect of the event.

A discussion forum for participants on [Discord](https://discord.gg/yqtgW4TC). 

Virtual meetings will be organized during the sprint to answer questions and explain the model/forecast submission processes; the invitation for these meetings will be sent to the registered email.


## **Sprint Rules:**

1\. **Public GitHub Repository:** All participating models must maintain their code in a public GitHub repository created from this template permanently, even after the end of the event. The readme.md of the repository must contain an explanation of the methodology.

2\. **Forecast Submission Format:** The forecast submission format is documented in the template repository available [here](https://github.com/Mosqlimate-project/sprint-template-2025) and in the [API documentation](https://api.mosqlimate.org/docs/registry/POST/predictions/). The upload code will check the formatting before submission. 

3\. **Data Sharing:** Participants may use other data sources as long as they are anonymized and shared with other participants through the organizers. The data used must be open-access and updatable.

4\. To be considered for the validation round and ensemble construction, each submitted model must provide predictions for all target variables.

**Tutorials and support information can be found [here](../instructions/).** 

**References**

[1.	Banholzer, N. ](https://www.zotero.org/google-docs/?O1n02o)[*et al.*](https://www.zotero.org/google-docs/?O1n02o)[ A comparison of short-term probabilistic forecasts for the incidence of COVID-19 using mechanistic and statistical time series models.](https://www.zotero.org/google-docs/?O1n02o)

[2.	Gneiting, T. & Raftery, A. E. Strictly Proper Scoring Rules, Prediction, and Estimation. ](https://www.zotero.org/google-docs/?O1n02o)[*J. Am. Stat. Assoc.* ](https://www.zotero.org/google-docs/?O1n02o)[**102**](https://www.zotero.org/google-docs/?O1n02o)[, 359–378 (2007).](https://www.zotero.org/google-docs/?O1n02o)

[3.	Bracher, J., Ray, E. L., Gneiting, T. & Reich, N. G. Evaluating epidemic forecasts in an interval format. ](https://www.zotero.org/google-docs/?O1n02o)[*PLOS Comput. Biol.* ](https://www.zotero.org/google-docs/?O1n02o)[**17**](https://www.zotero.org/google-docs/?O1n02o)[, e1008618 (2021).](https://www.zotero.org/google-docs/?O1n02o)

[4.	Gneiting, T., Raftery, A. E., Westveld, A. H. & Goldman, T. Calibrated Probabilistic Forecasting Using Ensemble Model Output Statistics and Minimum CRPS Estimation. (2005) doi:10.1175/MWR2904.1.](https://www.zotero.org/google-docs/?O1n02o)

[5.Eduardo Correa Araujo, Luiz Max Carvalho, Fabiana Ganem, Lua Bida Vacaro, Leonardo Soares Bastos, Lais Picinini Freitas, Marcio Bastos, Ramila Alencar, Lucas Bianchi, Raul Capellan, Xiang Chen, Oswaldo Cruz, Americo Cunha Jr., Haridas K Das, Chloe Fletcher, Raquel Martins Lana, Rachel Lowe, Daniela Luhrsen, Giovenale Moirano, Paula Moraga, Lucas M. Stolerman, Fernanda Valente, Claudia Torres Codeco, Flavio Codeco Coelho. Leveraging probabilistic forecasts for dengue preparedness and control: the 2024 Dengue Forecasting Sprint in Brazil. medRxiv 2025.05.12.25327419](https://doi.org/10.1101/2025.05.12.25327419)



## Financial Support: 
Mosqlimate project coordinates the 2025 Sprint with financial support from Wellcome Trust grant number 226088/Z/22/Z. 

**Contact**:
mosqlimate@gmail.com

[^1]: <http://mosqlimate.org/> is hosting this modeling initiative.
[^2]: Probable dengue cases = reported cases - discarded cases. They include both confirmed cases and cases under investigation.

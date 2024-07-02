## Indicative data use cases for Resilient Kerala

In recent years, the Government of Kerala has invested significantly in data , recognizing it as a critical resource that will advance policy decisions and effect efficient resource-sharing and building amongst the government, businesses and communities.

Currently, there are several platforms that host these open data:
- [Open Government Data Portal of Kerala](https://kerala.data.gov.in/) : intended for use by Departments and Organizations of Government of Kerala to publish datasets, documents, services, tools and applications collected by them for public use.
- [Map Kerala](https://map.opendatakerala.org/) : an Open Data Kerala initiative that hosts downloadable geospatial information for Kerala districts.
- [Kerala State Spatial Data Infrastructure (KSDI)](https://opensdi.kerala.gov.in/): an Internet based Geo-spatial Data Directory for the state that facilitates users of the system to share and explore data related to political and administrative boundaries, natural resources, transportation and infrastructure, demography, agro and socio economy etc., of the state.

The team built several demos to illustrate use cases with open data that industry practitioners and governments can use as part of evidence based policymaking.

## Analysing Heatwaves and Air Quality in Kerala
Using Open Data retrieved from public platforms, the team studied the impact of heatwaves and air quality in Kerala, specifically in Kochi (also known as Cochin) and Trivandrum (also known as Thiruvananthapuram).

Air pollution is one of the greatest environmental risk to health, contributing to respiratory and cardiovascular diseases, cancer, and premature death. Heatwaves, on the other hand, impact human health through heat-related illnesses such as heatstroke, dehydration and heat exhaustion.
In addition to health impacts, air pollution and heatwaves can lead to droughts, wildfires, displacement and migration, having environmental, economic and social impacts as well.
Tracking heatwaves and air pollution levels can help governments and policy makers make informed policies and decisions to improve public and environmental health.

## Who is this for
Data Scientists, Public Health Officials, Emergency Responders, Policy Makers, Urban Planners and Local Government Officials, Environment Scientists and Researchers, General Public.

## How will this work
The analysis will be presented in the form a Data Good that can replicated and reused in other geographic contexts as well. More about data goods [here](https://datapartnership.org/heatwaves-in-india/docs/introduction_to_data_goods.html).

## Future Work

This work is a demonstration of what we could do with currently available open access data. In the forthcoming versions, it can be expanded in multiple ways.

### I. Understanding Impact of Heat in Cities of Kerala

Urban Heat Island (UHI) Effect has known to be the reason for the increased vulnerability of cities to heat risk {cite}`doi:10.1596/40771`. Studying the effect of UHI is critical in mitigation and adaptation to heat risk especially in India, which is considered to be highly vulnerable to it. To this end, the team proposes supplimenting the sample Land Surface Temperature Analysis with a few components -

Component 1: Citizen Science Heat Data Collection Campaigns: Measuring accurate indoor and outdoor temperature can help understand the difference in temperature across schools and hospitals allowing policymakers to take necessary interventions to mitigate impacts. This will also allow for an accurate climate map of the entire city which can become the basis for modelling scenarios under varying climate pathways.

Component 2: Overlaying heat risk with existing sociodemographic information to determine the people and infrastructure most impacted by rising temperatures. This will allow for adaptation interventions to be put in place for neighbrohoods that are worse impacted.

Component 3: Supplimenting data from satellite imagery and remote sensing: The existing analysis from LANDSAt will be supplimented with additional data from Copernicus ERA5, and any other temperature data available through the Indian Space Research Organization. Although satellite imagery is not the most accurate representation of reality, it is a dataset that is easily available, highly granular and can be updated at a high frequency. This makes the data useful once initial calibration is conducted using data obtained through citizen science campaigns.


### II. Understanding Impact of Air Pollution in Kerala

Ambient air pollution poses considerable health risk. Additionally, with rising temperature, citizens would have co-exposure to both heatwaves and high pollution which results in increased risk of morbidity {cite}`rahman2022effects`. Future work can explore different machine-learning models and compare accuracy across models.

<!-- ### III. Understanding Impact of Floods in Kerela
 -->


### IV. Analysing Urban Space Usage

Understanding how populations use urban space is critical for assessing economic activity, societal resilience, and infrastructure accessibility. However, measuring urban space usage at the frequency and granularity required to support these assessments can be challenging, especially when relying only on traditional survey methods. To overcome this challenge, the team proposes using mobility data -- i.e., telemetry data derived from mobile devices – to generate high-frequency indices of urban space usage (e.g., retail centers, construction sites, manufacturing zones, financial centers, residential areas, etc.).  This data can be used to deisgn two components -

Component 1: Methodological Research to Measure Urban Space Usage: The team will develop a methodology for processing and analyzing mobility data to generate urban space activity level indicators, or “index”. The output will be a detailed methodological guide that can be replicated in varied contexts and a suite of interactive visualizations that communicate mobility patterns and their correlations with economic indicators. The index will support informed urban planning and design decisions, particularly in relation to climate resilience.


Component 2: Urban Climate Shock Response Analysis: The team will employ the methodologies and tools developed in the first part, using the Kerala as a case study, to answer research questions around climate-driven shifts in urban space usage, regional comparison of these shifts, correlation between urban space usage and climate shocks, and predictive analysis of future impacts. The research, disseminated in the form of a policy research working paper, will support policy and planning decisions related to urban climate resilience in Kerala. The climate shocks can include floods and heatwaves.

A sample of a similar analysis can be found in the team's work for [Turkiye Earthquake response](https://datapartnership.org/turkiye-earthquake-impact/notebooks/mobility/activity.html#id1).



### References

```{bibliography}
:filter: docname in docnames
```

## License

This project is licensed under the [**Mozilla Public License**](https://opensource.org/license/mpl-2-0/) - see the [LICENSE](LICENSE) file for details.


<!-- ## Strategic Brief

*forthcoming*

<!-- Part of [Understanding the vulnerability of New Delhi to Heatwaves](https://portal.datapartnership.org/readableproposal/368), this repository holds a collection of (experimental) Jupyter notebooks exploring data available through the [Development Data Partnership](https://datapartnership.org). -->

<!-- ## Challenge

Heatwaves could impact the progress made in at least 10 of the 17 SDGs making them a critical, global phenomenon that needs to be addressed collectively and with urgency. Unlike sudden-onset disasters, heatwaves do not come with the drama of flying roofs and flooded streets. On the contrary, they are silent killers that trigger cascading impacts on agriculture, food security, healthcare, education, employment, energy, water supply, urban resilience, and human development. In 2022 alone, extreme heat has been the leading cause of crop failures in India, hydropower shortages in China, and exacerbated flooding in Pakistan through accelerated melting of glaciers. However, even within the same country, these impacts are not felt by every person and every sector equally. To inform targeted policy interventions that alleviate the impact of extreme heat, it is important to assess the vulnerability of different sectors to extreme heat at a granular scale, using a standardized methodology.

Currently, there is no standardized methodology to define or assess the impacts from heatwaves. Each meteorological department uses their own dataset and definition to estimate heatwaves and often do not differentiate the definition of a heatwave between people and crops. Impact from natural disasters is often measured in terms of number of deaths, number of people impacted, and economic losses caused by it. Such a methodology cannot be applied to heatwaves because it is a slow-onset disaster and the impacts from it are not felt immediately after the event.

## Proposed Solution

The team proposes the use of different definitions of heatwaves applicable to crops and people separately. These definitions will allow for the monitoring of impacts in different sectors differently. The impact can be measured across the sectors of health, electricity, water, agriculture, and the economy using a standard set of indicators (listed below).

One important impact of heatwaves is the triggering of cascading natural disasters – floods and droughts. To account for this, two indicators are identified. These two indicators allow for the spatial mapping of areas that are flood-prone and drought-prone due to heatwaves, thus making them more vulnerable.

The following indicators are proposed to assess the impact of heatwaves across sectors - The following indicators will be calculated at the granularity of the lowest administrative boundary data available, preferably a city. The impact will be measured between the years 2015 and 2022. -->

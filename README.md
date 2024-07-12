# Download
Below you'll find information about data granularity, structure and update cycle, time stamps and time intervals as well as on column separators, decimal dividers and missing values.

<!-- cf. https://opendatadocs.dmi.govcloud.dk/en/Download -->

## Data granularity
For all types of data MeteoSwiss uses standard granularities. Depending on the application not all granularites are available. 

For [*Ground-based* Measurements](https://github.com/MeteoSwiss/opendata/tree/main?tab=readme-ov-file#a-ground-based-measurements) the lowest granulartiy is usually called 'raw data' (Rohwert) or 'original data' (Originalwert). Higher granularities are called 'aggregations' or 'aggregated values'. The World Meteorological Organization (WMO) does issue guidelines on how national weather services have to aggregate values and MeteoSwiss does follow these guidelines.

If you need hourly, daily, monthly or yearly values, we strongly recommend that you download the according granularity. Downloading the raw data (10min) and calculating sums or means yourself, will not always lead to the same results! Furthermore for historic data it is possible that manual data corrections have only been applied on higher granularities (like hourly or daily data), which means that historic raw data can still contain errors.

This is the overview of the granularities for [Ground-based](https://github.com/MeteoSwiss/opendata/tree/main?tab=readme-ov-file#a-ground-based-measurements) and [Atmosphere Measurements](https://github.com/MeteoSwiss/opendata/tree/main?tab=readme-ov-file#atmosphere-measurements), as well as for [Observations Data](https://github.com/MeteoSwiss/opendata/tree/main?tab=readme-ov-file#observations-data) and [Homogenous Climate Data Series](https://github.com/MeteoSwiss/opendata/tree/main?tab=readme-ov-file#homogenous-data-series) used by MeteoSwiss:

| Granularity | Name | Description | Used for |
| ----------- | ---- | ----------- | -------- |
| T | 10min value | At MeteoSwiss this is the standard granularity for realtime data of the automatic measurement network SwissMetNet (SMN) or the model output. Meteorological observations do also use this granularity but only offer values at fixed intervals like 6UTC, 12UTC and 18UTC (called "Terminwerte")! | [SMN](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-measurement-network.html), [OBS](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-observation-network.html) |
| H | Hourly value | Either aggregated from 10min values or provided by the instrument/network | [Pollen](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/automatic-pollen-monitoring-network-swisspollen.html) |
| D | Daily value | Used throughout the MeteoSwiss measurement network before automatization in 1981 started. Today still used for manual precipitation and snow measurements. For automatic stations daily values are calculated using 10min values according to WMO guidelines. | [NIME](https://www.meteoswiss.admin.ch/weather/measurement-systems/land-based-stations/manual-precipitation-monitoring-network.html) |
| M | Monthly value | Usually aggregated from daily values and widely used in climatology for homogenized data and norm values and for seasonal data. For some very old data series (pre 1864) only monthly data exists!| [Homogeneous data series](https://www.meteoswiss.admin.ch/climate/climate-change/changes-in-temperature-precipitation-and-sunshine/homogeneous-data-series-since-1864.html), [Climate normals](https://www.meteoswiss.admin.ch/climate/the-climate-of-switzerland/climate-normals.html) |
| Y | Yearly value | Usually aggregated from daily values and mostly used in climatology or climate change screnarios. | [Climate change scenarios](https://www.meteoswiss.admin.ch/climate/climate-change/swiss-climate-change-scenarios.html)|

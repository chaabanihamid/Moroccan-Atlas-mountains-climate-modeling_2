# Mountains climate modeling in the context of climate change  
## This project aims to study the Atlas Snow characteristics and trends as simulated by High-Resolution CMIP6 Forced-Atmosphere Runs, compared to reanalysis, remote observations, and in-situ observations. 

First, we collected data for the period 1982-2014 within the Moroccan Atlas domain. The dataset encompasses information on snow cover obtained from reanalyses (ERA5 & ERA5-LAND), outputs from six CMIP6 High-Resolution models, satellite data from ESA CCI, and measured snow depth at six stations: Ifrane, Midelt, Oukaimeden, Tichki, M'goun, and Tizi Touzna. Additionally, precipitation and temperature data were collected from the same sources.

1) The initial pre-processing steps included:
2) Domain Extraction: Defining and isolating the geographical area of interest within the Moroccan Atlas domain.
3) Unit Transformations: Standardizing units across various datasets to ensure uniformity and comparability.
4) Gap-Filling: Gap-filling of missing data in in-situ data and ECA CCI (satellite data).
5) Resampling to Daily: Adjusting the temporal resolution of the data to a daily scale.

Second, we computed monthly snow cover values over land by aggregating daily values. We calculated also the monthly number of days with snow over land applying different thresholds and we extrapolated this number using the linear method to overcome the impact of missing data. We applied an additional constraint as well, which consists of excluding monthly-year-mesh(pixel) where there are more than 15 days without data. Moreover, if it is excluded from one product, it is excluded from all other products. This ensures an equal number of time steps for all products across every mesh (pixel) in the end. We did the same calculation for precipitation and temperature. 

Third, we conducted a detailed comparison. 
The initial comparison was performed at the station level by extracting grid points and pixels closest to the stations. The comparison was based on the number of days with snow, as gridded data provides snow cover, while in-situ data provides snow depth. We relied on a common parameter extracted from both cover and depth, which is the number of days with snow. This comparison was conducted using climatological averages.
The second comparison was carried out across the entire Atlas region and in altitude ranges, using ERA5, ERA5-LAND, and ECA CCI data as references. This comparison was based on the calculation of spatial biases and spatial Root Mean Square Error (RMSE).

Fourth, we explored correlations between land snow biases and biases in precipitation and temperature. We attempted to explain snow biases by analyzing meteorological fields of temperature and precipitation in different altitude ranges.

Fifthly, we explored the inter-annual variability and trends of snow using these data sources.





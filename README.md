---
output:
  pdf_document: default
  html_document: default
---
# American Pika Population and Distribution Trends at Niwot Ridge


## Summary

This repository was created to facilitate data storage and analysis for a research project analyzing the effects of climate change on the American pika at Niwot Ridge, CO. The goal was to understand pika population changes over the past 10-15 years and examine the connection to a changing alpine climate. The prevalence of parasites (mites and fleas) found on pikas was also assessed over time, as an increase in disease is a widely accepted consequence of climate change. 

The repository contains raw and processed data files, metadata, information on the data sources, and code used for wrangling, analysis, and visualization. 



## Investigators

Authors: Jacob Freedman and Logan Dye, Masters of Environmental Management Students at Duke University's Nicholas School of the Environment

jacob.freedman@duke.edu
logan.dye@duke.edu

## Keywords

Pika, climate change, temperature, alpine tundra, disease, parasites, spatial analysis, population analysis


## Database Information

Both climate and pika data was sourced from the Niwot Ridge LTER website on November 27th, 2022. All datasets are for public use and are available here: https://nwt.lternet.edu/data-catalog 

Significant wrangling was required to answer the research questions. The raw pika dataframe  contained information for each pika capture, but through the wrangling process additional dataframes were generated to summarize general trends. This included annual pika counts and average annual flea/mite abundance. The raw climate dataframe included daily observations, but had gaps in the average daily temperature measurements. Interpolation was used to create a new "complete" dataframe which was necessary for calculating accurate mean annual temperature values. 

Although not used in the formal analysis, approximate elevations for the 3 pika sampling locations were determined by using the USGS TNM Elevation Map. https://apps.nationalmap.gov/elevation/



## Folder structure, file formats, and naming conventions 

The Data folder contains both raw pika and climate data files (Data/Raw) and an empty processed data folder (Data/Processed) for a future researcher if they wish to fork our repository. The Code folder contains wrangling and analysis code required to generate the visualizations in the final report. The final report is located in the Output folder.


| File Folder/Name | File Format |
| --- | --- |
| Raw Data | CSV |
| DataWrangling | R Markdown |
| DataAnalysis| R Markdown |
| README | Markdown and PDF |
| Final Report | R Markdown and PDF |


## Metadata

Pika Demography Data at Niwot Ridge

| File/Column Name | Description |
| --- | --- |
| pika_demography.cr.data.csv | Raw Pika Data csv file | 
| LTER_site | Niwot Ridge LTER Site | 
| local_site | WK=west knoll: LL=Long Lake; ML=Mitchell Lake; CG=Cable Gate | 
| date | date | 
| slope_asp | slope-aspect as cardinal direction or FLAT | 
| easting | GPS E-W coordinate as UTM easting | 
| northing | GPS N-S coordinate as UTM northing | 
| tag_type | A = aluminum "rabbit" tag, C = ear-notching code | 
| code_r_ear | color code of right ear  | 
| code_l_ear | color code of left ear | 
| num_r_ear | number of right ear, N = Notch, H = Hole, M = Mangled | 
| num_l_ear | number of left ear, N = Notch, H = Hole, M = Mangled | 
| weight | body weight (g) | 
| stage | A = adult; J = juvenile | 
| sex | sex | 
| repro_status | P = pregnant, L = has lactated this year, T = testes detected by feel, U = no evidence | 
| ear-mites_samp | Whether mites were collected (1=collected, 0=not collected) | 
| ear-mite_obs | Ear mite cover: N = none, L = low (0-4 sq mm), M = medium (4-16 sq mm) or H = high (>16 sq mm) | 
| fleas_samp | number of fleas collected | 
| fleas_obs | number of fleas observed | 
| tissue_samp | tissue sample collected: 1 = collected; 0 = not collected | 
| hair_samp | hair sample collected: 1 = collected; 0 = not collected | 
| urine_samp | urine sample collected: 1 = collected; 0 = not collected | 
| feces_samp_dry | dry pellet fecal sample collected: 1 = collected; 0 = not collected | 
| feces_samp_wet | wet pellet fecal sample collected: 1 = collected; 0 = not collected | 
| feces_samp_cae | caecal fecal sample collected: 1 = collected; 0 = not collected | 
| blood_samp_r-o | blood sample collected via retro-orbital bleeding: 1 = collected; 0 = not collected | 
| blood_samp_ear | blood sample collected from ear: 1 = collected; 0 = not collected | 
| smear | slide with blood smear prepared: 1 = collected; 0 = not collected | 
| nobuto | Nobuto strip saturated with blood: 1 = collected; 0 = not collected | 
| saliva_samp | saliva sample collected with cotton swab: 1 = collected; 0 = not collected | 
| rectal_temp | rectal temperature (C) | 
| neck_circ | circumference of neck (cm) | 
| foot_length | foot length (mm) | 
Table 1. Niwot Ridge pika demography metadata. All pika demography data in the raw dataframe is of class "factor", with the exception of easting and northing, which are of class "integer". Adapted from Niwot Ridge LTER Metadata at https://portal.edirepository.org/nis/metadataviewer?packageid=knb-lter-nwt.8.4


Climate Data at Niwot Ridge

| File/Column Name | Description | Class |
| --- | --- | --- |
| d-1cr23x-cr1000.daily.ml.data.csv | Raw Climate Data csv file | |
| LTER_site | Niwot Ridge LTER site | Factor |
| local_site | C1 site | Factor |
| logger | data logger type (CR23X or CR1000) | Factor |
| date | date (yyyy-mm-dd) | Factor |
| year | year (yyyy) | integer |
| jday | Julian day | integer | 
| airtemp_max | maximum air temperature (C) | numeric |
| flag_airtemp_max | flag for maximum air temperature: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_min | minimum air temperature (C) | numeric |
| flag_airtemp_min | flag for minimum air temperature: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_avg | average air temperature (C) | numeric |
| flag_airtemp_avg | flag for average air temperature: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_max | maximum relative humidity (Percent) | numeric |
| flag_rh_max | flag for maximum relative humidity: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_min | minimum relative humidity (Percent) | numeric |
| flag_rh_min | flag for minimum relative humidity: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_avg | average relative humidity (Percent) | numeric |
| flag_rh_avg | flag for average relative humidity: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| bp_max | maximum barometric pressure (Millibars) | numeric |
| flag_bp_max | flag for maximum barometric pressure: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| bp_min | minimum barometric pressure (Millibars) | numeric |
| flag_bp_min | flag for minimum barometric pressure: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| bp_avg | average barometric pressure (Millibars) | numeric |
| flag_bp_avg | flag for average barometric pressure: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| ws_max | maximum wind speed (m/s) | numeric |
| flag_ws_max | flag for maximum wind speed: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| ws_min | minimum wind speed (m/s) | numeric |
| flag_ws_min | flag for minimum wind speed: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| ws_avg | average wind speed (m/s) | numeric |
| flag_ws_avg | flag for average wind speed: n=no flag; m=missing; q=questionable; e=estimated | Factor | 
| wd | average wind direction (degree) | numeric |
| flag_wd | flag for average wind direction: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| solrad_avg (Watt/m^2)|  | numeric |
| flag_solrad_avg | flag for average solar radiation: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| solrad_tot | total solar radiation (Watt/m^2) | numeric |
| flag_solrad_tot | flag for total solar radiation: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| soiltemp_5cm_avg | average soil temperature at 5cm (C) | numeric |
| flag_soiltemp_5cm_avg | flag for soil temp at 5cm: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| soilmoist_5cm_avg | average soil moisture at 5cm | numeric |
| flag_soilmoist_5cm_avg | flag for soil moisture at 5cm: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_hmp1_max | maximum air temperature sensor 1 (C) | numeric |
| flag_airtemp_hmp1_max | flag for maximum air temperature sensor 1: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_hmp1_min |  q=questionable; e=estimated	minimum air temperature sensor 1 (C) | numeric |
| flag_airtemp_hmp1_min | flag for minimum air temperature sensor 1: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_hmp1_avg | average air temperature sensor 1 (C) | numeric |
| flag_airtemp_hmp1_avg | flag for average air temperature sensor 1: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_hmp2_max | maximum air temperature sensor 2 (C) | numeric |
| flag_airtemp_hmp2_max | flag for maximum air temperature sensor 2: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_hmp2_min | minimum air temperature sensor 2 (C) | numeric |
| flag_airtemp_hmp2_min | flag for minimum air temperature sensor 2: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_hmp2_avg | average air temperature sensor 2 (C) | numeric |
| flag_airtemp_hmp2_avg | flag for average air temperature sensor 2: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_hmp3_max | maximum air temperature sensor 3 (C) | numeric |
| flag_airtemp_hmp3_max | flag for maximum air temperature sensor 3: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_hmp3_min | minimum air temperature sensor 3 (C) | numeric |
| flag_airtemp_hmp3_min | flag for minimum air temperature sensor 3: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| airtemp_hmp3_avg | average air temperature sensor 3 (C) | numeric |
| flag_airtemp_hmp3_avg | flag for average air temperature sensor 3: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_hmp1_max | maximum relative humidity sensor 1 (Percent) | numeric |
| flag_rh_hmp1_max | flag for maximum relative humidity sensor 1: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_hmp1_min | minimum relative humidity sensor 1 (Percent) | numeric |
| flag_rh_hmp1_min | flag for minimum relative humidity sensor 1: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_hmp1_avg | average relative humidity sensor 1 (Percent) | numeric |
| flag_rh_hmp1_avg | flag for average relative humidity sensor 1: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_hmp2_max | maximum relative humidity sensor 2 (Percent) | numeric |
| flag_rh_hmp2_max | flag for maximum relative humidity sensor 2: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_hmp2_min | minimum relative humidity sensor 2 (Percent) | numeric |
| flag_rh_hmp2_min | flag for minimum relative humidity sensor 2: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_hmp2_avg | average relative humidity sensor 2 (Percent) | numeric |
| flag_rh_hmp2_avg | flag for average relative humidity sensor 2: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_hmp3_max | maximum relative humidity sensor 3 (Percent) | numeric |
| flag_rh_hmp3_max | flag for maximum relative humidity sensor 3: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_hmp3_min | minimum relative humidity sensor 3 (Percent) | numeric |
| flag_rh_hmp3_min | flag for minimum relative humidity sensor 3: n=no flag; m=missing; q=questionable; e=estimated | Factor |
| rh_hmp3_avg | average relative humidity sensor 3 (Percent) | numeric |
| flag_rh_hmp3_avg | flag for average relative humidity sensor 3: n=no flag; m=missing; q=questionable; e=estimated | Factor |
Table 2. Niwot Ridge climate metadata. Adapted from Niwot Ridge LTER Metadata at https://portal.edirepository.org/nis/metadataviewer?packageid=knb-lter-nwt.402.5

## Scripts and code

All code required for generating the visualizations in the final report is contained in the Code folder. Code is divided into Data Wrangling and Data Analysis Rmd files. 

## Quality assurance/quality control

Although no formal QA/QC analysis was conducted, pika demography data was initially examined to account for equal sampling effort between years. Each year contained at least one bout per Niwot Ridge location (West Knoll, Long Lake, Mitchell Lake) and no year contained a large enough number of captures to be considered an outlier. Missing temperature data was replaced using interpolation rather than excluding values outright, because it was clear the timeline of the missing data was not consistent between years. For example, 2012 was missing a large portion of summer temperatures while 2018 contained all temperatures.  
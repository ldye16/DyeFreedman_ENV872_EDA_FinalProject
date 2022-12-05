---
output:
  pdf_document: default
  html_document: default
---
# DyeFreedman_ENV872_EDS_FinalProject
This repository is for the Final Project of Environmental Data Analytics. 



Topic: We are examining Pika demography and climate data from the Niwot Ridge LTER site. Our goal is to understand Pika distribution changes over the past 10-15 years and examine whether there is any connection to the changing alpine climate. We also will investigate the prevalence of pests (mites and fleas) over time. Pika rely on alpine tundra, a habitat severely threatened by climate change, so understanding the population changes would be valuable for future species outlook.

## Summary

<describe the purpose of this repository, the information it contains, and any relevant analysis goals. What, why, where, when, how?>

This repository was created to facilitate data storage and analysis for a research project analyzing the effects of climate change on the American pika at Niwot Ridge, CO. The goal was to understand Pika distribution changes over the past 10-15 years and examine the connection to a changing alpine climate. The prevalence of pests (mites and fleas) found on pikas was also assessed over time, as an increase in disease is a widely accepted consequence of climate change. 

The repository contains raw and processed data files, metadata, information on the data sources, and code used for analysis and visualization. 



## Investigators

<name(s), affiliation(s), contact information, roles (if applicable)>

Authors: Jacob Freedman and Logan Dye

## Keywords

<add relevant keywords here>

Pika, climate change, temperature, alpine tundra, disease, spatial analysis, population analysis

## Database Information

<describe the origin of all data in the repository, including data collected from outside sources and new data generated by the investigator(s). If data was accessed from an outside database, the date(s) of data access should also be included.>

Both climate and pika data was sourced from the Niwot Ridge LTER website on November 27th, 2022. All datasets are for public use and are available here: https://nwt.lternet.edu/data-catalog Significant wrangling was required to answer the research questions. 


## Folder structure, file formats, and naming conventions 

<describe the folders contained in the repository, including what type of files they contain>

<describe the formats of files for the various purposes contained in the repository>

<describe your file naming conventions>

## Metadata

<For each data file in the repository, describe the data contained in each column. Include the column name, a description of the information, the class of data, and any units associated with the data. Create a list or table for each data file.> 

Metadata: Pika Demography Data at Niwot Ridge

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




Metadata: Climate Data at Niwot Ridge

| File/Column Name | Description |
| --- | --- |
| d-1cr23x-cr1000.daily.ml.data.csv | Raw Climate Data csv file | 
| NTL-LTER_Lake_Carbon_Raw.csv | NTL LTER Lake: Carbon data | 

## Scripts and code

<list any software scripts/code contained in the repository and a description of their purpose.>

## Quality assurance/quality control

<describe any relevant QA/QC procedures taken with your data. Some ideas can be found here:>
<https://www.dataone.org/best-practices/develop-quality-assurance-and-quality-control-plan>
<https://www.dataone.org/best-practices/ensure-basic-quality-control>
<https://www.dataone.org/best-practices/communicate-data-quality>
<https://www.dataone.org/best-practices/identify-outliers>
<https://www.dataone.org/best-practices/identify-values-are-estimated>
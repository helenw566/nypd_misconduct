## NYPD Misconduct

Helen Wang (@helenw566, email: hw566@georgetown.edu)

#### Abstract

> Capital Bikeshare was first implemented in the metropolitan DMV area in 2010 as an alternative transit option for residents. In our study, we assessed the impact of opening such a station on local traffic volume. Using traffic APIs and station coordinates, we obtained Annual Average Daily Traffic (AADT) from monitors around each Bikeshare station between the years of 2007-2019. Using 2013 as the reference year, we limited our sample to the 78 stations that opened that year and evaluated change in AADT 6 years pre- and post-station opening. Using OLS, we observed no significant effects, however, panel data analysis with entity effects found significant reductions in traffic volume, with opening a station being linked to a 9% reduction in AADT. A two-way fixed effect model with time effects included, on the other hand, suggested that opening a station did not affect traffic volume. As such, the current results of the study are inconclusive and require further investigation. Limitations of the study include the need to control for confounding factors such as population density and public transit infrastructure changes. The scarcity of the granular geolocation and time data needed for such changes remain prominent challenges for future work.

#### Reposiory Contents

This repository contains the following folders: 

- data
  - cleaned_data
  - raw_data
- proposal
- scripts
- visualizations
  - tables
  - graphs
 - report

 Descriptions of folder contents can be found below.

 #### Data

This folder contains all the data files we used to conduct our analysis. Specifically, the raw_data folder contains all the raw, uncleaned data utilized in our study. We include in this folder the following:

 - "county_shape_file_zipped" and "dc_shape_file_zipped": The zipped files of the Shapefiles utilized in our study, namely the 2024 County and Equivalent National shapefile as well as the 2024 Census Tract shape files for the District of Columbia
 - "opened_capital_bikes_proposed.xlsx": The .xlsx file for the Capital Bikeshare Expansion Plans
 - "capital_bike_locations.geojson": The .geojson file contain the location of all Capital Bikeshare Locations

We do not include the traffic volume data here because they were extracted from an API (data is in cleaned_data below). The size of the Capital Bikeshare Trip history .csvs are too large for Github so we attached a file ("trip_history_data_links.md") containing the links to the raw dataset.

The cleaned_data folder contains all the datafiles we cleaned throughout the project, including:

- "opened_capital_bikes.csv": This .csv contains the merged Capital Bikeshare Location data as well the opening year variable constructed from the Capital Bikeshare Trip History data
- "opened_cb_traffic.csv": This .csv contains the results of "opened_capital_bikes.csv" merged with data extracted from the Traffic API. It contains all the traffic volume data for all capital bikeshare stations that are opened as of 2024
- "unopened_cb_traffic.csv": This .csv contains the results of "opened_capital_bikes_proposed.xlsx" merged with data extracted from the Traffic API. It contains allt the traffic volume data for proposed capital bikeshare stations.
- "final_data.csv": This .csv contains contains the result of merging "opened_cb_traffic.csv" with "unopened_cb_traffic.csv"

#### Proposal

This folder contains a .pdf file of the original Project Proposal that launched this project

#### Scripts

This folder contains all the .ipynb files used to clean the data, run analyses, and create visualizations. Here are the descriptions of the purpuses and outputs of each script:

- "01_cleaning_capital_bikeshare.ipynb": This script extracts the data from "capital_bike_locations.geojson" and computes the opening year from the Trip History data before mergining the files together. This produces the "opened_capital_bikes.csv" file.
- "02_cleaning_traffic.ipynb": This strip takes in "opened_capital_bikes.csv" and uses it to query the Traffic API. It produces the following files: "opened_cb_traffic.csv" and "unopened_cb_traffic.csv"
- "03_merging_data.ipynb": This script merges "opened_capital_bikes.csv" and "opened_cb_traffic.csv" to create "final_data.csv"
- "04_data_analysis.ipynb": This script contains all the code used to run our analysis, including our OLS models and Panel Data Anlysis. It produces all the latex tables stored in \visualisations\tables as well as some of the regression graphs in \visualizations\graphs
- "05_visualizations.ipynb": This script contains the code used to create MOST but not all of our visualizations in \visualizations\graphs. This constructs most of our maps, basic linegraphs, and bar graphs.
- "06_proposed_stations.ipynb": This script runs the descriptive analysis used to construct on our policy recommendations. It also produces one of the visualizations present in \visualizations\graphs

#### Visualizations

This folder contains all of the tables and visualizations producted in our analysis. They are separated into the following folders:

 - tables: This contains all of our latex tables
 - graphs: This contains all of our maps, line graphs, and bar graphs

#### Report

This folder contains a .pdf of our final report that was producted in Overleaf Latex.

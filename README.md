## Predicting NYPD Misconduct Case Outcomes and Penalties

Helen Wang (@helenw566, email: hw566@georgetown.edu)

#### Abstract

> The issue of police misconduct is important, especially given rising cases of police violence, police brutality, and fatalities as a result of such misconduct. Such issues have resulted in the loss of multiple lives, increased racial tensions across the US, and fractured public trust in law enforcement. The literature has explored various factors linked to police misconduct and has similarly evaluated predictors of not only future misconduct but also misconduct case outcomes. Few studies, however, have accounted for the impact of media coverage on police misconduct. Those who do have primarily limited their analysis to the impact of media coverage on public perceptions of police misconduct. No article to date has assessed the role that the media can play in influencing misconduct case outcomes, despite the potential pressure that media can have on ensuring that sufficient sanctions are levied. To address this gap, in this study, we will utilize a dataset of police misconduct cases drawn from the New York City Police Department (NYPD) to do the following:
> 1.	Develop supervised models to predict case and penalty outcomes for police misconduct cases.
> 2.	Assess the impact that media coverage/visibility of a given police misconduct incident has on its case outcome, specifically its complaint disposition, as well as the resulting penalty.
> 3.	Identify and verify the factors most predictive of police misconduct case outcomes as well as penalty outcomes.


#### Repository Contents

This repository contains the following folders: 

- `data`
- `paper`
- `scripts`
- `slides`

 Descriptions of folder contents can be found below.

 #### Data

This folder contains the cleaned data utilized for this study, the raw police misconduct data, as well as data collected via NYT scraping.

We primarily drew data from three sources:

- [NYPD Civilian Complaint Review Board (CCRB) Database](https://data.cityofnewyork.us/browse?Data-Collection_Data-Collection=CCRB+Complaints+Database&sortBy=relevance&pageSize=20&page=1), which contains the following datasets
  - Allegations Against Police Officers: a list of all closed allegations made against NYPD officers, including information about the complainant, the officer, allegation, and resulting deposition 
  - Complaints Against Police Officers: a list containing information such as dates, locations, and circumstances surrounding the allegation 
  - Police Officers: a list of all NYPD officers and the number of total and substantiated complaints on their record 
  - Penalties: a list containing case and trial penalty information
- [Mapping Police Violence Project](https://airtable.com/appzVzSeINK1S3EVR/shroOenW19l1m3w0H/tblxearKzw8W7ViN8), which used google alerts to get news articles on police violence events to construct their dataset
- [New York Times API](https://developer.nytimes.com/docs/articlesearch-product/1/overview), to scrape for relevant news articles on the officers and their associated misconduct cases. 


#### Paper

This folder contains .docx and .pdf files for all stage submissions for the final paper of the project as well as the final report generated. Written for PPOL5204: Data Science II: App Stat Lng at Georgetown

#### Scripts

This folder contains all the .ipynb and resulting html files used to scrap data, preprocess, and run analyses. Here are the descriptions of the purpuses and outputs of each script:

- `01_preprocessing`: This script takes in the raw data, merges it, preprocesses it, and runs initial descriptive analysis before producing cleaned_data.csv
- `02_news_data`: This stript scrapes the NYT Article API for news hits and produces a data file that is then merged into cleaned_data.csv in "01_preprocessing.ipynb"
- `03_modeling`: This script conducts initial SMOTE and initial model selection as well as hyperparameter tuning.

#### Slides
This folder contains a .pdf file of a brief slide deck summarizing the project.


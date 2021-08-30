# ITMoB Training Seminar Series #1: Modeling on Population Distribution Projection for Scenario Analysis
ITMoB launched a series of open online training seminars as an opportunity for technical capacity building.
The first training seminar on population distribution modeling will be organized on 3rd September.
The program is designed for researchers and students who want to obtain the modeling skills for scenario analysis on population distribution.

Date: 3rd September (Friday)

Time: 15:00-17:00 in Japan time（14:00-16:00 in Philippines time, 13:00-15:00 in Western Indonesian time）

Venue: Zoom (the link will be sent few days before to registered emails)

Language: English

Fee: Free

Information: https://supportoffice.jp/eAsia2021/events/

# Requirements
## Hardware
- 64 bit OS
  - Windows 10
  - Mac (Intel / M1)
- PC memory >= 8GB
- Storage >= 10GB
## Software
- R >= 4.0.0
  - see, https://rstudio-education.github.io/hopr/starting.html
  - download "R" and "R-studio" matching to the specification of your PC
- Excel >= 2010


# Advanced preparation by Sep. 03 JST 15:00
### 1. Data download

### 2. Install R & Rstudio
- download "R" and "R-studio" matching to the specification of your PC
  - Follow the instruction of https://rstudio-education.github.io/hopr/starting.html


### 3. Excel 'Development' ribbon activation
-  open 'file'.
-  click 'Enable Content' at the SECURITY WARNING bar ![image](https://user-images.githubusercontent.com/85103588/130731917-cbc33026-c8df-4d54-a78b-af0b690ad617.png)
-  go to 'File' tab -> select 'Options' ![image (1)](https://user-images.githubusercontent.com/85103588/130732218-0f7416dc-90fe-4c15-aded-988d790f650f.png)
-  go to "Customize Ribbon" -> check the ribbon named "Developer" in Main Tabs ![image (2)](https://user-images.githubusercontent.com/85103588/130732311-a6f9f6aa-5bdc-4b28-84b8-eee022dbec16.png)


# Agenda
<img width="708" alt="image" src="https://user-images.githubusercontent.com/85103588/131284597-7c278e28-c088-4c9a-a8ba-ff3a6d8eb6ff.png">

## The 1st session：Presentation about population distribution modeling
### 15:00-15:10 (JST) Opening remarks and introduction of e-Asia (Dr. Osamu Saito, IGES)
### 15:10-15:20 (JST) Population scenario development (Dr. Takanori Matsui, Osaka Univ.)
#### IPBES conceptual framework (https://ipbes.net/conceptual-framework)
![image](https://user-images.githubusercontent.com/85103588/131281250-a924758c-4c14-4dd1-b8f6-5a321080b7c6.png)

#### PANCES simulation system for describing socio-ecological systems (http://pances.net/eng/theme1.html)
![image](https://user-images.githubusercontent.com/85103588/131280906-b1e1aa83-6557-47eb-925d-c4ddb95ff9e1.png)

#### PANCES scenarios (https://link.springer.com/article/10.1007/s11625-017-0475-8)
![scenario](https://user-images.githubusercontent.com/85103588/131283167-edb2d7bb-113b-4dbc-9f7c-7c9cd6a7a676.png)

#### Training series
![series](https://user-images.githubusercontent.com/85103588/131282667-214efa7e-e0e7-41ac-8070-d716a618b233.png)




### 15:20-15:35 (JST) Development and application of gravity-based population allocation model (Dr. Chihiro Haga, Osaka Univ.)
#### https://link.springer.com/article/10.1007%2Fs11625-018-0605-y
- What is gravity model?
- Residential population distribution assumption of Compact & Dispersed scenarios
- Application: Overlay the future gridded population and socio-ecological status
### 15:35-15:40 (JST) Q&A

### 15:40-15:55 (JST) Development and application of combined model by cohort-component method and gravity-based method (Dr. Keiko Hori, IGES)
#### https://link.springer.com/article/10.1007%2Fs11625-020-00835-5

### 15:55-16:00 (JST) Q&A

## The 2nd session：Demonstration of scenario analysis on grid population
### 16:05-16:45 (JST) Scenario simulation of grid population by gravity model will be demonstrated
- Indonesian data will be used as sample data from open data source 
- Participants can experience the same simulation with shared dataset and codes

#### 16:05-16:20 (JST) Step 1. Preprocessing population data (Haga)
- Data: Age and sex structures provided by [WorldPop](https://www.worldpop.org/geodata/listing?id=87)
- Processing in R & Rstudio
    1. Install & Load libraries
    1. Initialize parameters
    1. Read province & builtup area maps (in *step1_preprocessing_pop/data* folder)
    1. Iterate for each age & sex category
        1. Read population data (in *step1_preprocessing_pop/data/idn_westjawa* folder)
        1. Mask the population data within the west jawa province
        1. Remove non-residential area
        1. Compute proportion
        1. Save the raster data as dataframe in CSV format
    1. Merge all CSVs into one CSV file (*./output/step1_output_westjawa_cohort_data.csv*)
#### 16:20-16:35 (JST) Step 2. Calculate future population scenario (Hori & Haga)

#### 16:35-16:45 (JST) Step 3. Visualize & compare scenarios (Haga)
- Processing in R & Rstudio
    1. Install & Load libraries
    1. Initialize parameters
    1. Read the province map
    1. Iterate for each scenario
        1. Read the calculated population scenario from excel file (*step2_generate_future_pop_scenarios/ScenarioProj_Model.xlsm*)
        1. Add longitude & latitude information
        1. Rasterize the future population data
        1. Save the raster data
    1. Visualize the raster data

## 16:45-16:55 (JST) Q&A, feedbacks from participants
## 16:55-17:00 (JST) Closing remarks（Dr. Osamu Saito）


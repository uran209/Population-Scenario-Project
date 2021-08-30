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
### Excel 'Development' ribbon activation
-  open 'file'.
-  click 'Enable Content' at the SECURITY WARNING bar ![image](https://user-images.githubusercontent.com/85103588/130731917-cbc33026-c8df-4d54-a78b-af0b690ad617.png)
-  go to 'File' tab -> select 'Options' ![image (1)](https://user-images.githubusercontent.com/85103588/130732218-0f7416dc-90fe-4c15-aded-988d790f650f.png)
-  go to "Customize Ribbon" -> check the ribbon named "Developer" in Main Tabs ![image (2)](https://user-images.githubusercontent.com/85103588/130732311-a6f9f6aa-5bdc-4b28-84b8-eee022dbec16.png)

### Data download
-  


# Agenda
## The 1st session：Presentation about population distribution modeling
---
### 15:00-15:10 (JST) Opening remarks and introduction of e-Asia (Dr. Osamu Saito, IGES)
### 15:10-15:20 (JST) Population scenario development (Dr. Takanori Matsui, Osaka Univ.)
- Integrated Assessment model vs. Technical model for describing socio-ecological systems
- PANCES scenarios
- PANCES simulation flow
- The role of population scenario
### 15:20-15:35 (JST) Development and application of gravity-based population allocation model (Dr. Chihiro Haga, Osaka Univ.)
- What is gravity model?
- Residential population distribution assumption of Compact & Dispersed scenarios
- Application: future population & socio-ecological status
### 15:35-15:40 (JST) Q&A

### 15:40-15:55 (JST) Development and application of combined model by cohort-component method and gravity-based method (Dr. Keiko Hori, IGES)

### 15:55-16:00 (JST) Q&A

## The 2nd session：Demonstration of scenario analysis on grid population
---
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
        1. Read the calculated population scenario from exel file (*step2_generate_future_pop_scenarios/ScenarioProj_Model.xlsm*)
        1. Add longitude & latitude information
        1. Rasterize the future population data
        1. Save the raster data
    1. Visualize the raster data

---
## 16:45-16:55 (JST) Q&A, feedbacks from participants
## 16:55-17:00 (JST) Closing remarks（Dr. Osamu Saito）


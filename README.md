# Fatal Police Shootings Analysis (2015-present)

![Heatmap of Shootings by State](outputs/figures/heatmap.png)  

## 📌 Overview
This project examines patterns and factors associated with fatal police shootings in the United States using comprehensive data analysis and statistical modeling techniques. By exploring geographical distributions, demographic patterns, situational characteristics, and temporal trends, we identify key factors that influence these incidents and classify police departments based on their patterns of fatal shootings.


## Table of Contents
- [Data Source](#data-source)
- [Project Objectives](#project-objectives)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Repository Structure](#repository-structure)
- [Setup and Requirements](#setup-and-requirements)
- [Contributors](#contributors)

## Data Source
The analysis utilizes data from the Washington Post's Fatal Police Shootings Database, which documents all fatal encounters involving law enforcement in the United States since 2015.

Source: [Washington Post Police Shootings Database](https://github.com/washingtonpost/data-police-shootings/blob/master/v2/README.md)

### Key Variables
- **id**: Unique identifier for each incident
- **date**: Date of the incident
- **threat_type**: Type of threat perceived by officers
- **flee_status**: Whether and how the person was attempting to flee
- **armed_with**: Weapon or item the individual was armed with
- **location data**: City, county, state, latitude, and longitude
- **demographic information**: Name, age, gender, and race of the deceased
- **race_source**: Origin of racial classification information
- **was_mental_illness_related**: Indicator for mental illness involvement
- **body_camera**: Indicator for body camera usage
- **agency_ids**: Identifiers for law enforcement agencies involved

## Project Objectives
1. Explore the distribution and patterns of fatal police shootings across geographic, demographic, and situational dimensions
2. Identify key factors associated with these incidents
3. Classify police departments based on their shooting patterns using hierarchical clustering
4. Analyze temporal patterns and trends in fatal shootings

## Methodology
1. **Data Cleaning and Preprocessing**: Handling missing values using multiple imputation approaches
2. **Exploratory Data Analysis**: Visualizing patterns across geographic, demographic, and situational dimensions
3. **Hierarchical Clustering**: Categorizing police departments based on shooting patterns
4. **Survival Analysis**: Examining factors influencing the timing and frequency of shootings

## Key Findings
- **Geographic Variation**: Significant differences in shooting frequency across states
- **Demographic Patterns**: Disproportionate impact on certain racial groups when adjusted for population
- **Body Camera Usage**: Only about 17% of incidents involved officers wearing body cameras
- **Department Typology**: Police departments cluster into three distinct groups:
  - Cluster 1: Moderate shooting counts with predominantly white victims
  - Cluster 2: High shooting counts with diverse victim demographics
  - Cluster 3: Lower shooting counts with predominantly Black victims

## Repository Structure
```plaintext
📦 fatal-police-shootings-analysis
├── 📂 data
│   ├── csv                  # Original data (CSV/JSON)
├── 📂 scripts
│   ├── 📄 coding.rmd
├── 📂 outputs
│   ├── 📂 figures               # Saved plots (PNG/SVG)
├── 📂 docs
│   ├── 📄 presentation.pdf
│   └── 📄 report.pdf
├── 📄 .gitignore
├── 📄 requirements.txt
├── 📄 LICENSE
└── 📄 README.md
```

## Setup and Requirements
This analysis was conducted in R. The following packages are required:

```r
# Required packages
packages <- c(
  "tidyverse",   # Data manipulation
  "ggplot2",     # Visualization
  "maps",        # Geographic mapping
  "cluster",     # Hierarchical clustering
  "factoextra",  # Clustering visualization
  "survival",    # Survival analysis
  "survminer"    # Survival visualization
)

```

## Contributors
- [Suleiman Saka](https://github.com/sakasuleiman)
- [Yousra Shleibik](https://github.com/YourGitHubUsername)
- [Elijah Alabi](https://github.com/YourGitHubUsername)

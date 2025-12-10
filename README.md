# MegaCollision Project
## Data Engineering Project - Motor Vehicle Collisions Analysis

## Overview

This project implements a comprehensive data engineering solution for analyzing motor vehicle collision data from three major US cities: **New York, Chicago, and Austin**. The solution includes data ingestion, transformation, warehousing, and business intelligence capabilities to provide actionable insights into traffic safety patterns.

## 🎯 Project Objectives

- Design and implement a scalable data architecture for traffic collision analysis
- Create a unified data model across multiple city datasets
- Provide business intelligence capabilities for traffic safety insights
- Address data quality issues and standardize heterogeneous data sources

## 📊 Data Sources

The project integrates crash data from official city data portals:

- **[New York City](https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95/about_data)** - Motor Vehicle Collisions dataset
- **[Chicago](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if/about_data)** - Traffic Crashes dataset  
- **[Austin](https://data.austintexas.gov/Transportation-and-Mobility/Austin-Crash-Report-Data-Crash-Level-Records/y2wy-tgr5/about_data)** - Austin Crash Report dataset

## 🛠️ Technology Stack

### Core Technologies
- **ETL Platform**: Talend Data Integration
- **Databases**: Azure SQL Server, MySQL, SQL Server
- **Data Profiling**: Alteryx, YData Profile
- **Visualization**: Tableau, Power BI
- **Data Modeling**: Star Schema Dimensional Modeling

### Development & Infrastructure
- **Version Control**: Git/GitHub
- **Documentation**: Markdown, PDF
- **Data Formats**: CSV, Excel, SQL
- **Cloud Platform**: Azure (for database hosting)
- **Operating System**: Cross-platform (Windows, macOS, Linux)

### Data Engineering Tools
- **Data Quality**: Built-in Talend data validation
- **Data Transformation**: Talend Data Mapper
- **Metadata Management**: Talend Metadata Manager
- **Job Orchestration**: Talend Job Server
- **Monitoring**: Talend Administration Center

### Project Structure
```
MegaCollision/
├── TALEND FILES/Job Designs/DAMG7370_GROUP2/
│   ├── metadata/          # Connection configurations
│   ├── process/           # ETL job designs
│   │   ├── Stage_Tables/  # Data staging jobs
│   │   ├── Date_DIM/      # Date dimension processing
│   │   ├── Time_DIM/      # Time dimension processing
│   │   ├── Geo_DIM/       # Geographic dimension processing
│   │   ├── Accident_Fact/ # Fact table processing
│   │   └── References/    # Lookup tables and mappings
│   └── talend.project
├── DDL.sql               # Database schema definitions
├── datasets.pdf          # Data profiling documentation
└── DOCUMENTATION.pdf     # Comprehensive project documentation
```

## 🔄 Project Phases

### Phase 1: Data Profiling and Staging
- **Data Profiling**: Comprehensive analysis using Alteryx and YData Profile
- **Staging Environment**: Azure SQL Server/MySQL staging tables
- **Dimensional Model Design**: Star schema with facts and dimensions

### Phase 2: Data Integration and Transformation
- **ETL Implementation**: Talend jobs for staging to integration layer
- **Data Validation**: Quality checks and row rejection handling
- **Business Intelligence**: Query development for analysis questions

### Phase 3: Visualization and Reporting
- **Dashboard Creation**: Tableau and Power BI visualizations
- **Insight Delivery**: Actionable business intelligence reports

<span style="color:red">
To view the PowerBI dashboard, could you please request access? I’ll approve it as quickly as possible 🙂

[View the live PowerBI dashboard](https://app.powerbi.com/groups/me/reports/ab58b540-b155-48df-a196-bdbfaf01c224/ReportSection?ctid=a8eec281-aaa3-4dae-ac9b-9a398b9215e7&experience=power-bi&bookmarkGuid=1cb3be2c-c0fd-48a8-b99c-6a971ad80f5b)

In the meantime, you can view the exported dashboard here:  
[PowerBI Dashboard (PPT Export)](https://github.com/Nishieee/MegaCollision/blob/main/MegaCollision_PowerBI_Dashboards_Export.pptx)
</span>


## 📈 Business Analysis Questions

The project addresses 10 key traffic safety questions:

1. **Accident Volume**: Total accidents per city
2. **High-Risk Areas**: Top 3 accident-prone areas per city
3. **Injury Patterns**: Accidents resulting in injuries
4. **Pedestrian Safety**: Pedestrian involvement rates
5. **Seasonal Trends**: Temporal accident patterns
6. **Motorist Impact**: Motorist injuries and fatalities
7. **Fatal Hotspots**: Top 5 fatal accident areas
8. **Time Analysis**: Day/time accident patterns
9. **Fatality Comparison**: Pedestrian vs. road user fatalities
10. **Contributing Factors**: Most common accident causes

## 🗄️ Data Model

### Star Schema Design
- **Fact Table**: `Accident_facts` - Core metrics (injuries, deaths, units involved)
- **Dimension Tables**:
  - `Time_DIM` - Time-based analysis attributes
  - `Date_DIM` - Date-specific information
  - `Geo_DIM` - Location data (lat/long, street, city, ZIP)
  - `SpeedLimit_DIM` - Speed limit information
  - `Crash_DIM` - Crash-specific details
  - `ContributingFactor_DIM` - Accident contributing factors
  - `Vehicle_DIM` - Vehicle type information
- **Junction Tables**: Many-to-many relationships for factors and vehicles

![Dimensional Model](https://github.com/Nishieee/MegaCollision-Project/blob/main/dimenaional%20model.png)

## 🔧 Data Quality & Transformations

### Chicago Data Issues Resolved
- Missing contributing factors → Specific code mapping
- Multiple contributing factor columns → Merged and normalized
- Inconsistent speed limits (0 values) → Updated to -1
- Combined date/time → Split into separate columns

### New York Data Issues Resolved
- Multiple contributing factor columns → Merged and normalized
- Vehicle type inconsistencies → Standardized classifications
- Missing units involved → Computed from related columns
- Time format standardization → Added seconds component

### Austin Data Issues Resolved
- Vehicle type inference → Computed from available data
- Multiple contributing factor columns → Merged and normalized
- Date/time formatting → Split and standardized to yyyy-mm-dd

## 🚀 Getting Started

### Prerequisites
- Talend Data Integration Studio
- SQL Server/Azure SQL Database
- Tableau Desktop or Power BI

### Setup Instructions
1. Clone the repository
2. Import Talend project from `TALEND FILES/Job Designs/DAMG7370_GROUP2/`
3. Configure database connections in metadata folder
4. Execute DDL.sql to create database schema
5. Run ETL jobs in sequence: Staging → Dimensions → Facts

## 📋 Key Features

- **Multi-City Data Integration**: Unified analysis across NYC, Chicago, and Austin
- **Comprehensive Data Quality**: Addresses real-world data inconsistencies
- **Scalable Architecture**: Star schema design for performance and flexibility
- **Business Intelligence Ready**: Pre-built analysis queries and visualizations
- **Documentation**: Complete project documentation and data profiling reports

## 📄 Documentation

- **DDL.sql**: Complete database schema definitions
- **datasets.pdf**: Data profiling and quality analysis
- **DOCUMENTATION.pdf**: Comprehensive project documentation
- **Screenshots**: ETL job designs and process flows

---

*This project demonstrates end-to-end data engineering capabilities, from raw data ingestion through to actionable business insights, with robust data quality controls and comprehensive documentation.*






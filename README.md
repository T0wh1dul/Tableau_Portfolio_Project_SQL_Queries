#  COVID-19 Global Data Analysis

A data analysis project using SQL and Tableau to explore the global impact of COVID-19. This project focuses on identifying trends in cases, deaths, infection rates, and vaccination coverage across countries and continents.

---

##  Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [SQL Queries Explained](#sql-queries-explained)
- [Key Insights](#key-insights)
- [Tableau Dashboard](#tableau-dashboard)
- [Credits](#credits)

---

##  Project Overview

This project aims to analyze the global spread and impact of COVID-19 using SQL for data exploration and Tableau for visualization. The main goals include:

- Calculating total cases and deaths worldwide
- Identifying countries with the highest death counts
- Determining which countries had the highest infection rates relative to their population
- Analyzing vaccination trends over time

---

##  Data Sources

The data used in this project comes from the COVID-19 dataset provided by [Our World in Data](https://ourworldindata.org/coronavirus).

- **CovidDeaths Table**: Contains daily data on cases, deaths, population, location, continent, and date.
- **CovidVaccinations Table**: Contains vaccination counts and dates for each country.

The data was loaded into SQL Server for processing.

---

## Tools Used

- **SQL Server** – for querying and data transformation
- **Tableau** – for creating interactive dashboards and visualizations
- **GitHub** – for version control and sharing the project

---

## SQL Queries Explained

The analysis is built on several key SQL queries:

### 1. Total Global Cases and Deaths
Calculates global totals and the death percentage:

```sql
SELECT 
  SUM(new_cases) AS total_cases,
  SUM(CAST(new_deaths AS INT)) AS total_deaths,
  SUM(CAST(new_deaths AS INT)) / SUM(new_cases) * 100 AS DeathPercentage
FROM PortfolioProject..CovidDeaths
WHERE continent IS NOT NULL

### Key Insights
The global death percentage is approximately (fill from your data)%.
Country (fill from your data) has the highest total death count.
Country (fill from your data) has the highest percentage of population infected.
Countries with strong vaccination rollout show noticeable drops in infection rates over time.

**Tableau Dashboard
The interactive dashboard visualizes:

Global total cases and deaths

Death percentage by continent

Top 10 countries by death count

Percent of population infected per country

Vaccination rollout trends over time

🔗 View Tableau Dashboard **https://public.tableau.com/app/profile/towhidul.islam8478/viz/COVID19Dashboard_17493884683050/Dashboard1**
**

**Credits**
Data Source: Our World in Data
Author: Towhidul Islam
linkdin: **https://www.linkedin.com/in/towhidul-islam01/**


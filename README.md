# Covid Death and Vaccinations SQL Analysis

## Project Overview

This project aims to analyze and visualize the impact of COVID-19 across different countries and continents. Using data from the PortfolioProject, the analysis explores various key metrics, including total cases, deaths, infection rates, and vaccination progress. The project utilizes SQL queries to provide insights into global and regional trends, helping to understand the effects of the pandemic on public health and identify opportunities for improvement in vaccination efforts.

## Data Sources

The data for this analysis is derived from two main sources:
1. **CovidDeaths** - Contains information on total cases, new cases, total deaths, and the population for various locations.
2. **CovidVaccinations** - Includes data on new vaccinations administered per location.

Both datasets cover various regions, including countries, states, and continents, for the years 2019 onward.

## Key Queries and Insights

### 1. **Initial Data Selection**
   - The project starts by selecting data from the `CovidDeaths` table where the continent is not null. This gives us a clear starting point with relevant data across different continents and countries.

### 2. **Total Cases vs Total Deaths**
   - This query calculates the likelihood of dying from COVID-19 in different countries, showing the death percentage for each location based on total cases and deaths.

### 3. **Total Cases vs Population**
   - This query calculates what percentage of a country’s population has been infected with COVID-19 by comparing total cases to the population.

### 4. **Countries with Highest Infection Rate**
   - By grouping data by country and population, this query identifies countries with the highest COVID-19 infection rates.

### 5. **Countries with Highest Death Count per Population**
   - This query focuses on the countries with the highest number of COVID-19 deaths, providing insights into the mortality burden per location.

### 6. **Analysis by Continent**
   - In this section, the analysis is broken down by continent, identifying regions with the highest death counts per population.

### 7. **Global COVID-19 Numbers**
   - This query provides a global view of the total new cases and deaths, as well as the overall death percentage from new cases worldwide.

### 8. **Total Population vs Vaccinations**
   - This query explores the percentage of the population that has received at least one dose of the COVID-19 vaccine. It uses window functions to calculate a rolling total of vaccinated individuals over time.

### 9. **Using CTEs (Common Table Expressions) for Calculations**
   - This query demonstrates the use of a CTE to perform calculations on partitioned data, providing insights into vaccination trends over time.

### 10. **Using Temp Tables for Calculation**
   - This query creates and populates a temporary table to perform similar calculations, offering a method for storing intermediate results for further analysis.

### 11. **View Creation for Later Visualizations**
   - A view named `PercentPopulationVaccinated` is created to store the data for use in future visualizations. This view tracks the cumulative number of people vaccinated, making it easier to analyze vaccination progress across locations.

## Project Goals

The primary goals of this project are:
- To analyze COVID-19 death and vaccination trends across various regions.
- To assess the infection rates and their impact on different populations.
- To track the progress of vaccination campaigns and their effect on reducing the spread of the virus.
- To provide actionable insights for health authorities and organizations working to mitigate the effects of the pandemic.

## Key SQL Concepts Used

- **Aggregation**: SUM, MAX, and other aggregate functions to summarize data.
- **Window Functions**: `SUM() OVER (PARTITION BY ...)` for cumulative calculations.
- **Common Table Expressions (CTEs)**: Used to simplify complex queries and calculations.
- **Temp Tables**: Used to store intermediate data for further analysis.
- **Views**: Created to store reusable queries for easier data analysis and visualization.

## Conclusion

This project provides valuable insights into the COVID-19 pandemic's progression and the global response through vaccination. By analyzing death rates, infection rates, and vaccination data, we can better understand the impact of COVID-19 and identify the most affected regions and populations. The SQL queries and analyses presented in this project form the basis for deeper insights and informed decision-making in pandemic response efforts.

## Future Enhancements

- Integrating additional datasets for more comprehensive insights (e.g., socio-economic factors, healthcare infrastructure).
- Visualizing the data with charts and graphs to make trends easier to understand for stakeholders.
- Adding predictive models to estimate future trends based on historical data.

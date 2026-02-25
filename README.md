# Texas Real Estate Market Analysis – Descriptive Statistics

## Project Overview

This project analyzes the real estate market in four Texas cities over a 5-year period (2010–2014) using descriptive statistics. The dataset contains monthly data on sales, volume, median price, listings, and months of inventory, allowing for a detailed understanding of market trends and variability.

The analysis includes:
- Variable exploration and classification (quantitative, qualitative)
- Position, variability, and shape indexes calculation
- Class creation and frequency distributions
- Conditional analysis by city, year, and month
- Visualization of trends with `ggplot2` and `gghalves`
- Creation of new variables for mean property price and listings efficacy
- Market insights and strategic recommendations

The study focuses on both descriptive metrics and the practical implications for real estate investment and marketing strategies.


## Business Objective

The goal of this analysis is to provide actionable insights into the Texas real estate market:

- Identify cities and periods with the highest sales growth and volume
- Evaluate the efficacy of listings (sales per 100 active listings)
- Detect seasonal and city-specific trends
- Support investment and strategy optimization in the real estate market

The ultimate objective is to help stakeholders allocate resources efficiently and identify high-potential markets.


## Dataset

The dataset includes 240 monthly observations across four cities:

| Variable | Type | Notes |
|----------|------|-------|
| city | qualitative (nominal) | City name |
| year | quantitative (continuous) | Year of observation |
| month | qualitative (nominal) | Month of observation |
| sales | quantitative (discrete) | Number of sales per month |
| volume | quantitative (continuous) | Total sales volume in millions |
| median_price | quantitative (continuous) | Median price of properties sold |
| listings | quantitative (discrete) | Number of active listings |
| months_inventory | quantitative (continuous) | Number of months of inventory |

New derived variables:
- `mean_price` – Average property price per sale
- `efficacy` – Listings efficacy: sales per 100 active listings


## Exploratory Data Analysis

### Position Indexes

- Calculated using `summary()` for mean, median, min, max, and quantiles.
- Observations indicate a mean of 192 sales/month and mean volume of 31 million USD.
- The listings variable averages 1,738 active listings/month, with a mean inventory of 9 months.

### Variability Indexes

- Interquartile range (IQR), standard deviation (SD), and coefficient of variation (CV) were calculated.
- The variable `volume` shows the highest variability (CV ≈ 54%), whereas `median_price` shows the lowest (CV ≈ 17%).

### Shape Indexes

- Skewness and kurtosis were calculated using the `moments` package.
- Most variables are positively skewed (right-tailed) and slightly platykurtic.
- `months_inventory` is closest to a normal distribution.


## Conditional Analysis

### By City
- Bryan-College Station exhibits the highest listings efficacy (~40% in peak months) and median prices.
- Beaumont and Tyler show moderate efficacy increases over time.
- Wichita Falls remains stable with low efficacy and prices.

### By Year and Month
- Monthly efficacy increases steadily from 2010–2014, with seasonal peaks in spring–autumn.
- City contributions to total sales show seasonal patterns but relatively stable relative weights.


## Visualization Highlights

- **Boxplots & Half-violin plots** – Compare median prices between cities.
- **Line charts** – Track sales and listings efficacy trends over time.
- **Bar plots (stacked & normalized)** – Show monthly and yearly distribution of sales volumes per city.
- **Error bars** – Illustrate variability in listings efficacy by city, year, and month.

These visualizations provide a clear understanding of heterogeneity, seasonal patterns, and investment potential in each city.


## Key Insights

1. **Market trends**
   - Overall increase in sales number and volume across 2010–2014.
   - Median prices remain relatively stable (CV ≈ 17%), suggesting more volume growth than price increase.

2. **Listings efficacy**
   - Bryan-College Station has the highest efficiency and growth potential.
   - Tyler shows growing sales but stable efficacy due to high listings numbers.
   - Beaumont shows moderate growth, while Wichita Falls shows low potential.

3. **Investment recommendations**
   - Focus investments on Bryan-College Station for high growth and limited competition.
   - Tyler is promising but may require marketing optimization.
   - Beaumont is moderate; Wichita Falls has limited opportunities.


## Tech Stack

* R
* RStudio
* dplyr
* ggplot2
* gghalves
* zoo
* moments
* DT


## Project Deliverables

- Cleaned dataset with derived variables (`mean_price`, `efficacy`)
- Descriptive statistics and summary tables
- Plots and charts visualizing trends and variability
- Strategic insights and city-level recommendations

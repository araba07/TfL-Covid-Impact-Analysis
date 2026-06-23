# London Tube Pandemic Resilience Analysis
![pandas](https://img.shields.io/badge/pandas-%2337287B?style=for-the-badge&logo=pandas&labelColor=black)
![python](https://img.shields.io/badge/python-579AC9?style=for-the-badge&logo=python&labelColor=black)
![vscode](https://img.shields.io/badge/visual%20studio%20code-%231B395A?style=for-the-badge&labelColor=black)
![git](https://img.shields.io/badge/git-%23D47553?style=for-the-badge&logo=git&labelColor=black)

## What is this project about?
During the COVID-19 pandemic, travel across London changed drastically. This project looks at London Underground passenger data from Transport for London (TfL) to see how different areas (Zones 1 through 6) and specific tube stations handled the lockdowns. 
* **Data Sources:** 

The goal was to find out **which areas saw the biggest drop in passengers** and **which stations were hit the hardest.**

## Project Structure
```
├── .gitignore                      
├── LICENSE                         
├── README.md                       
├── tfl_stations.csv
├── london_tube_pandemic_analysis.ipynb
└── zone_impact_chart.png

```
## Visualisations
![Zone impact chart image](zone_impact_chart.png)

## How I Built It & The Data Cleaning Phase
The initial data contained tracking for millions of passengers, but it also included overground trains and newer extensions. Because TfL expanded its network over the years, running math on the raw data would leave massive gaps and skew the results.

To keep the project clean, I focused strictly on classic London Underground stations and filtered out the noise using Pandas in Python: 
```python
tube_df = tube_df[tube_df['London Underground'] == 'Yes']

```

## Data Analysis & Key Findings
### Finding the Busiest Stations (Pre-Pandemic Baseline)
Before looking at the pandemic's impact, I needed to understand what "normal" looked like by sorting to find the absolute busiest station before the pandemic.
```python
busiest_stations = tube_df.sort_values('En/Ex 2019', ascending=False)
busiest_stations.head(1)

```
* **Result:** Stratford was the busiest station in London. Unlike classic tourist hubs, Stratford is a massive interchange connecting multiple train lines, the DLR, and a major shopping center, making it London's top transit bottleneck.

## Remaining Busy During Lockdown
I ran the same query on the 2020 data to see which stations managed to keep footfall3 even during strict lockdowns.




[← Back to Main Portfolio](https://github.com/araba07/Analytics-Portfolio)

# Summary Data

Aggregated outputs from the cleaned Divvy trip data. The Power BI and Tableau dashboards read these files.

| File | Grain | Columns |
|---|---|---|
| `summary_by_rider_year.csv` | year × rider type | rides, average and median ride length |
| `summary_by_weekday.csv` | year × weekday × rider type | rides, average and median ride length, share of rides |
| `summary_by_hour.csv` | year × start hour × rider type | rides, average ride length |

Raw and cleaned trip-level data are not redistributed in this repository.

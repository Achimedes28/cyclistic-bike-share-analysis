# Methodology

## Business Question

How do annual members and casual riders use Cyclistic bikes differently?

## Data Sources

The analysis uses public Divvy trip data from:

- Q1 2019
- Q1 2020

The analysis is a Q1 year-over-year comparison and does not represent a complete annual analysis.

## Tools

- Google Sheets
- Python
- Pandas
- Google Colab
- Tableau Public
- Microsoft PowerPoint

## Data Preparation

The 2019 and 2020 files used different schemas. The following fields were standardized:

| 2019 Field | Standard Field |
|---|---|
| trip_id | ride_id |
| start_time | started_at |
| end_time | ended_at |
| from_station_name | start_station_name |
| to_station_name | end_station_name |
| usertype | member_casual |

Rider classifications were standardized as follows:

- Subscriber → member
- Customer → casual

## Derived Fields

- ride length in minutes
- day of week
- day name
- year
- start hour

## Data Validation

The final dataset was checked for:

- correct datetime conversion
- consistent rider categories
- consistent column names
- missing values
- duplicate or invalid records
- row count after concatenation

## Analysis

The analysis compares:

- total rides
- average ride duration
- weekday usage
- hourly usage
- differences between casual riders and members

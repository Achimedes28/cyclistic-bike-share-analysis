# Cyclistic Bike-Share Analysis

How do annual members and casual riders use Cyclistic bikes differently, and how can that turn more casual riders into members?

[![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?logo=powerbi&logoColor=black)](dashboards/powerbi/)
[![Tableau](https://img.shields.io/badge/Tableau-Dashboard-E97627?logo=tableau&logoColor=white)](https://public.tableau.com/shared/ZF6PXPNS3?:display_count=n&:origin=viz_share_link)
[![Presentation](https://img.shields.io/badge/Slides-PDF-555555)](presentation/cyclistic_case_study.pdf)
[![Python](https://img.shields.io/badge/Python-pandas-3776AB?logo=python&logoColor=white)](notebooks/cyclistic_bike_share_analysis.ipynb)

![Power BI dashboard](dashboards/powerbi/preview.png)

## Key findings

| | Members | Casual riders |
|---|---|---|
| Share of Q1 2020 rides | 88.6% | 11.4% |
| Median ride length (Q1 2020) | 8.6 min | 21.2 min |
| Busiest day (Q1 2020) | Tuesday | Sunday |
| Busiest start hours | 8 AM and 5 PM | 2 PM to 4 PM |

1. Members take most rides and use bikes for short weekday commutes.
2. Casual riders take rides 2 to 3 times longer, mostly on weekends and in the afternoon.
3. Total Q1 rides grew 16.9% from 2019 to 2020, and casual rides more than doubled.

## Recommendations

1. **Weekend membership offers.** Target casual riders on Saturdays and Sundays, when their usage peaks.
2. **Convert long rides.** Show the membership savings after rides that exceed a set length.
3. **Segmented digital campaigns.** Time messages to the hours and days each group actually rides.

## Data

- Public Divvy trip data for Q1 2019 and Q1 2020 (about 792,000 rides after cleaning).
- Raw trip files are not redistributed. The repository keeps only aggregated outputs in [`data/summary/`](data/summary/).
- Q1 only, so results are not a full-year or seasonal view.

## Approach

| Step | Work |
|---|---|
| Ask | Defined the business question and stakeholders |
| Prepare | Reviewed schema, credibility, licensing, and limits of the data |
| Process | Aligned 2019 and 2020 schemas and rider labels, derived ride length, weekday, and hour ([methodology](docs/methodology.md)) |
| Analyze | Compared volume, duration, weekday, and hourly patterns in Python |
| Share | Built [Power BI](dashboards/powerbi/) and [Tableau](dashboards/tableau/) dashboards and an [executive deck](presentation/cyclistic_case_study.pdf) |
| Act | Turned findings into three membership-conversion recommendations |

**Tools:** Python (pandas) · Google Colab · Google Sheets · Power BI (Power Query, DAX) · Tableau · PowerPoint

## Repository

```
├── data/summary/        aggregated CSV outputs used by the dashboards
├── notebooks/           cleaning and analysis notebook
├── dashboards/
│   ├── powerbi/         Power BI Project (.pbip), DAX measures, theme
│   └── tableau/         Tableau dashboard screenshot and link
├── presentation/        executive case study (PDF and PPTX)
└── docs/                methodology
```

## Limitations

- Covers Q1 2019 and Q1 2020 only.
- Trip purpose, weather, pricing, and campaign data are not available.
- No rider ID, so repeat usage by the same person cannot be tracked.
- A few very long casual trips inflate averages (the 2020 casual average is 95.8 minutes against a median of 21.2), so medians are used for comparisons.
- Trips with a negative duration and Divvy test rides (station "HQ QR") were not removed; see [methodology](docs/methodology.md).

## Disclaimer

Independent educational portfolio project, not affiliated with or endorsed by Divvy, Lyft, or the City of Chicago.

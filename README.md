# Flight-Delay
# US Airline On-Time Performance Dashboard

An interactive Power BI dashboard built from 1.19M+ U.S. domestic flight records (January 2019 and January 2020) —mainly to get real practice with data cleaning, data modeling, and DAX, and to have something concrete to show while I look for Data Analyst / Business Analyst roles.

## About the data

Source: US DOT/BTS Airline On-Time Performance data, January 2019 and January 2020 (via Kaggle). Two CSVs of roughly 580K rows each, one per year, cleaned and combined into a single fact table in Power Query.

One thing worth flagging upfront: there's no passenger-count field in this data, even though similarly named versions of this dataset sometimes get described that way online. It's flight-level on-time performance data — delays, cancellations, diversions , not passenger volume. Flight counts are used here as a proxy for traffic, not a headcount.

## What's in the dashboard

**Overview** — total flights, cancellation/diversion rates, on-time performance, daily flight volume for both years overlaid, and flight volume by carrier.

**Delay Analysis** — delay rate by carrier, plus a day-of-week × time-of-day heatmap showing how delays build up over the course of a day.

**YoY Comparison** — January 2019 vs. January 2020, side by side and carrier by carrier.

<img width="665" height="376" alt="delay " src="https://github.com/user-attachments/assets/1c27e47c-4a1d-42a4-a035-60ddd3565c1c" />
<img width="668" height="374" alt="YOY comparison" src="https://github.com/user-attachments/assets/be96b1a8-3671-4ce5-b404-68d31681ae86" />
<img width="668" height="374" alt="YOY comparison" src="https://github.com/user-attachments/assets/b4428fb1-8c45-4743-b1e5-be9580823df4" />




## A few things I found

- Delay rates climb steadily through the day — around 6.5% for 6 AM departures, up to roughly 21% by early evening.
- Cancellation rates vary a lot by carrier — from 0.17% to 5.34% across the 17 carriers in the data.
- January 2020 actually had a better on-time rate than January 2019 (83% → 86%). I expected the opposite going in.

## How it's built

- Power Query for cleaning, type fixes, and combining the two years into one table
- A data model with dedicated Date and Carrier dimension tables, related to a single Flights fact table — not one flat sheet
- DAX measures for rates, KPI cards, and year-over-year comparisons
- Slicers synced across pages

## Files
https://github.com/muskaanjindal9020-art/Flight-Delay/blob/main/Aviation.pbit
## About me

Self-taught in Power BI, SQL, and Excel while transitioning from an operations background into data analytics. This is my second portfolio project. Open to feedback, and open to Data Analyst, Business Analyst, or MIS roles.

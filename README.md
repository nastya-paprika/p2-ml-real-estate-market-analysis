# Real Estate Market Analysis

## Introduction

**Source Data**: The dataset is provided by the Yandex Real Estate service and contains an archive of apartment sales listings in Saint Petersburg and the surrounding areas collected over several years.

**Goal**: The objective is to identify the key parameters that influence the market value of real estate. The findings from this Exploratory Data Analysis (EDA) will be used to build an automated system capable of detecting anomalies and fraudulent activity in the listings.

The dataset includes two types of data for each property:

- User-generated data: Information entered manually by the seller.
- Automated (Spatial) data: Information calculated automatically based on map data (e.g., distance to the city center, airport, nearest parks, and bodies of water).

**Key Business Questions**:

- *Time to Sale*: How long does it typically take to sell an apartment? At what point is a sale considered "too fast" or "abnormally slow"?
- *Price Drivers*: Which factors have the strongest impact on the total market value of an apartment?
- *Location Analysis*: What is the average price per square meter in the top 10 locations with the highest number of listings?
- *City Center vs. Suburbs*: Which factors influence prices specifically in the Saint Petersburg city center, and how do they differ from the overall market trends?

## Prerequisites

- Jupyter Notebook
- Python 3

## Data Description

- `total_images`(int64) - number of photos in the listing,
- `last_price`(float64) - price at the time the listing was removed,
- `total_area`(float64) - total apartment area in square meters (m²),
- `first_day_exposition`(object) - date of publication,
- `rooms`(int64) - number of rooms,
- `ceiling_height`(float64) - ceiling height (m),
- `floors_total`(float64) - total number of floors in the building,
- `living_area`(float64) - living area in square meters (m²),
- `floor`(int64) - the floor the apartment is located on,
- `is_apartment`(object) - apartment status,
- `studio`(bool) - whether the apartment is a studio,
- `open_plan`(bool) - whether the apartment has an open floor plan,
- `kitchen_area`(float64) - kitchen area in square meters (m²),
- `balcony`(float64) - number of balconies,
- `locality_name`(object) - name of the locality/settlement,
- `airports_nearest`(float64) - distance to the nearest airport (m),
- `cityCenters_nearest`(float64) - distance to the city center (m),
- `parks_around3000`(float64) - number of parks within a 3 km radius,
- `parks_nearest`(float64) - distance to the nearest park (m),
- `ponds_around3000`(float64) - number of bodies of water within a 3 km radius,
- `ponds_nearest`(float64) - distance to the nearest body of water (m),
- `days_exposition`(float64) - number of days the ad was listed (from publication to removal).

## Notes

`data.csv` is private and cannot be shared. Example of data:

```csv
total_images	last_price	total_area	first_day_exposition	rooms	ceiling_height	floors_total	living_area	floor	is_apartment	studio	open_plan	kitchen_area	balcony	locality_name	airports_nearest	cityCenters_nearest	parks_around3000	parks_nearest	ponds_around3000	ponds_nearest	days_exposition
20	13000000.0	108.0	2019-03-07T00:00:00	3	2.7	16.0	51.0	8		False	False	25.0		Санкт-Петербург	18863.0	16028.0	1.0	482.0	2.0	755.0
7	3350000.0	40.4	2018-12-04T00:00:00	1		11.0	18.6	1		False	False	11.0	2.0	посёлок Шушары	12817.0	18603.0	0.0		0.0		81.0
10	5196000.0	56.0	2015-08-20T00:00:00	2		5.0	34.3	4		False	False	8.3	0.0	Санкт-Петербург	21741.0	13933.0	1.0	90.0	2.0	574.0	558.0
0	64900000.0	159.0	2015-07-24T00:00:00	3		14.0		9		False	False		0.0	Санкт-Петербург	28098.0	6800.0	2.0	84.0	3.0	234.0	424.0
```

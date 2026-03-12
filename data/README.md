# 📂 Data

## Datasets Used

This project uses three datasets provided by Turismo de Lisboa (LTA) via NOVA IMS:

| File | Description | Key Fields |
|------|-------------|------------|
| `attractions_list.csv` | Master list of Lisbon tourist attractions | `tripadvisor_id`, attraction name, category, location |
| `attractions_data_metadata.csv` | Attraction-level metadata | `tripadvisorId`, subcategory, price range, accessibility info |
| `reviews.csv` | Individual TripAdvisor visitor reviews | reviewer info, ratings, review text, date, language |

## Merge Strategy

The three datasets were merged on `tripadvisor_id` using left joins:
1. `reviews` ← `metadata` (on `tripadvisor_id`)
2. merged result ← `attractions` (on `tripadvisor_id`)

## Data Not Included

The raw data files are **not included** in this repository. They were provided under academic licence from Turismo de Lisboa through NOVA IMS.

If you wish to reproduce this analysis, you would need an equivalent dataset containing:
- Attraction reviews with text, rating (1–5), reviewer ID, date, and language
- Attraction metadata (category, subcategory, location, pricing)
- Attraction master list with unique identifiers

A suitable public alternative is the [TripAdvisor Hotel Reviews dataset on Kaggle](https://www.kaggle.com/datasets/andrewmvd/trip-advisor-hotel-reviews).

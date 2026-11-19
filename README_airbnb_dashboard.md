# Airbnb – Guest Experience & Marketplace Performance Dashboard

## Project context
This portfolio project uses public Inside Airbnb data to explore marketplace supply, guest review patterns, listing ratings and listed prices in New York City. It is an independent analysis and is **not** based on Airbnb's internal operational or customer-support systems.

## Business questions
1. How is listing supply distributed across NYC boroughs?
2. How do recorded guest ratings vary by borough and room type?
3. How has the volume of recorded guest reviews changed over time?
4. How do median listed nightly prices differ by room type?
5. How can marketplace teams use these patterns to prioritise deeper investigation?

## Data source
Inside Airbnb: https://insideairbnb.com/get-the-data/

Files used:
- `listings.csv.gz` – listing-level details, price, room type, availability, review counts and ratings.
- `reviews.csv.gz` – individual review records and dates.

The supplied listings snapshot was scraped on 14–15 September 2026. The supplied review history runs from 25 May 2009 to 14 September 2026.

## Data quality and methodology
- Listing prices are converted from text to numeric values. Missing prices are excluded from price calculations.
- Missing listing ratings are excluded from rating averages.
- Host response-time and host response-rate fields are entirely missing in this extract, so they are not analysed.
- Review trends count rows in the reviews file by calendar year.
- Listing review totals use `number_of_reviews` from the listing file; this is distinct from counting the review rows.
- Availability days are not equivalent to booked nights or occupancy.
- Public review records are an imperfect proxy for guest experience and do not represent every stay.
- Results are descriptive; they do not establish causation.

## Dashboard
Open `airbnb_marketplace_dashboard.html` in a modern browser. The dashboard uses Plotly from its public CDN, so an internet connection is required to render the charts.

## Suggested next steps
- Add a neighbourhood-level drill-down.
- Add a map view using listing latitude/longitude.
- Add a separate methodology and insights section to the portfolio case study.
- Publish the HTML file using GitHub Pages.

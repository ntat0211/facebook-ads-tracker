# Facebook Ads Tracker Pro

A lightweight, browser-based dashboard for Meta Ads exports. It is designed to help compare campaign, ad set, and ad performance for lead-generation campaigns.

## Features

- Import CSV/TSV/TXT exports from Meta Ads Manager.
- Import Excel files when the browser can load SheetJS from its CDN.
- Map Meta columns manually when export column names differ.
- Filter by date range, campaign, ad set, and ad.
- View KPIs including spend, leads, CPL, CTR (link), CPC (link), impressions, reach, CPM, and frequency.
- Compare daily or weekly performance (weeks begin Monday).
- View spend and lead shares by campaign objective.
- Export the grouped performance table to CSV.
- Choose a currency display. Choosing a currency changes the display symbol/format only; it does not convert amounts.

## How to use

1. Open `index.html` in a modern browser, or publish the repository using GitHub Pages.
2. Export a report from Meta Ads Manager, ideally with daily time breakdown.
3. Include campaign name, campaign objective (if available), ad set name, ad name, amount spent, impressions, reach, link clicks, and one appropriate lead-result column.
4. Upload the export.
5. Review the column mapping, particularly the Leads / Results field, and choose the right currency if it is not detectable from the column headers.
6. Apply mapping before analyzing.

## Important data notes

- Meta's generic `Results` column can mean different actions depending on the campaign objective. Confirm it represents leads before using it as the lead count.
- Map only one lead-result column to avoid double-counting conversions.
- Reach may overlap across reporting dates; summing daily reach does not produce unique people reached.
- If the export does not include a campaign-objective field, the app infers a likely objective from campaign names. Treat inferred labels as estimates and verify them.
- Currency selection does not perform foreign-exchange conversion.
- For an apples-to-apples comparison, use consistent reporting dates and the same level of breakdown. Avoid mixing campaign-, ad-set-, and ad-level rows in a single export if that duplicates metrics.

## Privacy

CSV data is processed locally in the browser by this app and is not sent to a backend server. Excel import loads the SheetJS library from a CDN, so it requires an internet connection. Do not commit private ad reports, customer information, or credentials to this repository.

## Tech

Single-page HTML, CSS, and JavaScript. No build step is required.

# Group CF — Performance Dashboard

A live-linked broker performance dashboard: KPIs, pipeline funnel, trail movement, year-on-year trends, and an auto-generated business-health score — all read from a Google Sheet.

## What's here

- **`index.html`** — the dashboard. A single self-contained file (no build step). Open it in any browser or host it on GitHub Pages.
- **`Groupcf_dashboard_data.xlsx`** — the data-entry template. Import into Google Sheets and enter one row per month.

## Setup

1. Import `Groupcf_dashboard_data.xlsx` into Google Sheets (New → File upload → open → *Save as Google Sheets*).
2. Enter your numbers on the **Data** tab — one row per month. Fill what you have; blank columns are simply left empty on the dashboard.
3. Share the sheet: **Share → Anyone with the link → Viewer**.
4. Open the dashboard, paste your **Sheet ID** (the code in the sheet URL between `/d/` and `/edit`), and click **Load**.

The dashboard opens on a clean "no data" screen until you load your sheet. Click **Demo data** any time to preview the design with sample numbers.

## Hosting it live (GitHub Pages)

**Settings → Pages → Source: Deploy from a branch → Branch: `main` / `root` → Save.**
Your dashboard goes live at `https://<your-username>.github.io/<repo-name>/`.

## Data columns

Month · Enquiries · Applications · Lodgements (No. & $) · Approvals (No. & $) · Unconditional (No.) · Settlements (No. & $) · Active Pipeline ($) · Trail Book ($) · New Trail ($) · Trail Lost ($) · Run-off ($).

## Notes

- Monthly $ targets are set in `index.html` near the top of the script (`const TARGETS = {...}`).
- The **business-health score and insight are computed from your data with fixed rules**, not a live AI model.
- No data is stored in the file; the Sheet ID you type stays in your own browser. Safe to keep the repo public.

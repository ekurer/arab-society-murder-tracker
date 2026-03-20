# Homicide Tracker

## Concept

This project turns yearly homicide records from a public Google Sheet into a single normalized dataset, then presents it in an interactive dashboard.

The goal is to make trends and patterns easy to inspect by year, locality, and key indicators (totals, solve rate, firearm share, and comparisons between years).

## Repo Layout

- `public/`: published GitHub Pages site and browser-consumed data artifacts
- `public/data/processed/`: normalized CSV/JSON outputs used by the dashboard
- `public/data/reference/`: reference datasets such as locality coordinates
- `data/raw/google-sheet/`: yearly raw CSV pulls from the public sheet

## Run Locally

Prerequisite: Ruby installed.

1. (Optional) Refresh data from the Google Sheet and rebuild normalized files:

```bash
./scripts/sync_from_google_sheet.sh
```

2. Start the local server:

```bash
./scripts/start_dashboard.sh
```

3. Open:

- `http://localhost:8000/dashboard/`

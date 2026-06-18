# Shift Tracker

A single-page, no-build web app for logging work shifts and tracking pay across multiple jobs. Everything runs client-side in `index.html` — data is saved to the browser's `localStorage`, no backend or build step required.

## Features

- **Log shifts** with date, start/end time, job, break minutes, and an optional note
- **Live pay preview** while filling in the add-shift form
- **Multiple jobs** with color-coded tags (Acoustics Project, POD, Innohub)
- **Summary views**
  - *Shifts* — full table of every logged shift
  - *Weekly* — hours and pay grouped by ISO week
  - *Monthly* — hours and pay grouped by month, with a running total
- **Dashboard metrics** — total shifts, total hours, total pay, and pay for the current month
- **Delete with confirmation** to undo accidental entries
- Hourly rate is configurable via the `RATE` constant in [index.html](index.html)

## Usage

Open [index.html](index.html) directly in a browser — no server or installation needed.

1. Click **+ Add shift** to log a new shift
2. Fill in the date, start/end time, job, and optional break/note
3. Click **Save shift** — it appears in the Shifts table and rolls up into the Weekly/Monthly views
4. Use the tabs to switch between per-shift, weekly, and monthly summaries

## Data

Shifts are stored in `localStorage` under the key `wurk_shifts`. A seed dataset is bundled in the script for first-time use; any shifts you add persist locally in your browser.

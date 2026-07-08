# studio-musicians
# Session Musicians — Belmont AET

**Live URL:** https://bradwintersmusic-cloud.github.io/studio-musicians/

Public-facing directory of Belmont AET students available for session work. Loads live from a Google Sheet populated via Tally form submissions.

---

## Overview

- Alphabetical list grouped by first name initial
- Filters: instrument, genre, click track ability, school year, availability
- Full-text search: name, instruments, genres, notes
- Click any row to open full detail modal
- Copy buttons for name/contact info
- Sign-up button links to Tally form
- Public disclaimer on page — no data is protected

---

## ⚠️ Public Page Notice

This page is publicly accessible. All submitted information is visible to anyone with the URL. Students are informed of this on the Tally form before submitting.

---

## Data Source

**Google Sheet CSV** — URL defined at the top of the script in `index.html`:

```javascript
var SHEET_CSV_URL = "YOUR_GOOGLE_SHEET_CSV_URL_HERE";
```

To publish: Google Sheets → File → Share → Publish to web → select sheet tab → CSV → copy URL.

---

## Google Sheet Column Headers

Must match exactly (case-sensitive):

| Column | Required | Notes |
|---|---|---|
| First Name | Yes | |
| Last Name | Yes | |
| School Year | Yes | Freshman, Sophomore, Junior, Senior, Graduate |
| Major | Yes | AET, School of Music, Songwriting, Music Business, Other |
| Email Address | Yes | Displayed in modal only |
| Phone Number | No | Hidden from page display |
| Preferred Contact Method | No | Email, Text, Either |
| Primary Instruments | Yes | Comma-separated from checkboxes |
| Additional Instruments | No | Comma-separated |
| Primary Genre | Yes | Comma-separated; "All" matches any genre filter |
| Additional Genres | No | Comma-separated |
| Click Track | Yes | Yes — Comfortably / Yes — With Practice / Not Yet |
| Years of Experience | No | |
| Availability | No | Comma-separated from checkboxes |
| Portfolio Link | No | URL |
| About Me | No | Long text |
| Active | Manual | FALSE to hide; missing or TRUE = visible |

---

## Managing Musicians

**To hide a musician:** Set `Active` to `FALSE` in the sheet. They will not appear on the page but their data is preserved.

**To re-activate:** Change `FALSE` back to `TRUE` or clear the cell.

New submissions appear automatically — no approval step. Tally writes directly to the sheet.

---

## Tally Form

The sign-up form is linked from the page. The form link is set in the `index.html`:

```javascript
// Find the signup button href and update with your Tally form URL
```

---

## Tech Stack

- Static HTML / CSS / JS
- Google Sheets (CSV data source)
- Tally (form submissions, direct Google Sheets integration)
- GitHub Pages hosting

---

## Repo

`bradwintersmusic-cloud/studio-musicians`
Maintained by Brad Winters
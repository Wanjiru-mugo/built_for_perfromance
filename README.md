# BFP podcast finance

Live dashboard for every cost behind Built for Performance: studio sessions, editing, kit and guest hospitality.

## Files

- `index.html`: the dashboard. Don't edit unless changing the design.
- `data.json`: all the numbers. This is the only file you update.
- `blueprint.html`: map of how the finance flow works.

## Set up GitHub Pages (once)

1. Create a repo called `bfp-finance` and upload these files.
2. Settings > Pages > Source: Deploy from a branch > `main` / root > Save.
3. In `data.json`, set `meta.github.owner` to your GitHub username so the "Edit on GitHub" button works.
4. Your site appears at `https://<username>.github.io/bfp-finance/` within a couple of minutes.

## Adding spend

Option A: on the live page click **+ Add spend**, then **Export data.json**, then upload the downloaded file to the repo (Add file > Upload files > Commit).

Option B: edit `data.json` on GitHub with the pencil icon. Copy an entry, change the values, commit.

Categories: `Production`, `Kit & accessories`, `Hospitality`, `Other`.
Use the guest's name in `guest` so each line rolls up to the right recording.

## Bookings

Upcoming sessions live in the `bookings` list in `data.json` (date, guest, status, package, studio cost, hospitality plan and budget). Add them with **+ Add booking** on the site, then export and upload as above.

## Hospitality entry example

```json
{
  "id": "e8", "date": "2026-10-30", "guest": "Natalie", "category": "Hospitality",
  "supplier": "Restaurant name", "ref": "", "hours": 0,
  "items": ["Meal / drinks"], "amount": 64.50, "status": "Paid",
  "payments": [], "notes": "Lunch with Peter before recording"
}
```

## Privacy

Unless the account is on GitHub Enterprise Cloud, a Pages site is public to anyone with the link.

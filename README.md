# Fuel Mate app prototype

Clickable demo of the redesigned Liberty Fuel Mate app, for internal review.

Live demo: https://joshbattaglia-hub.github.io/fuel-mate-demo/

All names, litres, distances, receipts and card numbers in the demo are sample data.

## Adding national promotions to the Deals tab

The Deals tab shows every image in the `deals/` folder.

1. Open the `deals` folder on GitHub and choose **Add file → Upload files**.
2. Drop in the promo images (JPG or PNG, portrait 4:5 works best, e.g. 1080 × 1350).
3. Click **Commit changes**. The images appear in the app within a minute or two.

The deal's title comes from the file name (`eclipse-mints-4-each.jpg` shows as "Eclipse Mints 4 Each").
For a proper title and an end date, add an entry to `deals/deals.json`:

```json
{ "file": "eclipse-mints-4-each.jpg", "title": "Eclipse mints 40g: $4 each", "starts": "2026-09-30", "ends": "2026-10-27" }
```

Deals listed in `deals.json` disappear from the app automatically after their end date.
To remove a deal straight away, delete its image from the folder.

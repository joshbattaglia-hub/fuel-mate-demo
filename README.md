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

### Hero deals you scan to redeem

Add `"hero": true` and a `redeem` block to a deal in `deals.json` to make it the featured, app-exclusive offer.
It gets a large banner at the top of Home and Deals, and a barcode screen customers show at the counter:

```json
{
  "file": "chicken-tenders-3-for-6.jpg",
  "title": "Triple Treat: 3 chicken tenders for $6",
  "starts": "2026-09-30",
  "ends": "2026-12-22",
  "hero": true,
  "redeem": { "barcode": "2600300600013", "terms": "One redemption per member per day." }
}
```

Landscape 16:9 images (e.g. 2000 × 1125) work best for hero deals.
To remove a deal straight away, delete its image from the folder.

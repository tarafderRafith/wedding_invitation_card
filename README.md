# Rafith & Nishat — Wedding Invitation

A mobile-first, single-page wedding invitation website. The four supplied couple illustrations are embedded directly in `index.html`, so no image files or build tools are required.

## Run locally

1. Open `index.html` in a modern browser.
2. Tap the envelope seal to open the invitation.
3. Scroll through the invitation and try the scratch-to-reveal card.
4. Use the music button after adding your own MP3 file (instructions below).

## Personalize the invitation

Open `index.html` in a text editor and find:

```js
const WEDDING = {
  date: "2027-05-14T18:00:00+06:00",
  displayDate: "14 MAY 2027",
  venue: "Reception Venue",
  address: "Add your full village-home address here",
  mapsUrl: ""
};
```

Update these values:
- `date`: Reception date and time in ISO format. Bangladesh time uses `+06:00`.
- `displayDate`: The date text shown under the scratch layer.
- `venue`: Your venue name.
- `address`: The full venue address.
- `mapsUrl`: Your Google Maps share URL.

The current date/time (`14 May 2027`, 6:00 PM Bangladesh time) is only a placeholder based on the initial brief. Confirm or change it before sharing the invitation.

## Background music

The supplied MP3 is included at `assets/wedding-music.mp3`. It starts when a visitor taps the envelope to open the invitation. The floating music button toggles play/pause. The audio loops continuously.

Browsers generally block sound autoplay before a visitor interacts with a page, so playback is triggered by the envelope tap rather than on initial page load.

## Publish free with GitHub Pages

1. Create a new GitHub repository.
2. Upload `index.html`, `README.md`, `.nojekyll`, and the `assets` folder.
3. Open the repository's **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)` folder, then save.
6. Wait for GitHub Pages to publish and open the provided website URL.

No Node.js, React, npm, or build step is needed.

## Notes

- All four uploaded illustrations are embedded in `index.html` as optimized WebP data, so they travel with the single HTML file.
- The layout adapts to phone, tablet, and desktop widths.
- The Google Maps button needs your real Maps share link.
- Check the date, venue, address, and music before distributing the public link.

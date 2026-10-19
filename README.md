# Houssem & Maha — Wedding Invitation Website

A lightweight, responsive, static wedding invitation page designed for WhatsApp sharing.

## Included
- English copy with an elegant-but-playful style
- Wedding date: Saturday, October 24, 2026
- Arrival time: 19:00 (7:00 PM)
- Venue label: Family's house
- Dress code: No strict dress code
- Dinner followed by a Hadhra party
- Google Maps directions link supplied by the couple
- Personalized greeting from a URL parameter, e.g. `?to=Amine`
- Native share button on compatible phones, clipboard fallback elsewhere
- Open Graph / WhatsApp link preview metadata placeholders
- No RSVP flow

## Preview locally
Open `index.html` in a browser. Most content works locally; the final WhatsApp preview metadata only works after hosting because social apps need a public URL.

## Free hosting: GitHub Pages
1. Sign in to GitHub and create a new public repository, for example `houssem-maha-invitation`.
2. Upload `index.html` to the repository root.
3. Open **Settings → Pages**.
4. Under the build/deployment source, select **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Wait for GitHub Pages to publish the site. Your public URL will look like `https://YOUR-USERNAME.github.io/houssem-maha-invitation/`.

Alternative: drag the folder into Netlify's manual deploy workflow and use the public URL it provides.

## Important: configure social preview metadata
Before sending the final link, edit `index.html` and replace these placeholders:
- `https://YOUR-DOMAIN.example/og-wedding.jpg` with a publicly accessible preview image URL.
- `https://YOUR-PUBLISHED-SITE.example/` with the exact public website URL.

For reliable WhatsApp previews, create a 1200×630 JPG or PNG invitation image and host it publicly (you can put `og-wedding.jpg` in the same repository and use the absolute URL to it). Then update `og:image` and `og:url` in the HTML. Some platforms cache link previews, so test the final public URL before sending it widely.

## Personalize a link for each friend
Use the public website URL plus `?to=` and a URL-encoded name:
- `https://YOUR-USERNAME.github.io/houssem-maha-invitation/?to=Amine`
- `https://YOUR-USERNAME.github.io/houssem-maha-invitation/?to=Sarah%20Ben%20Ali`

Each link displays a unique greeting. Send the links individually via WhatsApp; don't post private personalized links in a group if you want the greeting to remain personal.

## Suggested WhatsApp message
Hey Amine! 💌 A little personal invitation from Houssem & Maha. Open yours here: [YOUR PERSONALIZED LINK]

## Notes
- The supplied Google Maps URL is used as provided. Confirm that it opens the intended venue before sharing.
- The venue is labeled “Family's house” because no more specific venue name/address was supplied.
- The page intentionally does not include an RSVP button.
- The date and time are shown exactly as supplied; no timezone or extra schedule times are invented.
- External fonts load from Google Fonts; fallback fonts are included if those are unavailable.

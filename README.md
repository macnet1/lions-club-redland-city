# Lions Club of Redland City — Website

A simple, free-to-host website for the Lions Club of Redland City. Plain HTML/CSS/JS — no build step required.

## Pages

- `index.html` — Home
- `about.html` — About the club
- `events.html` — Upcoming events (edit the table with real dates)
- `membership.html` — Join us
- `donate.html` — Donate / sponsorship
- `contact.html` — Contact form + details

## Things to update with real info

- **Logo**: `images/emblem.svg` is a placeholder emblem. Replace it with your official club logo/crest (see below).
- **Email**: currently set to `mandteresa@gmail.com` in every page footer and the contact page — update if you want a different club address.
- **Meeting schedule & location**: placeholder in `events.html` — replace with real dates/venue.
- **Donation details**: `donate.html` has no live payment link yet — add a PayPal/bank/Givewell link when ready.
- **Contact form**: uses a `mailto:` action, which opens the visitor's email app. For an automated form (no email client needed), sign up free at [Formspree](https://formspree.io) and swap the `action` attribute in `contact.html`.

## Using your official club logo

If you have a logo image file (PNG/JPG/SVG):

1. Save it into the `images/` folder, e.g. `images/lions-logo.png`.
2. In every HTML file, replace:
   ```html
   <img src="images/emblem.svg" alt="Lions Club of Redland City emblem" class="brand-emblem">
   ```
   with:
   ```html
   <img src="images/lions-logo.png" alt="Lions Club of Redland City emblem" class="brand-emblem">
   ```
3. Also update the favicon line in each `<head>`:
   ```html
   <link rel="icon" href="images/lions-logo.png">
   ```

## Deploying free on GitHub Pages

1. Create a free GitHub account at https://github.com if you don't have one.
2. Create a new **public** repository, e.g. `lions-club-redland-city`.
3. From this folder, run:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/lions-club-redland-city.git
   git push -u origin main
   ```
4. On GitHub, go to the repo's **Settings → Pages**.
5. Under "Build and deployment", set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
6. Your site will be live in a minute or two at:
   `https://<your-username>.github.io/lions-club-redland-city/`

### Optional: custom domain

If the club later buys a domain (e.g. `lionsredlandcity.org.au`), add a `CNAME` file with that domain in the repo root and point the domain's DNS to GitHub Pages — GitHub's docs walk through this under Settings → Pages → Custom domain.

## Previewing locally

Just open `index.html` in a browser — no server needed. For a local dev server (optional), you can run:
```bash
python -m http.server 8000
```
and visit `http://localhost:8000`.

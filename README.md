# Tally

A personal finance dashboard for tracking bills, subscriptions, bank accounts, savings goals and debt in one place. Tally is a static web app: plain HTML, CSS and JavaScript with no build step and no dependencies. All data stays in your browser's `localStorage`; nothing is sent to a server.

## Features

- **Dashboard wheel**: balance of the bank account you pick, or all banks combined, with the share your upcoming bills will take.
- **Banks / Savings / Debt tiles**: double tap to update balances quickly, hold to choose which account is shown.
- **Customizable graphs**: hold a circle to switch it between saving goal, debt, credit used and rent goal. Debt and rent have their own limits.
- **Calendar and upcoming bills**: every bill and subscription appears on its due day. Bills count as paid automatically once the date passes.
- **Accounts**: banks, savings (with goals) and debt (with credit limits). Savings goals sync with the dashboard.
- **Company logos** for popular banks, bills and subscriptions, plus custom logo upload.
- **Personalization**: name greeting that changes with the time of day, blue accent palettes, dark mode, currency, animations on/off.
- **First-run tutorial**, replayable from the ⋯ menu.

## Run locally

No install needed. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a repository and push this folder to the `main` branch:

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-user>/<your-repo>.git
   git push -u origin main
   ```

2. In the repository go to **Settings → Pages** and set **Source** to **GitHub Actions**.
3. The included workflow (`.github/workflows/pages.yml`) publishes the site on every push to `main`.

## Project structure

```
index.html   Page shell
styles.css   All styling, themes and animations
app.js       App state, rendering, gestures, logo data
favicon.svg  Icon
.github/workflows/pages.yml   GitHub Pages deployment
```

## Data and privacy

State is saved in `localStorage` under a single key. Clearing site data resets the app. Use **Settings → Reset to original data** to restore the sample data.

## Credits

- Brand marks come from [Simple Icons](https://simpleicons.org) (CC0 1.0). Brand names and logos are trademarks of their respective owners and are used here only to identify those companies; Tally is not affiliated with or endorsed by them.
- Typeface: Bricolage Grotesque via Google Fonts.

## License

MIT, see [LICENSE](LICENSE). Update the copyright holder to your name before publishing.

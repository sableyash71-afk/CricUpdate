# Boundary Live Cricket Score App

## Files
- `index.html` — app structure
- `styles.css` — responsive dark-green mobile design
- `index.js` — CricketData.org API connection, match list refresh, scorecard rendering

## Run it
1. Create an account at https://cricketdata.org/ and copy your API key.
2. Open `index.html` in a modern browser, or host the three files on a static web host.
3. Paste your key into the API key box and tap **Connect**.
4. Tap a match card to request its scorecard.

## Important notes
- The app calls `https://api.cricapi.com/v1/matches?apikey=...&offset=0` and `https://api.cricapi.com/v1/match_scorecard?apikey=...&id=...`.
- CricketData.org may vary returned fields by endpoint and plan. If batting/bowling detail is missing, check their current API documentation and plan.
- Browser-based API requests may be blocked by CORS in some setups. If so, use a small backend proxy.
- For a public/production app, do not embed a private API key in frontend code. This demo keeps the entered key in browser localStorage, which is convenient but not secret from someone using that browser.
- Automatic refresh is every 60 seconds to avoid excessive API requests. Check your plan's request limits.

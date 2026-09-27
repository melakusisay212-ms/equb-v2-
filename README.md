# Equb Admin v2 – Corrected Logic

Digital organizer for traditional Ethiopian Equbs (ዕቁብ).

## Key Corrections in this version

### 1. Payments are per cycle
- When you mark a member as paid, it is recorded for the **current cycle** (Cycle 1, Cycle 2, Cycle 4…).
- Member detail page shows payment status for every cycle separately.
- No more global “paid” flag that mixes cycles.

### 2. Ethiopian (Habesha) calendar
- Today’s date is shown in Ethiopian calendar.
- New Equb records:
  - **Start date** (today in Habesha calendar)
  - **Finish date** (estimated from number of members × cycle type)
- Calendar view belongs to the **current Equb only**.

### 3. Complete isolation between Equbs
- Each Equb is a completely separate ledger.
- Opening Equb A never shows members, payments, or history from Equb B.
- No data transfer or overlapping between different Equbs.
- Export (CSV/PDF) is always for the currently open Equb only.

## How to deploy

1. Create a new public GitHub repository
2. Upload all files in this folder
3. Go to **Settings → Pages → Source = GitHub Actions**
4. Push to `main` – the site will be live automatically

## Google Login (optional)

1. Create a Google Cloud project
2. Enable Google Drive API
3. Create OAuth Client ID (Web application)
4. Add your GitHub Pages URL to Authorized JavaScript origins
5. Replace this line in `index.html`:

```js
const GOOGLE_CLIENT_ID = 'YOUR_GOOGLE_CLIENT_ID.apps.googleusercontent.com';
```

## Install on phone

- Android Chrome: three-dots menu → **Add to Home screen**
- iPhone Safari: Share → **Add to Home Screen**

---

Built for Ethiopian community organizers.

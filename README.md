# IMA Asana Reports Dashboard

Live reporting dashboard for Idaho Medical Academy — pulls directly from Asana via API.

**Live URL:** https://asanareports.idahomedicalacademy.com

---

## Setup Instructions

### Step 1 — Add files to your repo

Copy `index.html` and `CNAME` into the root of this repo (or a `/dashboard` subfolder if preferred).

### Step 2 — Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Choose **main** branch, **/ (root)** folder → click **Save**
5. GitHub will give you a `*.github.io` URL — that's the fallback

### Step 3 — Point your DNS to GitHub Pages

Log into your domain registrar (wherever `idahomedicalacademy.com` is managed) and add:

| Type  | Name           | Value                    |
|-------|----------------|--------------------------|
| CNAME | asanareports   | camerondaly789.github.io |

DNS propagation takes 5–30 minutes.

### Step 4 — Confirm custom domain in GitHub

1. In **Settings → Pages**, enter `asanareports.idahomedicalacademy.com` under **Custom domain**
2. Click **Save** — GitHub will verify the DNS record
3. Check **Enforce HTTPS** once the cert is issued (usually within 10 min)

---

## Updating the Asana Token

If you ever need to rotate the PAT, open `index.html` and find this line near the top of the `<script>` block:

```js
const PAT = 'your-token-here';
```

Replace with the new token and push to GitHub.

---

## What the Dashboard Shows

- **Current Reports** — Latest Asana goal status for EMS, Healthcare, CPR/AHA, Admin, and Marketing
- **All History** — Every status update ever submitted, in reverse chronological order with timeline view
- **Filters** — Filter by department or time period
- **Live sync** — Pulls fresh from Asana every time the page loads

---

*Idaho Medical Academy — Where Your Journey Begins*

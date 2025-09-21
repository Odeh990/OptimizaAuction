# Auction Page (Single File, No Email)

This is a single-file auction page in Arabic for **Optimiza** staff to bid on a *Smart Apple Watch Series 10*. 
- Shows **countdown (3 days)** from first visit (per-browser).
- Accepts bids (name, email, amount, currency, note).
- Displays **last bid**, keeps a **local log** with **integrity hash chain** to detect tampering per browser.
- Exports the log as **JSON/CSV**.

## Deploy to GitHub Pages (fast)
1. Create a new GitHub repository (public): `auction-page`.
2. Upload `index.html` to the repository root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Branch: `main` (or `master`), folder: `/ (root)` → **Save**.
6. GitHub Pages will give you a URL like:  
   `https://<your-username>.github.io/auction-page/`

## Deploy to Vercel
- Import the repo in Vercel → Project Settings → Framework: **Other** → Root directory: `/`.
- Vercel will deploy and provide `https://auction-page.vercel.app`.

## Deploy on Hostinger
- Upload `index.html` to `public_html/auction/` → access via `https://your-domain.com/auction/`

> IMPORTANT SECURITY NOTE  
This version stores bids in the browser's `localStorage` and uses a hash-chain to detect tampering **per device**. 
For multi-user, tamper-proof logging, add a small backend (Apps Script/Node/Power Automate) that accepts POST-only and stores records centrally (append-only).


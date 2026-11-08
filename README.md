# ILVORA Billing System — GitHub Pages Prototype

A browser-based, interactive prototype for ILVORA Healthcare Group billing workflows.

## Included prototype workflows
- Dashboard with branch-level demo metrics
- Patient registration and patient search
- Bill creation with line items, discounts, tax preview and partial/full payment
- Branch-specific invoice number preview
- Printable receipt (Print / Save as PDF)
- Bill register and status filtering
- Editable sample service rates
- Branch directory and collection summary
- Role selector to preview the intended role model
- Local browser persistence and JSON backup/restore export
- Responsive desktop and mobile layout

## Deploy on GitHub Pages
1. Create a new **public** GitHub repository, for example `ilvora-billing-prototype`.
2. Upload `index.html`, `.nojekyll`, and this `README.md` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main`, folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish. The URL will look like `https://YOUR-ORG.github.io/ilvora-billing-prototype/`.

No build command, API key, database or server is required for this demonstration.

## Important limitations
This is a **front-end prototype**, not a production billing system. It uses browser `localStorage`; records are visible only in the same browser profile on the same device and are not synchronized between branches or users. Clearing browser data can erase records. The role selector is only a UI demonstration and is not authentication or access control. Do not enter real patient information, real payment details, or confidential business data.

Before live use, connect a managed backend (e.g. Supabase PostgreSQL + Auth), enforce branch access with server-side Row Level Security, implement audited payment/refund/void workflows, test backups and restore, complete independent security testing, and obtain Indian healthcare/privacy/accounting legal review. Do not publish database secrets or service-role keys in a GitHub repository.

## Local preview
Open `index.html` in a modern browser. For a local web server, use `python -m http.server 8000` and visit `http://localhost:8000`.

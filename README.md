# Open Order Console

A browser-based tool that cross-checks open sales orders against current stock,
strips lines that can't be fulfilled, and rolls the rest up by region, customer,
and location.

## How it works
Everything runs client-side in the browser — no backend, no server, no database.
Upload your five SAP exports, click **Generate Open Order Report**, and the
calculation happens entirely on your machine. Nothing is transmitted anywhere.

## Local development
This is a single static HTML file (`index.html`) with no build step. Open it
directly in a browser, or serve it with any static file server:

```bash
npx serve .
```

## Deployment
Deployed via Netlify, connected to this repository. Any push to `main`
triggers a new deploy automatically.

## Data privacy note
This app has no login and no access control. Treat the deployed URL as public.
If the underlying sales/inventory data is sensitive, restrict who has the link,
or enable Netlify's password protection / add an app-level password gate.

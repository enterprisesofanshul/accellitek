# Google Search Console Setup

## Step 1 — Add Property

1. Go to https://search.google.com/search-console
2. Sign in with your Google account
3. Click **"Add property"** → choose **"URL prefix"** → enter `https://accellitec.com`

## Step 2 — Verify Ownership (HTML file method, easiest with Netlify)

1. GSC will give you an HTML file like `google1234abcd.html`
2. Place that file in your Astro project's `public/` folder:
   ```
   c:\Users\Anshul\Downloads\accellitek\public\google1234abcd.html
   ```
3. Deploy to Netlify (it will be served at `accellitec.com/google1234abcd.html`)
4. Back in GSC, click **Verify**

Alternative: Use the **DNS record** method in your domain registrar — GSC gives you a TXT record to add.

## Step 3 — Submit Sitemap

Once verified:
1. In GSC left sidebar → **Sitemaps**
2. Enter: `sitemap-index.xml`
3. Click **Submit**

Your sitemap URL is: `https://accellitec.com/sitemap-index.xml`

It lists all 8 pages:
- https://accellitec.com/
- https://accellitec.com/services/
- https://accellitec.com/training/
- https://accellitec.com/webinar/
- https://accellitec.com/contact/
- https://accellitec.com/products/
- https://accellitec.com/terms/
- https://accellitec.com/refund/

## Step 4 — Request Indexing (optional, speeds things up)

In GSC → **URL Inspection** → paste each URL → click **"Request indexing"**

## Step 5 — Add OG Image

Place your social preview image (1200×630px JPG) at:
```
c:\Users\Anshul\Downloads\accellitek\public\og-image.jpg
```

This image appears when someone shares any AccelliTec page on LinkedIn or WhatsApp.

## Deploy to Netlify

1. Push this project to a GitHub repo
2. In Netlify → "Add new site" → "Import from Git" → connect repo
3. Build command: `npm run build`
4. Publish directory: `dist`
5. Netlify will auto-detect the `netlify.toml`

Or drag-and-drop the `dist/` folder directly into Netlify's deploy drop zone for a quick test.

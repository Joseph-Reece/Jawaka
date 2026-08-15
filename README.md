# Jawaka Distributors Limited — Website

Static marketing site for Jawaka Distributors Limited: poultry feeds, day-old chicks,
consultation services, a learning centre, and free farmer resources (vaccination
schedule, feeding charts, poultry house checklist, feed cost and FCR calculators).

Contact: 0715 083 866 · sales@jawaka.co.ke · Karatina, Nyeri County

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The deployed site. Add SEO head tags here. |
| `Jawaka Distributors.dc.html` | Editable design source. `index.html` is generated from this. |
| `support.js` | Runtime required by both HTML files. Do not edit. |
| `favicon.svg` | Site icon. |

`index.html` and `Jawaka Distributors.dc.html` are the same document apart from the
extra `<head>` tags in `index.html`. When you change the design, edit the `.dc.html`
source and regenerate `index.html`.

## Deploy to Cloudflare Pages

There is no build step — Cloudflare serves these files as-is.

1. Push this repository to `main` on GitHub.
2. In the Cloudflare dashboard go to **Workers & Pages → Create → Pages → Connect to Git**.
3. Authorise GitHub and select **Joseph-Reece/Jawaka**.
4. Configure the build:
   - Production branch: `main`
   - Framework preset: **None**
   - Build command: *leave empty*
   - Build output directory: `/`
5. Click **Save and Deploy**. The site goes live at `https://jawaka.pages.dev`.

Every later push to `main` redeploys automatically.

### Custom domain (when you are ready for jawaka.co.ke)

In the Pages project open **Custom domains → Set up a domain**, enter `jawaka.co.ke`,
and follow the DNS instructions Cloudflare shows. Then update the `og:url` and
`canonical` tags in `index.html` to the new address.

## Notes

- Photo and map areas are placeholders pending real photography.
- The contact form opens WhatsApp with the message pre-filled; no server or email
  service is involved.
- Resource "Download PDF" buttons currently show a confirmation only — the PDF files
  still need to be produced and linked.

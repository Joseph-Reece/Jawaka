# Jawaka Distributors Limited — Website

Static marketing site for Jawaka Distributors Limited: poultry feeds, day-old chicks,
consultation services, a learning centre, and free farmer resources (vaccination
schedule, feeding charts, poultry house checklist, feed cost and FCR calculators).

Contact: 0715 083 866 · sales@jawaka.co.ke · Karatina, Nyeri County

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole site. This is the source of truth — edit it here. |
| `support.js` | Runtime required by `index.html`. Do not edit. |
| `favicon.svg` | Site icon. |

## Editing in VS Code

`index.html` loads `support.js`, so opening the file directly over `file://` will not
work. Use the **Live Server** extension: right-click `index.html` → *Open with Live
Server*.

Structure of `index.html`:

- `<head>` — title, meta description, Open Graph tags, favicon.
- `<x-dc>…</x-dc>` — the markup for every page, top to bottom: nav, Home, About,
  Products, Consultation, Learning Centre, Farmer Resources, FAQ, Contact, footer.
  Each page sits in its own `<sc-if>` block. Styling is inline on the elements.
- `<script data-dc-script>` at the bottom — `class Component`, holding all page data
  (feed brands, articles, FAQs, vaccination schedule, feeding charts, checklist) and
  the calculator logic. Content lives in the `…Data` properties near the top of the
  class; that is usually the part you want.

Commit and push to `main` when done — Cloudflare redeploys automatically.

## Deploy to Cloudflare Pages

No build step; Cloudflare serves these files as-is.

1. Push this repository to `main` on GitHub.
2. Cloudflare dashboard → **Workers & Pages → Create → Pages → Connect to Git**.
3. Authorise GitHub and select **Joseph-Reece/Jawaka**.
4. Production branch `main` · Framework preset **None** · Build command *empty* ·
   Build output directory `/`.
5. **Save and Deploy** → live at `https://jawaka.pages.dev`.

### Custom domain (jawaka.co.ke)

Pages project → **Custom domains → Set up a domain**, enter `jawaka.co.ke`, follow the
DNS instructions. Then update the `canonical` and `og:url` tags in `index.html`.

## Still outstanding

- Photo and map areas are placeholders pending real photography.
- The contact form opens WhatsApp with the message pre-filled; no server or email
  service is involved.
- Resource "Download PDF" buttons show a confirmation only — the PDF files still need
  to be produced and linked.

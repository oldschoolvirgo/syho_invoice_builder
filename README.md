# Sing Your ❤️‍🔥 Out — Invoice Studio

A mobile-friendly, static invoice generator. No account, backend, remote fonts, analytics, or runtime dependencies. Contact and payment details are entered in Business & payment settings and saved in localStorage in the current browser. They are not in the published files. Customer and invoice details stay in memory and reset on reload; save each PDF for your records. Browser storage is not encrypted and can be cleared by browser settings or private browsing.

## Preview

Run `npm start` and open http://localhost:4173. Run `npm test` for calendar, privacy-option, and PDF structure checks.

1. Enter your business contact details and at least one payment method in Settings, then save.
2. Enter the client and whole billable hours, rounded up. Rate is fixed at $100/hour.
3. Override the invoice number or date when recreating an invoice. Due date is five calendar days after invoice date. Number and date are independent after their initial defaults.
4. Select optional address / EIN inclusion and generate the invoice.
5. Save PDF or Share invoice. Sharing requires a supported browser, HTTPS (or localhost), and an installed app that accepts PDFs. If unavailable, save and attach the PDF manually. Print is also available.

PDFs are rendered locally at 180 DPI, preserving emoji as drawn by the device. PDF text is rasterized rather than selectable. Long content flows onto additional letter-size pages. HTML preview and PDF use the same information, with the sample?s two-column PDF layout and stacked sections on small screens. Inter is bundled locally; PDF generation waits for the regular and bold font weights to load.

## GitHub Pages

Publish these static files from the repository root: `index.html`, `styles.css`, `app.js`, `core.js`, the `fonts/` folder, and `.nojekyll`. In the repository's Settings → Pages, choose Deploy from a branch, your branch, and `/ (root)`. Relative URLs also work on project Pages sites. No build step or secrets are required. The development server and tests are not needed for hosting.

Never commit filled-in business settings, customer information, or generated invoices. Publishing the site does not synchronize settings between devices. Mobile download and share behavior should be checked on your actual phone before sending a client invoice.

# KODE — QR Invitation & Access System (Prototype)

A working front-end prototype of KODE's QR invitation system.

**Live demo:** https://salmaaselimm.github.io/Kode/

## What it does
- **Import** an Excel/CSV guest list (name, email, phone, company) — columns auto-detected, duplicates skipped, invalid emails flagged
- **Issue** every guest a unique QR pass (`KODE|<eventId>|KD-XXXX-XXXX`)
- **Invite** via email / WhatsApp / SMS with editable templates and live preview
- **Auto-reply** instantly when a guest confirms or declines
- **Scan** passes at the door (photo/camera upload, manual code entry) — duplicates and fake codes rejected
- **Report** live KPIs, funnel, arrivals over time, per-company stats, and export to Excel / CSV

## Notes
- Single static `index.html` — no build step. Data is stored in the browser (localStorage).
- Message delivery is **simulated**. Production would plug into an email provider (SendGrid / SES), the WhatsApp Business API, and a backend + database for shared state.

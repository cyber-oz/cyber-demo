# cyberOZ interactive demo

One static file, `index.html`. No backend, no real data, no cookies.

## Put it on demo.cyberoz.io (Cloudflare Pages, free)
1. Cloudflare dashboard > Workers & Pages > Create > Pages > Upload assets.
2. Name the project `cyberoz-demo`, drag in this folder, deploy.
3. Custom domains > Set up a custom domain > `demo.cyberoz.io`. Cloudflare shows the CNAME record to add at your DNS provider (automatic if cyberoz.io is already on Cloudflare).

Netlify Drop (app.netlify.com/drop) works the same way: drag the folder in, then add the domain.

## Change before sending
- Booking buttons: `BOOKING_URL` in `index.html` points to https://calendly.com/iliademko-cyberoz/30min. Bookings carry utm_source=cyberoz-demo, and personal links add the ?ref name as utm_content, so Calendly shows which prospect booked.
- Analytics: uncomment the Plausible line in the head after adding the site in Plausible.

## Personal links
`https://demo.cyberoz.io/?ref=Acme` shows "Prepared for Acme" in the top bar. Plausible lists `ref` as the visit source, so you see which prospect opened it and when.

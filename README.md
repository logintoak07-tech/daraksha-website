# Daraksha Overseas LLP - Website

Static website (HTML + CSS + JavaScript). No build step, no database.

## Folder layout
- index.html              - the whole site (single page)
- assets/css/style.css    - design
- assets/js/config.js     - YOUR phone, email, address, form settings (edit this)
- assets/js/main.js       - menu, animations, form logic
- images/                 - logo, favicon, photos
- favicon.ico             - browser tab icon

## 1. Fill in your details (2 minutes)
Open assets/js/config.js and add phone, email, office address, hours and the form endpoint.
Anything left empty is hidden automatically.

## 2. Publish (pick one)
**Cloudflare Pages / Netlify (recommended, free HTTPS)**
1. Create a free account.
2. Choose "Add new site" > "Deploy manually / Direct upload" and drag in this folder (or the ZIP).
3. In the site's "Custom domains" section add your domain (and www).
4. At your domain registrar, add the DNS records the host shows you:
   - A record (or CNAME / nameservers) for the root domain
   - CNAME for www
5. Wait for DNS to update (usually minutes to a few hours, up to 48 hours). HTTPS turns on automatically.

**cPanel / FTP hosting**
Upload everything inside this folder to public_html/ so index.html sits at the top level.

## 3. Make the enquiry form work
Create a free endpoint at Formspree or Web3Forms, then paste the URL into formEndpoint in config.js.
Submissions arrive in your mailbox. If you leave formEndpoint empty, the form opens the visitor's
email app addressed to your email instead.

## 4. Business mailbox on your domain (e.g. info@yourdomain.com)
Email is separate from the website and can live in the same DNS zone.
1. Choose a provider: Microsoft 365 Business, Google Workspace, or Zoho Mail (has a free tier).
2. Add your domain in the provider's admin portal and create the mailbox.
3. Verify ownership by adding the TXT record they give you in your domain's DNS.
4. Add the mail records they give you:
   - MX - routes incoming mail
   - SPF (TXT) - authorises the provider to send for you
   - DKIM - signs outgoing mail
   - DMARC (TXT) - protects against spoofing
5. Send and receive a test mail, then add the account to Outlook / your phone.
6. Put the address in config.js (email).

## Notes
- Photos are AI-generated illustrations. Replace files in images/ with real photos of your team,
  testing centres and deployments when available (keep the same file names).
- Fonts load from Google Fonts; the site falls back to system fonts if offline.
- Add registration/licence numbers, testimonials and real figures only when you can document them.

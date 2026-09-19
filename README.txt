ARR HOMES — WEBSITE PACKAGE (built on your Crafto "Architecture" template)
============================================================================

WHAT THIS IS
------------
This site is built from the "Architecture" demo inside your Crafto ThemeForest
template — the best-fitting of its 56 demos for a construction/building
business. It has been fully re-branded and re-colored for ARR Homes:

- Accent color changed from the demo's lime-yellow to your logo's gold
  (#C79A34), dark tone changed to a true near-black (#0B0B0A)
- Headings set in Bodoni Moda to echo your logo's serif lettering
- Your logo swapped in everywhere (white/black variants generated for
  dark vs light headers)
- Every page's text, images, team members, project examples, testimonials,
  and contact details replaced with ARR Homes content — no leftover
  "Crafto", "Lorem ipsum", or placeholder images anywhere on the site
- Working image gallery filters on the Projects page (New Homes / Extensions
  / Renovations / Outdoor Living) using the theme's built-in filter system

WHAT'S INSIDE
-------------
index.html            Homepage
about/index.html       About page (story, timeline, team)
services/index.html    Services page (6 services, process, FAQs)
projects/index.html    Projects/portfolio page with filterable gallery
contact/index.html     Contact page with quote request form
css/, js/, fonts/       Theme assets (trimmed to only what these 5 pages use)
demos/architecture/     Theme's demo-specific stylesheet, recolored for ARR Homes
images/                 Your logo (in white/black variants) + small theme assets
email-templates/        PHP contact form handler (see FORM SETUP below)
robots.txt, sitemap.xml SEO files
404.html                Custom "not found" page
.htaccess, netlify.toml, vercel.json   Clean-URL configs for common hosts

Note: most photos across the site are high-quality stock photos (Unsplash)
used for layout purposes — see "BEFORE YOU GO LIVE" below.

CLEAN URLS (NO .html)
----------------------
Every page lives in its own folder as "index.html" (e.g. about/index.html),
so a browser shows:
    yourdomain.com.au/about/
instead of:
    yourdomain.com.au/about.html
This works automatically on Netlify, Vercel, and any standard Apache/Nginx
host. The .htaccess file is included for Apache hosts (most cPanel/GoDaddy
plans) to also redirect old-style ".html" links to the clean version.

FORM SETUP
----------
The contact form posts to /email-templates/contact-form.php, which is the
PHP mailer that ships with your Crafto template. It's pre-configured to send
enquiries to hello@arrhomes.com.au using PHP's built-in mail() function.

This ONLY works if your hosting supports PHP (most shared hosting does;
Netlify and Vercel's free static hosting do NOT run PHP). If you're hosting
on Netlify or Vercel, you have two options:
  1. Switch the form to Netlify Forms (add data-netlify="true" to the <form>
     tag in contact/index.html), or
  2. Use a service like Formspree and point the form's "action" at their
     endpoint instead.
For higher deliverability than PHP mail(), open email-templates/contact-form.php
and fill in the SMTP block (search for YOUR_SMTP_HOST) with your email
provider's SMTP details.

GOOGLE MAP ON THE CONTACT PAGE
--------------------------------
The map on the Contact page needs a Google Maps API key to render. Open
contact/index.html, find this line near the bottom:
    <script async defer src="https://maps.googleapis.com/maps/api/js?key=<YOUR_API_KEY>&callback=initMap"></script>
and replace <YOUR_API_KEY> with a key from the Google Cloud Console
(Maps JavaScript API). The map is already centered on Melbourne CBD —
update the lat/lng in the same file if your office is elsewhere.

BEFORE YOU GO LIVE
-------------------
1. Replace placeholder business details:
   - Phone number, email, and office address (currently placeholders)
   - Building licence number (currently CDB-U 00000 — placeholder)
   - Team member names/photos (about/index.html) — currently Unsplash
     stock photos standing in for Anthony, Rob, Rhys and Maya
   - Social media links in the footer

2. Swap stock photography for real job-site photos. Every project photo,
   hero image, and team photo across the site is a stock photo from
   Unsplash used for layout — replacing these with real ARR Homes project
   photography is the single highest-impact thing you can do, both for
   credibility and for Google image search / local SEO.

3. Point your domain at wherever you host this (Netlify, Vercel, or any
   standard PHP-capable web host if you want the contact form to work
   out of the box).

SEO WORK ALREADY DONE
-----------------------
- Unique, descriptive <title> and meta description on every page
- Canonical URLs on every page
- Open Graph tags for social sharing
- Structured data (schema.org): GeneralContractor, BreadcrumbList
- Semantic HTML with proper heading hierarchy and alt text on every image
- robots.txt + sitemap.xml
- Mobile-responsive (this theme is Bootstrap 5 based)

SEO WORK YOU STILL NEED TO DO (a website alone can't rank you)
------------------------------------------------------------------
- Submit the sitemap in Google Search Console
- Set up and verify a Google Business Profile for local "near me" searches
- Get listed on Master Builders Victoria, hipages, Houzz etc. with matching
  name/address/phone (NAP consistency)
- Collect real Google reviews
- Publish real project photos and case studies over time

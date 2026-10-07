SKILLWIZ 2.0 WEBSITE · CUSTOMER REVIEW BUILD v1.0
=================================================
Static site: plain HTML, CSS and JavaScript. No build step, no database.

FOLDER MAP
index.html ............ page structure and all fixed copy (headlines, paragraphs, contact details)
assets/css/style.css .. all styling; brand colours and fonts are the variables in :root at the top
assets/js/main.js ..... all dynamic content, in labelled blocks:
    CONFIG ............ slide timings (heroSeconds, journeySeconds, autoplay)
    J ................. the eight journey stages (name, headline, supporting line)
    D ................. Industry pulse data: one entry per sector (figures, news links,
                        investments, roles, streams, CTA, audience messages)
    PEND .............. sectors still awaiting data (Chip design, Autonomous driving)
    BOT ............... Wiz assistant quick answers; askWiz() is where a live AI backend connects
    platform layers, stakeholder roles and the 13-product portfolio are arrays further up
assets/images/ ........ hero, platform, journey, karm-patri, eutp, proof, logos
assets/video/ ......... hero-1.mp4 ... hero-4.mp4, journey-bg.mp4 (+ optional .vtt captions)
assets/icons/ ......... favicons and apple-touch-icon
robots.txt, .htaccess . review-stage privacy, compression and caching

NAMING CONVENTIONS
Lowercase, hyphen-separated, no spaces. Numbered sets use -1, -2. Add the pixel width to images
(e.g. eutp-incubation-bench-1600.webp). Video: hero-N.mp4, journey-bg.mp4, captions share the name (.vtt).

UPLOAD TO HOSTINGER
1. hPanel > Websites > Manage > File Manager > public_html
   (for a review link, first create a subdomain such as review.yourdomain.com and open its folder).
2. Upload this zip and use Extract. The zip has no outer folder, so index.html lands directly in the target
   folder. If you see an extra folder, move its contents up one level.
3. Turn on "Show hidden files" so .htaccess is visible.
4. Optional: hPanel > Websites > Password protect directory, so only your customer can open it.
5. Open the URL and hard refresh (Ctrl+Shift+R).

EDITING GUIDE
Change slide timing .......... assets/js/main.js, CONFIG at the top (or data-seconds="4" on a <section class="car">)
Edit hero messages ........... index.html, section id="hero" (four .slide blocks)
Edit journey messages ........ main.js, array J
Update an industry figure .... main.js, object D, then change the value and the "note" source line. Add the source and date.
Add a new sector ............. copy any entry in D and rename it; remove the name from PEND if it is listed there
Edit bot answers ............. main.js, object BOT
Replace a placeholder ........ index.html, find <div class="ph"> and replace the block with:
  Image: <img src="assets/images/eutp/eutp-incubation-bench-1600.webp" alt="Describe the image" width="1600" height="1200" loading="lazy" style="width:100%;height:auto;border-radius:20px;aspect-ratio:4/3;object-fit:cover">
  Video: <video poster="assets/video/hero-poster.webp" controls playsinline preload="none" style="width:100%;border-radius:20px;aspect-ratio:16/9"><source src="assets/video/hero-1.mp4" type="video/mp4"></video>
News screenshots in Industry pulse are placeholders; their image slots are generated in main.js (class "ph"), so
add the images through the sector data when you have licensed or captured them.

MEDIA SPECS (deliver at 2x)
Hero and journey videos 1920x1080 H.264, muted loops; hero under 5 MB each
Platform visual 1200x900; Karm-Patri illustration 1200x1200; EUTP photo 1600x1200 (WebP, under 200 KB)
News screenshot 1200x750; logo walls 760x380 one-colour SVG; social share 1200x630 JPG

BRAND RULES (Brand Bible Vol. II)
Five colours only (Saffron, Deep Forest, Warm Cream, Charcoal; Mustard max 5%). Anton uppercase for display, Manrope for body.
No gradients, outlines or shadows on the logo. Replace the text logo with the official SVG; keep one W of clear space.

FIGURES TO VERIFY BEFORE GOING LIVE
Defence FY2023-24 exports (21,083 crore): confirm against the Ministry of Defence release.
Robotics: the 500 crore MeitY humanoid fund is "as reported"; confirm with MeitY. Confirm the 2025 robot count against IFR.
Every sector's "Checked" date is in its source note; refresh these on each update.

BEFORE GOING LIVE
Delete robots.txt contents and remove the noindex meta tag in index.html.
Connect the contact form (it only shows a confirmation now), add a privacy policy, add official logo and favicons.
Wiz assistant currently gives scripted answers only.

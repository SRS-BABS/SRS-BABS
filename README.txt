Bachmann-Bupp Family Coalition website
Live at https://bachmann-bupp.org (since 11 November 2026; HTTPS enforced since 13 November 2026)

What this repository is
  The whole public site. GitHub Pages serves the root of the main branch.
  Repository: SRS-BABS/SRS-BABS (owned by the Snyder-Robinson Foundation account; site editor: Menachem Handler)

Files
  index.html          the site (a single self-contained page; all pages are built inside it)
  assets/docs/        ICPD-programme-2026.pdf
  assets/video/       coalition-2 and roberto clips (.mp4, .webm, -poster.jpg)
  robots.txt          allows search engines; points to the sitemap
  sitemap.xml         the site address for search engines
  CNAME               one line: bachmann-bupp.org.  DO NOT DELETE OR EDIT. Removing it takes the domain offline.
  .nojekyll           tells GitHub Pages to serve files as they are
  README.txt          this file

Updating the site
  Replace index.html (and add any new files under assets/) through "Add file > Upload files" on main.
  Changes appear on bachmann-bupp.org within a few minutes.
  Do not change CNAME, and do not change the Pages settings.

Domain and DNS (bachmann-bupp.org, registered and managed at Squarespace Domains)
  A     @    185.199.108.153
  A     @    185.199.109.153
  A     @    185.199.110.153
  A     @    185.199.111.153
  CNAME www  srs-babs.github.io
  The "Squarespace Domain Connect" and "Email Security" records are left in place.
  www and http:// both forward to https://bachmann-bupp.org.

Security certificate
  Issued automatically by GitHub (Let's Encrypt) and renewed automatically.
  If it ever stops working: in Settings > Pages (owner account only), remove the custom domain,
  add bachmann-bupp.org again, wait for "DNS check successful", then tick "Enforce HTTPS".

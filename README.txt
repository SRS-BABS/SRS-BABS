BABS website — deploy package (built 9 October 2026 from the 23 September export)

Contents
  index.html                       the site (the standalone export, renamed)
  assets/docs/ICPD-programme-2026.pdf
  assets/video/coalition-2.mp4 / .webm / -poster.jpg
  .nojekyll                        tells GitHub Pages to serve files as-is

Staging (no custom domain yet)
  Repository: https://github.com/SRS-BABS/SRS-BABS  (created by Chris Abbott; must be PUBLIC —
  GitHub Pages on a private repo needs a paid plan).
  1. Upload everything in this folder to the root of that repository (keep the assets/ folder structure).
  2. Settings -> Pages -> Build and deployment: Source = "Deploy from a branch", Branch = main, folder = / (root). Save.
  3. After a minute or two the staging site is at  https://srs-babs.github.io/SRS-BABS/
     (a "project site": the repo name is part of the path until a custom domain is attached).
     Do NOT add a CNAME file or a custom domain at this stage.

Cutover (only after written approval from Michael and Sofia)
  4. Settings -> Pages -> Custom domain: bachmann-bupp.org -> Save (GitHub creates the CNAME file itself).
  5. In the Squarespace domain panel (Domains -> bachmann-bupp.org -> DNS settings):
       FIRST screenshot the current records (that screenshot is the rollback). Then delete the Squarespace default records for @ (A) and www (CNAME), then add
       A     @    185.199.108.153
       A     @    185.199.109.153
       A     @    185.199.110.153
       A     @    185.199.111.153
       CNAME www  srs-babs.github.io      (the account host only, never the repo name)
  6. Back in GitHub Pages, wait for the DNS check to pass, then tick "Enforce HTTPS" (may take up to 24 h to become available).
  7. Verify https://bachmann-bupp.org and https://www.bachmann-bupp.org both load the site with a valid certificate; log it.

Rollback
  Delete the GitHub records, re-enter the Squarespace records exactly as in the screenshot taken at step 5, and remove the custom domain in GitHub Pages.

Known gap carried in still-needed.html
  The <video> element in index.html has no <source> tags (left as a comment in the Design build), so the clip will not play until the next Design export adds:
     <source src="assets/video/coalition-2.webm" type="video/webm">
     <source src="assets/video/coalition-2.mp4"  type="video/mp4">

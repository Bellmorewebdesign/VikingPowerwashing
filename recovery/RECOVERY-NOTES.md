# Viking Power Washing website recovery

Recovered September 6, 2026 from the Internet Archive's Wayback Machine.
Original domain: https://vikingpowerwashingli.com/

## Result

The original public frontend is partially recovered. This is actual archived HTML,
CSS, JavaScript, and image data, not a newly generated recreation. It is useful as
a starting point for restoring or rebuilding the website, but is not ready to
publish as-is.

`original-site/` contains 28 recovered files:

- Five distinct pages: Home, About Us, Services, Working Gallery, and Contact.
- One additional capture of the root homepage. `homepage-root-snapshot.html`
  is the February 27, 2025 root-URL capture; `index.html` is the January 17,
  2025 explicit index capture. The recovered contents are identical.
- Two CSS files: `style.css` and `vendor.min.css`.
- Two JavaScript files: `functions.js` and `vendor.min.js`.
- Eighteen images and graphics, including the mobile logo, favicon, homepage
  hero photograph, two other large photographs, backgrounds, and service icons.

The separate Testimonials navigation item points to a homepage section.
The page HTML was captured in January and February 2025; recovered assets were
captured March 1, 2024. These are mixed-date archival copies and may not represent
the site's last version before the outage. No live hosting files were obtained.

## What is missing

- All 39 gallery photographs referenced by `work-gallery.html`.
- Several additional photographs, backgrounds, decorative graphics, and the
  desktop logo file. A mobile logo image is recovered.
- The local jQuery 3.6.0 dependency. This is a standard public library that can be
  supplied again; it is not the developer's private code.
- Locally referenced icon fonts and some other template assets. Several font
  references are alternate formats or may belong to unused template styles.
- `assets/php/contact.php`, the server-side estimate form handler. Public
  archives cannot recover PHP source just by requesting the page. Rebuild the
  form processing using a new, verified destination.

`missing-files.json` lists 97 unresolved local paths found in active HTML
attributes and CSS URLs. That includes unused template assets and alternative
font formats; it does not mean 97 separate visible features are broken.
The scan is not exhaustive for dynamically constructed JavaScript paths.

## Notes for Claude or another developer

1. Keep `original-site/` as the reference copy. Work in a separate project.
2. For a faithful restoration, restore jQuery before the two recovered scripts,
   replace missing fonts/icons and images, and test the page interactions. The
   existing preloader may obscure the page while jQuery is missing.
3. Ask the client for the original logo and job photos. The recovered mobile logo
   may be a useful reference, but do not present it as the missing desktop file.
4. Rebuild the estimate form and verify its recipient before enabling submission.
   The visible form markup alone does not deliver requests.
5. Review the old Google Analytics ID before reusing it. The original archive
   preserves `G-927JK6PB94`; ownership/access has not been verified.
6. Check phone/email, hours, services, testimonials, and marketing claims with
   the client before publication. The old copy's licensing/insurance and other
   claims are historical site content, not independently verified facts.
7. Repair the malformed Google Fonts hostname containing a tab in the homepage
   source, review the leftover `page-about.html` link, and update canonical URLs
   if a different domain is selected.
8. Test desktop/mobile navigation, image loading, gallery, and estimate form in
   the completed project before publishing. This recovery package has not been
   browser-validated as a functioning site.

The original page files and JavaScript retain their old analytics and form
behavior. Nothing has been deployed or connected to a new domain in this work.

## Domain and outage findings

The Verisign .com registry RDAP response retrieved September 6, 2026 reports:

- Registrar: HOSTINGER operations, UAB.
- Registered: May 11, 2022.
- Expires: May 11, 2027 at 12:08:39 UTC.
- Nameservers: `ns1.dns-parking.com` and `ns2.dns-parking.com`.
- Status: `client transfer prohibited`.

Google Public DNS and Cloudflare DNS both returned NOERROR with no A or AAAA
answer for the root domain. `www` was a CNAME to the root, also without a usable
A answer. This establishes a current DNS problem; it does not prove why records
are missing, whether hosting was canceled, or whether the original files still
exist on the host. Requests for the live site's HTTP/HTTPS variants failed.

The expiry date does not establish who controls the account or whether recurring
payments were canceled. Public data did not identify the actual account holder.
Hostinger has an account-recovery process requiring evidence of ownership. That
could be worth trying if the client can prove the account is theirs; it does not
guarantee access to an agency-owned account. A new domain can be used independently
of recovering the old code. Recovering the old domain later could allow redirects.

## Sources and verification

- Latest root capture: https://web.archive.org/web/20250227045737/https://vikingpowerwashingli.com/
- Archive index: https://web.archive.org/cdx/search/cdx?url=vikingpowerwashingli.com%2F*&output=json&filter=statuscode:200
- Registry record: https://rdap.verisign.com/com/v1/domain/vikingpowerwashingli.com
- Hostinger account recovery instructions: https://www.hostinger.com/support/3284259-how-to-recover-your-hostinger-account-if-you-can-t-access-your-email/

`recovery-manifest.json` records original URLs, capture timestamps, download URLs,
file sizes, and SHA-256 hashes. Downloads used Wayback's `id_` mode to avoid its
navigation toolbar and URL rewriting; gzip transport encoding was decompressed.
No recovery edits were applied to the original page or asset contents.
`evidence/` includes the archive index, registry response, and DNS responses.

# VidLimit website

Static site for vidlimit.com. Plain HTML and CSS: no frameworks, no build step, no JavaScript, no cookies, no analytics.

## Structure

```
index.html            /          landing page
support/index.html    /support/  contact email and FAQ
privacy/index.html    /privacy/  privacy policy
style.css             shared styles
favicon.ico           root favicon (also linked from every page)
assets/               favicons, lockup, hands logo, social image (og-image.png)
robots.txt, sitemap.xml
```

Brand assets are copied from `vidlimit/brand/` in the app repo (`web/`, `logo/`). Colours: navy `#0B1B3A`, amber `#FFB020`, white.

Preview locally: `python3 -m http.server` in this folder, then open http://localhost:8000/.
Deploy by uploading the folder contents as-is to any static host.

## Keep in sync with the app

The pages make factual claims about the app (free tier of 5, $9.99 one-time unlock, 0.5 to 2000 MB custom range, presets, macOS 15 minimum, no network entitlement, privacy manifest contents, Help-menu URLs `/support` and `/privacy`). When the app changes, update the site in the same sitting, and the other way round. Source of truth: the app repo's `README.md`, `PROJECT.md` and `PrivacyInfo.xcprivacy`.

Open items are marked with `TODO` comments in the HTML (`grep -rn TODO --include=*.html .`). The "Coming soon" line on the landing page must be replaced with a real Mac App Store link, using Apple's official badge guidelines, only once the app is live.

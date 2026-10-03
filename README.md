# DuDu Publisher — Official Static Site

Official website for **DuDu Publisher**, the desktop publishing tool used by
**Learn Chinese with DuDu**.

This repository contains nothing but static HTML and CSS. It is intended for
TikTok Developer App review (Sandbox / Production) as the app's public website
URL, and for anyone who wants to read the policies before authorizing the app.

---

## App details

| | |
| --- | --- |
| App name | DuDu Publisher |
| Category | Education |
| Description | A desktop publishing tool for uploading original Learn Chinese with DuDu videos to TikTok. |

DuDu Publisher uses the **TikTok Login Kit** to authorize a TikTok account and
the **TikTok Content Posting API** to upload and publish original Learn Chinese
with DuDu videos.

It does not sell user data, and it is not used for third-party user marketing,
bulk/spam posting, or unauthorized account operation.

This site makes **no claim of official TikTok endorsement or partnership**, and
it carries **no TikTok logo, no analytics, no cookies, and no third-party
scripts or CDNs**.

---

## Files

```
DUDU_PUBLISHER_SITE/
  index.html       Home — what DuDu Publisher is and what it connects to
  privacy.html     Privacy Policy   (Last updated: October 4, 2026)
  terms.html       Terms of Service (Last updated: October 4, 2026)
  style.css        Single stylesheet, responsive, no framework
  README.md        This file
```

No JavaScript is used anywhere on the site.

---

## Expected URLs after deployment

- Home: <https://rockflyde.github.io/dudu-publisher/>
- Privacy Policy: <https://rockflyde.github.io/dudu-publisher/privacy.html>
- Terms of Service: <https://rockflyde.github.io/dudu-publisher/terms.html>

---

## Deploying to GitHub Pages

Manual upload (simplest):

1. Create a new public GitHub repository named **`dudu-publisher`** under the
   account `rockflyde`.
2. Upload `index.html`, `privacy.html`, `terms.html`, and `style.css` directly
   into the repository root (not inside a subfolder).
3. Open **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Set **Branch** to `main` (or `master`) and folder to `/ (root)`, then
   **Save**.
6. Wait for the deployment to finish (the Actions run shows a green check).
7. Visit <https://rockflyde.github.io/dudu-publisher/>.

Deployment from a branch (Git):

```sh
git init
git add index.html privacy.html terms.html style.css README.md
git commit -m "DuDu Publisher static site"
git branch -M main
git remote add origin https://github.com/rockflyde/dudu-publisher.git
git push -u origin main
```

Then follow steps 3–7 above.

> The URL `https://rockflyde.github.io/dudu-publisher/` is the **expected**
> URL and requires the repository to be named exactly `dudu-publisher` and be
> owned by the `rockflyde` account. If the site is instead deployed at the
> account level (repository named `<account>.github.io`), the pages would be
> served from the account root instead.

---

## Custom domain (optional)

If a custom domain is used later, add a `CNAME` file at the repository root
containing the domain, and configure the domain with your DNS provider. No
change to the HTML is required.

---

## Security and secrets

- This site requires **no OAuth Client Secret** and contains no credentials.
- It never reads, stores, or asks for a password, token, or secret.
- No configuration file is needed to serve it.

---

## Local preview

Open `index.html` directly in a browser, or serve the folder locally:

```sh
python -m http.server 8000
# then visit http://localhost:8000/
```

---

## Scope

These files are self-contained. They do not touch, import from, or depend on
`DUDU_VIDEO_FACTORY_V1`, `DUDU_PUBLISHER_V1`, or any TEST* project files.

---

## Disclaimer

DuDu Publisher is an independent project created for the Learn Chinese with
DuDu project. It is **not affiliated with, endorsed by, or sponsored by
TikTok or ByteDance**.

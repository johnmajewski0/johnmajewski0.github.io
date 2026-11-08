# jmajewski.dev — J. Clark Mulhall

A typography-forward, academic/professional portfolio for J. Clark Mulhall. Static HTML/CSS/JavaScript; built to publish directly on **GitHub Pages**, without a build step, npm, or server.

## Contents

- `index.html` — all on-page content, search engine metadata, and links
- `assets/styles.css` — typography, colors, layout, and mobile styles
- `assets/main.js` — mobile nav and automatic copyright year
- `assets/clark-portrait.webp` — optimized portrait adapted from supplied office photo
- `assets/social-preview.jpg` — open graph/social sharing image
- `assets/favicon.svg` — JCM favicon
- `CNAME` — custom-domain declaration (`jmajewski.dev`)
- `.nojekyll` — publishes this static site without Jekyll processing
- `sitemap.xml` and `robots.txt` — basic search engine discovery

## Preview locally

Double-click `index.html`, or use a local server in this directory:

```powershell
py -m http.server 8000
```

Open `http://localhost:8000/`.

## Publish on GitHub Pages

1. Sign in to GitHub.com. Create a **public** repository named `johnmajewski0.github.io`, where `johnmajewski0` is your actual GitHub handle. You can also use another repository name and publish via GitHub Pages; this package uses relative paths, so either works.
2. Place **the contents** of this folder (not an extra enclosing folder) at repository root. Preserve `CNAME` and `.nojekyll`.
3. Commit/push to the `main` branch.
4. In the repository, choose **Settings → Pages → Build and deployment → Deploy from a branch → main → /(root) → Save**.
5. In **Settings → Pages → Custom domain**, type `jmajewski.dev`, then save. GitHub recommends verifying your domain ownership first. Keep `CNAME` committed at repository root.
6. At your domain's DNS host, create four **A** records for `@`, with target values:

   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`

7. For `www.jmajewski.dev`, create a **CNAME** record: host `www`, target `johnmajewski0.github.io` (replace johnmajewski0 with your own GitHub account name). GitHub can redirect `www` to the apex domain.
8. Allow DNS/certificate provisioning time. Return to **Settings → Pages** and turn on **Enforce HTTPS** once it becomes available.

**Important DNS note:** If your domain currently has active website records, changing `@` A records will replace that website routing. Preserve existing MX, SPF, DKIM, DMARC, and other mail-related DNS records; do not delete them. Do not add wildcard CNAME records.

**Optional check on Windows PowerShell**:

```powershell
Resolve-DnsName jmajewski.dev -Type A
Resolve-DnsName www.jmajewski.dev -Type CNAME
```

GitHub documentation:
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Before publishing: content review

- The name **J. Clark Mulhall**, credentials, background, and subject expertise follow the project brief. Verify how you want your credentials displayed before publishing.
- Contact buttons use **vanya@jmajewski.dev**. Confirm the mailbox is active before publishing.
- The portfolio deliberately does **not** identify an employer, patient information, confidential client systems, claim unpublished papers, or fabricate project impact metrics.
- Optional: add links to a current CV, public GitHub code, professional profile, and published papers **only when you have confirmed destinations**.
- The supplied portrait is a user-provided image; remove/replace if you prefer to keep that photo private.

## Editing

For content: search for relevant heading text in `index.html`, then edit it in place. For colors: the CSS custom properties at the top of `assets/styles.css` control the theme. No dependencies or compilation are necessary.

## Privacy and accuracy

The website does not publish the residential address or telephone number from the résumé. The paused doctoral study is intentionally omitted, and planned papers are described as work in development, not accepted publications. Before switching any repositories to public, audit all commit history for credentials and confidential employer data.

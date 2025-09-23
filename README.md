# NextGen HERoes — Netlify deploy

Upload this **folder** to Netlify (Deploys → Upload deploy). The folder root must contain:
- `index.html`
- `_redirects`
- `_headers`
- `404.html`
- `images/…`

### Customizations
- Update the Google Form link in `index.html`:
  ```js
  const SIGNUP_FORM_URL = "https://forms.gle/your-real-form-link";
  ```
- Replace `images/olivia.jpg` and `images/wenbo.jpg` with real square photos.

### Custom domain
Point your DNS to Netlify, then click **Retry DNS verification** in Domain management:
- CNAME `www` → your-site-name.netlify.app
- ALIAS/ANAME `@` → your-site-name.netlify.app (or the A records Netlify provides)

### Why `_redirects`?
It routes every path to `/index.html` so deep links work in this single-page site.

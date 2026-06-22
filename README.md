# aisee-glasses-docs

Public, thin GitHub Pages wrapper that fronts the **gated** AiSee Glasses SDK
documentation at a memorable URL: **https://docs.glass.aisee.ai**.

`index.html` embeds the team-only Apps Script portal
(`aisee-glasses-docs-appscript`) in a full-page iframe, with an "Open in new tab"
fallback for when the visitor isn't yet signed in (Google's login page can't be
framed). The actual content + access control live in the Apps Script web app —
this repo is just branding + the custom domain.

- Custom domain: `docs.glass.aisee.ai` (CNAME → `aisee-ai.github.io`), set via the
  `CNAME` file. Served by GitHub Pages from `main` / root.
- Access is enforced by the Apps Script app (aisee.ai domain + allowlist), not by
  this public page.

To change which deployment is embedded, edit `APP_URL` in `index.html`.

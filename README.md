# Cutpath — website (privacy &amp; support)

Static pages for the **Cutpath** iOS app, hosted on GitHub Pages.

- `index.html` — landing page
- `privacy.html` — Privacy Policy (used in App Store Connect **and** linked inside the app)
- `support.html` — Support page (used in App Store Connect)

No app source lives here — only these static pages. (This local folder is named
`cutpath-site/`; the GitHub repo it publishes to is named **`cutpath`**.)

## Publish to GitHub Pages

1. You've created the **public** repo **`cutpath`** (owner `maxdmaxwell`). Push this folder to it:
   ```sh
   cd cutpath-site
   git remote add origin https://github.com/maxdmaxwell/cutpath.git
   git branch -M main
   git push -u origin main
   ```
   *(Or, in the browser: on the new repo choose "uploading an existing file" and drag in
   `index.html`, `privacy.html`, `support.html`, `README.md`, then commit to `main`.)*
2. In the repo, go to **Settings → Pages → Build and deployment** and set
   **Source: "Deploy from a branch," Branch: `main` / `/ (root)`**, then **Save**.
3. Wait ~1 minute for the first build. Your pages go live at:
   - Privacy: `https://maxdmaxwell.github.io/cutpath/privacy.html`
   - Support: `https://maxdmaxwell.github.io/cutpath/support.html`
   - Home:    `https://maxdmaxwell.github.io/cutpath/`

## Where these URLs go

| URL | Paste into |
| --- | --- |
| `…/cutpath/privacy.html` | App Store Connect → **App Privacy → Privacy Policy URL** |
| `…/cutpath/support.html` | App Store Connect → **App Information → Support URL** |

The app's paywall "Privacy" link already points at the privacy URL above
(`Legal.privacy` in `Cutpath/Views/PaywallView.swift`).

> The repo must be **public** for GitHub Pages to serve it on the free plan.

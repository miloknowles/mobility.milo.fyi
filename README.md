## Publishing with Quartz

This vault is the source of truth. It contains only markdown, and [Quartz](https://quartz.jzhao.xyz) is pulled in at build time, so the vault never holds Quartz's Node project.

### How it works

- Write and edit in Obsidian, then commit and push to `main`.
- A GitHub Action clones Quartz, copies this vault into Quartz's `content/` folder, builds the site, and deploys it to GitHub Pages.
- Folders listed in `ignorePatterns` (e.g. `private/`, `templates/`) are never published. Personal test logs go in `private/`.

### One-time setup

1. This folder is the git repo (`git@github.com:miloknowles/mobility.milo.fyi.git`). Commit and push to `main` to publish.
2. In the repo, go to **Settings → Pages → Source** and select **GitHub Actions**.
   - Custom domain: in your DNS, add a `CNAME` record from `mobility` to `miloknowles.github.io`. Then enter `mobility.milo.fyi` under **Settings → Pages → Custom domain** and tick **Enforce HTTPS**. Deploying through Actions doesn't need a `CNAME` file in the repo.
3. Add `.github/workflows/publish.yml`:
   ```yaml
   name: Publish
   on:
     push:
       branches: [main]
   permissions:
     contents: read
     pages: write
     id-token: write
   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v4
           with: { path: vault }
         - uses: actions/checkout@v4
           with: { repository: jackyzha0/quartz, ref: v4, path: quartz }
         - uses: actions/setup-node@v4
           with: { node-version: 22 }
         - run: |
             cd quartz && npm ci
             rm -rf content && mkdir content
             rsync -a --exclude '.git' --exclude '.github' --exclude '.obsidian' ../vault/ content/
             cp ../vault/quartz.config.ts . 2>/dev/null || true
             npx quartz build
         - uses: actions/upload-pages-artifact@v3
           with: { path: quartz/public }
     deploy:
       needs: build
       runs-on: ubuntu-latest
       environment: { name: github-pages }
       steps:
         - uses: actions/deploy-pages@v4
   ```
4. Copy Quartz's `quartz.config.ts` into the vault root and set `baseUrl: "mobility.milo.fyi"`, along with the site title, theme and `ignorePatterns`. The workflow uses this file if it's present.

### Local preview

```bash
git clone -b v4 https://github.com/jackyzha0/quartz.git ~/quartz && cd ~/quartz && npm ci
npx quartz build --serve --directory /path/to/this/vault   # http://localhost:8080
```

### Mobile / PWA

The site is responsive by default. To make it installable as a home-screen app, add a `manifest.json` and an icon to Quartz's `static/` folder and link the manifest in the page head (TODO).

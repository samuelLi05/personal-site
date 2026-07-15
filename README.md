# Personal Portfolio

A static personal portfolio site for GitHub Pages. The site is intentionally build-free: `index.html`, `styles.css`, `script.js`, and the pages in `projects/` are served directly from the repository root.

It is organized around a homepage with research, projects, experience, and contact sections, along with dedicated writeups in `projects/` for work that needs more architectural or technical detail.

## Structure

- `index.html`: homepage and primary sections
- `styles.css`: site styling and responsive layout
- `script.js`: small client-side interactions
- `projects/`: standalone project and research pages
- `assets/`: images and supporting media

## Run Locally

No build step or package installation is required. From the repository root, run:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000> in a browser. Stop the server with `Ctrl+C`.

Opening `index.html` directly also works for basic viewing, but the local server more closely
matches GitHub Pages and avoids browser restrictions that can affect local files.

## Deploy to GitHub Pages

This repository is intended to be deployed as a project site:

- GitHub repository: <https://github.com/samuelLi05/personal-site>
- Published site: <https://samuelli05.github.io/personal-site/>
- Publishing branch and folder: `main` and `/ (root)`

To deploy it for the first time:

1. Push the site to the `main` branch:

   ```sh
   git add .
   git commit -m "Update portfolio site"
   git push origin main
   ```

   The remote should point to `https://github.com/samuelLi05/personal-site.git`. Check it with
   `git remote -v`; if needed, correct it with:

   ```sh
   git remote set-url origin https://github.com/samuelLi05/personal-site.git
   ```

2. Open the repository on GitHub and go to **Settings > Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Select the `main` branch and `/ (root)` folder, then click **Save**.
5. Wait for GitHub to finish the Pages deployment, then use the published URL shown in the
   Pages settings: <https://samuelli05.github.io/personal-site/>.

Later updates only require committing and pushing to `main`; GitHub Pages will redeploy them
automatically. The repository name is part of this project's URL. To publish at
`https://samuelli05.github.io/` instead, rename the repository to `samuelLi05.github.io` and
update the Git remote to match the new repository name.

All internal links use relative paths, so they work both locally and under the `/personal-site/`
URL prefix. If a custom domain is added later, configure it under **Settings > Pages > Custom
domain** before changing DNS records.

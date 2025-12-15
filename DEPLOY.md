Deployment
----------

This repository includes a GitHub Actions workflow that deploys the static site to GitHub Pages.

- Workflow: `.github/workflows/deploy-pages.yml`
- Trigger: `push` to `main` or manual `workflow_dispatch`
- What it does: copies repository files (excluding `node_modules` and `.git`) into `public` and deploys them to the `gh-pages` branch using `JamesIves/github-pages-deploy-action`.

Notes:
- The workflow uses the built-in `GITHUB_TOKEN` so no additional secrets are required.
- After the first successful run, the Pages site should be available at `https://<your-username>.github.io/<repo>` (GitHub may take a minute to provision).

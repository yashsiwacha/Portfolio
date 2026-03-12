# Deployment Guide (GitHub Pages)

This portfolio is ready for automatic deployment using GitHub Actions.

## 1. Push to a GitHub repository

1. Create a repository (for example: `portfolio`).
2. Push the contents of this folder to the `main` branch.

## 2. Enable GitHub Pages

1. Open your repository on GitHub.
2. Go to **Settings -> Pages**.
3. Under **Build and deployment**, select **Source: GitHub Actions**.

The workflow file at `.github/workflows/deploy-pages.yml` will deploy on every push to `main`.

## 3. Custom domain (optional)

1. Create a file named `CNAME` in the repo root.
2. Put your domain in that file, for example:

```
portfolio.yourdomain.com
```

3. In your DNS provider, add a CNAME record pointing the subdomain to:

```
<your-github-username>.github.io
```

4. In **Settings -> Pages**, set the custom domain and enable HTTPS.

## Notes

- `.nojekyll` is included to ensure static assets are served without Jekyll processing.
- If your default branch is not `main`, update the branch in `.github/workflows/deploy-pages.yml`.

# umlauf.tech

Personal site of Mirek Umlauf. Static HTML, no build step.

## Structure

- `index.html` — homepage
- `essays/index.html` — essay index
- `essays/i-built-bi-for-two-ipos.html` — featured essay
- `CNAME` — custom domain for GitHub Pages

## Publish (first time)

1. Create repo `umlauf-tech` under github.com/mirekuml, push these files to `main`.
2. Repo → Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. DNS (at your registrar): remove the Google Sites mapping, then add
   - A records for `umlauf.tech` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - CNAME record `www` → `mirekuml.github.io`
4. Settings → Pages → Custom domain: `umlauf.tech` → wait for DNS check → tick **Enforce HTTPS** (cert can take up to an hour).
5. Unpublish the Google Sites custom-domain mapping.

## Analytics

Sign up for Cloudflare Web Analytics (free, no cookies, no consent banner), copy the token, then in `index.html` and `essays/*.html` replace `YOUR_TOKEN_HERE` and uncomment the `<script>` block at the bottom.

## Before launch

- Replace the portrait placeholder in `index.html` (hero, `.portrait` div) with a real monochrome photo.
- Fact-check flags: reconciliation outcome ("another close") and "healthcare-grade" vs. literal HIPAA.

## Adding an essay

Copy `essays/i-built-bi-for-two-ipos.html`, replace content, add a row in `essays/index.html`. Commit — Pages deploys automatically.

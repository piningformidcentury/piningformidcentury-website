# PiningForMidcentury — website starter

A responsive, no-checkout vintage furniture website built with your six supplied photos and retro logo.

## Preview locally

From this folder run `python3 -m http.server 8000`, then visit `http://localhost:8000`. Opening index.html directly as a file may prevent the gallery from loading due to browser security rules.

## Publish and enable the dashboard

1. Create a GitHub account and a repository for this site. Upload **all files**, including the hidden `.pages.yml` configuration file, preserving folders.
2. Publish the repository using a static host (for example, Cloudflare Pages or Netlify). Configure it as a static site with no build command and the root folder as the output directory. A public repository is simplest for the initial setup.
3. Sign in to https://pagescms.org with GitHub and authorize access to the repository. Open the repository in Pages CMS; the `Furniture collection` editor is configured by `.pages.yml`.
4. Add/edit furniture in the dashboard. Changes are committed to GitHub. The static host should automatically redeploy when changes are pushed to the connected repository.
5. Purchase your preferred domain and connect it in the hosting dashboard; update the host's DNS instructions at your domain registrar.

**Important:** Dashboard availability and editing permissions depend on the current Pages CMS service and GitHub authorization. The dashboard is an external service, not included as a locally hosted app. The current config uses one JSON list of furniture pieces.

## Before public launch

- Review `impressum.html` for any additional required German business disclosures; `privacy.html` is still a draft requiring adaptation to your hosting and services.
- The contact email has been configured. Add Instagram or WhatsApp links later if desired.
- Verify all furniture descriptions, availability, and any prices; example entries are not verified product attributions.
- Review third-party Google Fonts loading for your privacy requirements. For a privacy-minimal setup, remove the `@import` from `styles.css` and use the existing system font fallbacks, or self-host appropriately licensed fonts.
- Optimize photos if needed and verify on mobile.

## Update content manually (optional)

Edit `content/items.json` and upload photos into `assets/`. Image paths use `/assets/filename.jpg` in the JSON. Each item needs a unique `id`, `name`, `category`, `image`, and `status`. Optional `photos` is a list of additional image paths.

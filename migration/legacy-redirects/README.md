# Legacy domain redirects

This repository keeps the GitHub Pages custom domain `www.juleshaggard.com` and its HTTPS certificate. The current website lives at `https://darlingjules.com`.

The `site/` directory contains generated redirects for all 69 known HTML routes and a custom 404 fallback. `routes.json` records the old-to-new path mapping, including `/jules-haggard-creative-network` to `/jules-darling-creative-network`.

The Pages workflow copies retained `public/` files into `_site/`, overlays `site/`, then publishes `_site/`. This preserves existing media URLs while redirect HTML, the original custom-domain CNAME, and `.nojekyll` take precedence. Source code is retained for history and asset maintenance but is no longer built for this legacy domain.

JavaScript redirects preserve paths, query strings, and fragments. Each known route also has a new-domain canonical link, a visible continuation link, and a JavaScript-disabled meta-refresh fallback. These are client-side redirects, not HTTP 301/308 responses. Unknown paths retain an HTTP 404 status. The JavaScript-disabled fallback cannot preserve a runtime query string or fragment.

Keep this repository's Pages domain, DNS, and HTTPS enforcement intact. Changes to the actual website belong in `julesdarling/darlingjules-com`.

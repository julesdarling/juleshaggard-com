# Jules Darling: legacy domain redirects

The current website is [https://darlingjules.com](https://darlingjules.com). Edit and publish it from [julesdarling/darlingjules-com](https://github.com/julesdarling/darlingjules-com).

This repository keeps the `juleshaggard.com` / `www.juleshaggard.com` GitHub Pages domain binding and HTTPS certificate. It publishes the redirect pages in `site/`, preserving page paths, queries, and fragments.

The deployment workflow copies existing `public/` media first, then overlays `site/`. Retaining these files keeps old direct media links working. See [migration/legacy-redirects](migration/legacy-redirects/) for the route map and implementation.

The original Astro `src/`, rebuild scripts, and migration metadata are retained as a historical snapshot. They do not publish the current website. Do not replace the legacy CNAME or redirect bindings with the new domain.

Current personal portfolio: [Jules Darling](https://darlingjules.com/).

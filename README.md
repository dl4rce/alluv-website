# alluv-website

Static public website for **alluv — specialist LLM hosting**.
Served by GitHub Pages from `main` in this repository. Plain HTML and CSS; no
dependencies, no package manifest, no build step, no external fonts, no trackers,
no analytics. Do not run npm from this repository or its parent.

- Preview address: <https://dl4rce.github.io/alluv-website/>
- Product, platform and business case: private repository [`dl4rce/alluv`](https://github.com/dl4rce/alluv) (no access implied)
- Knowledge base: private Flaiwheel project `alluv`

## Repository boundary — read this before adding content

This repository is **public**. The private `dl4rce/alluv` repository holds the platform,
provisioning, serving configuration and the business case.

Never commit here:

- prices, plan names, token envelopes, discount structures or unit economics
- cost, power, lease or margin figures from the business case
- customer names, tenant identifiers, contract or SLA terms not yet publicly released
- hostnames, IP addresses, internal topology, GPUs-in-service counts or capacity data
- credentials, tokens, API keys or device identifiers (the Gitleaks workflow is a
  backstop, not a substitute for care)

Marketing copy only. Any published performance number must come from a finished,
reviewed measurement run on the exact offered configuration, and must keep its
labelling (measured vs. projected).

## Files

- `index.html` — single landing page: positioning, catalogue description, lane
  specification (descriptive, deliberately without numbers), status and contact.
- `site.css` — design system derived from the logo palette (pastel petals, graphite
  wordmark), responsive layout, visible focus states, reduced-motion support.
- `assets/alluv-logo.jpg` — 1024×1024 JPEG logo, currently used as a **placeholder** for
  the header mark, hero image and favicon. A proper sized and vector version is pending.
- `.nojekyll` — disables Jekyll processing on GitHub Pages.
- `robots.txt`, `sitemap.xml` — currently reference the preview address; update together
  with `CNAME` and the canonical link when the domain is chosen.
- `.gitleaks.toml`, `.github/workflows/gitleaks.yml` — secret scan on push and PR.

## Search visibility

Pages currently carry `<meta name="robots" content="noindex,nofollow">` because this is a
pre-launch preview without a legal notice. At launch, before announcing the domain:

1. set the robots meta in `index.html` to `index,follow`
2. replace the canonical and `og:url` / `og:image` values with the production domain
3. add the `CNAME` file and update `robots.txt` and `sitemap.xml`
4. publish the imprint and privacy statement, then link them from the footer

## Preview locally

Run from this repository:

```bash
python3 -m http.server 8765
```

Then open <http://localhost:8765/>. Files are served exactly as deployed. No npm needed.

## Deployment

GitHub Pages, legacy build type, source `main` branch, path `/` — the same setup as the
existing `dl4rce/stillpoint-website` repository. Pushing to `main` publishes the site.
Custom domain is not configured yet (no `CNAME`), by explicit decision.

## Open items

- **Domain** not chosen yet; site runs on the preview address in the meantime.
- **Imprint and privacy statement** required before launch (German legal requirements).
- **Pricing page** intentionally absent; publish only after an explicit release decision,
  and only with the numbers approved for public use.
- **Contact channel** (address, form or scheduling link) not defined.
- **Language** currently English; a German version may be required depending on audience.
- **Logo assets** — replace the placeholder JPEG with sized/vector variants and a proper
  favicon set.
- **`alluv` as a brand name** — `github.com/alluv` is an existing GitHub account and
  multiple unrelated `alluv*` projects exist publicly. Domain and trademark checks are
  still open and must be completed before promoting the name.

## Licence

Site content © alluv. No open-source licence is granted for the site content itself.
Entity details and the ownership line are pending decision — see Open items.

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
- `imprint.html` — imprint and legal disclosure plus a short privacy statement for this
  website. Cites § 5 DDG (in force since 14 May 2024), which replaced § 5 TMG.
- `site.css` — design system derived from the logo palette (pastel petals, graphite
  wordmark), responsive layout, visible focus states, reduced-motion support, legal page
  styles.
- `assets/alluv-logo.jpg` — 1024×1024 JPEG logo, currently used as a **placeholder** for
  the header mark, hero image and favicon. A proper sized and vector version is pending.
- `.nojekyll` — disables Jekyll processing on GitHub Pages.
- `robots.txt`, `sitemap.xml` — sitemap covers `index.html` and `imprint.html`; both
  reference the preview address and are updated together with `CNAME` at launch.
- `.gitleaks.toml`, `.github/workflows/gitleaks.yml` — secret scan on push and PR.

## Legal disclosure

`imprint.html` states the disclosure for **4rce.com Digital Technologies GmbH** and notes
that alluv is a project name of that company. Verified values:

- 4rce.com Digital Technologies GmbH, Grafentraubach 910, 84082 Laberweinting, Germany
- Managing Director: Volker Geith
- Amtsgericht Straubing, HRB 13771, VAT ID DE459375923
- Contact: info@4rce.com

The house number in the address is correct as stated. Two sibling sites —
`stillpoint-website` (`imprint.html`) and the Flaiwheel landing page — carry
`Grafentraubach 9`, which is **wrong** and should be corrected. The value here matches the
commercial register entry, the live 4rce.com legal notice, the aicollab.app data processing
agreement and the arcadeerrors.com imprint.

Two open items for the legal pages:

- `info@4rce.com` is the shared company address. A dedicated alluv address would be better
  once the domain exists.
- The imprint's privacy section covers **this static website** only. A full privacy
  statement for the hosting service itself is still required before launch.

## Search visibility

`index.html` carries `<meta name="robots" content="noindex,nofollow">` because this is a
pre-launch preview without a chosen domain. `imprint.html` uses `noindex,follow` so the
legal page stays reachable but out of the index. At launch, before announcing the domain:

1. set the robots meta in `index.html` to `index,follow`
2. replace the canonical and `og:url` / `og:image` values with the production domain
3. add the `CNAME` file and update `robots.txt` and `sitemap.xml`
4. link the imprint from the footer (already done) and publish the service privacy statement

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
- **Service privacy statement** still required: the imprint covers this static website
  only, not the hosting service or its data processing.
- **Dedicated contact address** for alluv — currently the shared `info@4rce.com`.
- **A full German-language version** of the imprint may be advisable; the page is English
  with the German heading retained.
- **Pricing page** intentionally absent; publish only after an explicit release decision,
  and only with the numbers approved for public use.
- **Language** currently English; a German version may be required depending on audience.
- **Logo assets** — replace the placeholder JPEG with sized/vector variants and a proper
  favicon set.
- **`alluv` as a brand name** — `github.com/alluv` is an existing GitHub account and
  multiple unrelated `alluv*` projects exist publicly. Domain and trademark checks are
  still open and must be completed before promoting the name.

## Licence

Site content © 4rce.com Digital Technologies GmbH. No open-source licence is granted for
the site content itself.

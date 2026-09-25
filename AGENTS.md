# Multicoaching Canada — Agent Governance

## Project identity

- Project: Multicoaching Canada
- Production domain: https://multicoaching.ca
- WWW domain: https://www.multicoaching.ca
- GitHub repository: `stivensp44-star/multicoaching-canada`
- Production branch: `main`
- Founder/operator: Aulida Valery
- Current hosting: Cloudflare Pages

## Mandatory future-agent preflight

Every future agent must:

1. Locate the repository root.
2. Read this repository-root `AGENTS.md` completely before inspection, editing, testing, validation, deployment, documentation changes, scene/asset work, or commits.
3. Read any additional governance or doctrine files referenced by this document.
4. Run `git status` and record the current branch and HEAD.
5. Preserve dirty-tree and user work.
6. Never overwrite unrelated work.

## Architecture

The site is static HTML, CSS, and vanilla JavaScript. Do not add an unnecessary framework.

Production files live under `outputs/`:

- French homepage: `outputs/index.html`
- English homepage: `outputs/en/index.html`
- French privacy page: `outputs/privacy.html`
- English privacy page: `outputs/en/privacy.html`
- CSS: `outputs/styles.css`
- JavaScript: `outputs/script.js`
- Assets: `outputs/assets/`

## Language doctrine

- French is the official and default website language.
- English is the backup language.
- `/` is French; `/en/` is English.
- Do not redirect visitors away from French based on browser language.
- Preserve canonical and hreflang metadata.
- New user-facing features must maintain French/English parity unless the owner explicitly approves otherwise.

## Brand assets

- Logo: `outputs/assets/MULTICOACHINGLOGO.jpeg`
- Founder image: `outputs/assets/koloplus.png`
- Do not replace real assets with stock images without owner approval.
- Preserve image proportions and responsive behavior.

## Business and contact information

- Founder: Aulida Valery
- Phone: `438-922-4181`
- Email: `multicoachingmtl@gmail.com`
- Facebook: `facebook.com/multicoachingmtl`
- Core services:
  - Coaching de vie
  - Coaching professionnel
  - Coaching en technologie de l’information
- Founded in 2006.

Never fabricate testimonials, client counts, awards, partnerships, certifications, statistics, pricing, addresses, or guaranteed results.

## Contact form doctrine

- The current contact form UI exists.
- V1 intentionally does not actually submit messages.
- JavaScript prevents submission until a real receiving service is configured.
- The site must never display a fake success message when no message was delivered.
- Phone and `mailto:` links must continue to work.
- Configure final contact infrastructure only after Multicoaching is moved to Aulida Valery’s own Cloudflare account.
- Intended receiving email: `multicoachingmtl@gmail.com`.
- Do not implement the contact backend unless explicitly requested.

## Cloudflare Pages

- Pages project: `multicoaching-canada`
- Production branch: `main`
- Framework preset: None
- Build command: `exit 0`
- Build output directory: `outputs`
- `multicoaching.ca` and `www.multicoaching.ca` are attached.
- SSL is enabled.
- HTTP/3/QUIC was disabled because it produced `ERR_QUIC_PROTOCOL_ERROR`.
- Do not re-enable HTTP/3 without production testing.
- Do not deploy or change Cloudflare configuration without explicit owner authorization.

## Ownership and future transfer

- Domain registration remains at GoDaddy for now.
- DNS currently uses Cloudflare.
- The website is temporarily hosted inside Stivo’s Cloudflare account.
- Long-term, Aulida Valery should create his own Cloudflare account.
- Recreate or transfer the Pages deployment there.
- Move Cloudflare DNS and zone management there.
- Configure his contact and email infrastructure there.
- Verify production completely before removing anything from Stivo’s account.
- Do not modify nameservers, DNS, registrar settings, or production infrastructure without explicit owner authorization.

## Git rules

- Production branch is `main`.
- Verify branch, HEAD, and status before writes.
- Never force-push.
- Never rewrite history.
- Never commit secrets, passwords, API keys, Cloudflare tokens, email credentials, or `.env` secrets.
- Use clear commit messages.

## SEO, accessibility, and mobile doctrine

Preserve:

- Canonical URLs.
- French/English hreflang and `x-default`.
- `sitemap.xml` and `robots.txt`.
- Semantic headings and descriptive alt text.
- Keyboard navigation and visible focus states.
- Readable contrast and typography.
- Accessible mobile navigation.
- Reduced-motion behavior where applicable.
- No horizontal overflow.
- Responsive layouts.

## Testing doctrine

Before reporting website changes complete, verify:

- French homepage.
- English homepage.
- Both privacy pages.
- Logo and founder image.
- Desktop and mobile layouts.
- Navigation, phone link, email link, and language switching.
- Browser console errors.
- Changed functionality.

For deployment work also verify the Cloudflare Pages deployment, `https://multicoaching.ca`, `https://www.multicoaching.ca`, and HTTPS/SSL.

## Change discipline

- Prefer the smallest safe change.
- Do not unnecessarily refactor working code.
- Do not rebuild the site from scratch unless explicitly requested.
- Preserve the brand, bilingual structure, production paths, and responsive behavior.

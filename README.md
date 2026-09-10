# Pizarro Studios

Pizarro Studios is an applied AI systems company focused on AI implementation, automation, web modernization, and practical business systems.

This repository contains the **public Pizarro Studios portfolio website** and the supporting cinematic brand-production assets used by the site.

> **Status:** public portfolio / proof-of-work site. Project descriptions should distinguish prototypes, MVPs, verified implementations, and real customer outcomes.

## Overview

The site is intentionally lightweight: it is a static website with no required application build step.

Primary goals:

- present Pizarro Studios clearly;
- show selected products and applied systems;
- publish proof of work without overstating results;
- provide a public URL suitable for outreach;
- support the Pizarro Studios cinematic brand system.

## Repository Structure

| Path | Purpose |
| --- | --- |
| `index.html` | Main public portfolio website |
| `cinematic/` | Brand-film system, production planning, prompts, references, and web-ready media |
| `cinematic/brand-system/` | Visual direction and brand rules |
| `cinematic/prompts/` | Generation prompts and structured shot data |
| `cinematic/shot-lists/` | Production tracking and shot planning |
| `cinematic/storyboards/` | Storyboards and narrative planning |
| `cinematic/audio/` | Audio direction |
| `cinematic/social-assets/` | Social cutdown planning |
| `cinematic/web-assets/` | Optimized media used by the website |
| `.gitignore` | Files intentionally excluded from version control |

Start with `cinematic/README.md` when working on the brand-film system.

## Local Preview

From the repository root, run:

```bash
python3 -m http.server 8080
```

Then open:

```text
http://localhost:8080
```

## Publishing Checklist

Before using the site in outreach:

1. Publish `index.html` and its referenced assets to a public host.
2. Open the live URL in a private/incognito browser window.
3. Confirm the page loads without authentication.
4. Test all navigation, email, phone, and external links.
5. Test desktop and mobile layouts.
6. Confirm video and image assets load correctly.
7. Use the public production URL in outreach rather than a local, private, or development preview.

## Content Standard

Every project shown publicly should use accurate status language.

Recommended labels:

- **Concept** — planned but not implemented.
- **Prototype** — working demonstration, not production-ready.
- **MVP** — core workflow implemented, still requiring broader testing or deployment work.
- **Verified implementation** — the stated behavior has been tested with inspectable evidence.
- **Customer outcome** — a real deployment produced a measured result for a real customer.

Do not turn a prototype into a customer-result claim simply because the interface looks complete.

## Cinematic Production System

The `cinematic/` directory contains the visual-production system for Pizarro Studios, including:

- visual rules;
- production status;
- shot prompts;
- structured shot data;
- storyboards;
- audio direction;
- social cutdowns;
- web integration guidance;
- optimized hero media.

See `cinematic/README.md` for the detailed workflow.

## Media and Repository Size

Keep source media separate from web-ready assets whenever possible. Large generated or approved production files should not be added to the repository unless they are required for the published website or intentionally preserved as versioned production assets.

For web delivery, prefer optimized files from `cinematic/web-assets/`.

## Security and Privacy

This is a public repository. Do not commit:

- API keys;
- passwords or tokens;
- `.env` files;
- private customer information;
- private proposals or internal business records;
- unpublished credentials or access links.

## Deployment

The repository does not require a specific hosting provider. A static host such as GitHub Pages, Netlify, or Vercel can serve the site.

Deployment should be considered verified only after the public URL has been opened and tested independently.

## Roadmap

Near-term repository priorities:

1. Keep the public portfolio aligned with current verified project status.
2. Finish and integrate the strongest cinematic assets without bloating the repository.
3. Publish a stable public deployment.
4. Add case-study evidence as real deployments produce measurable results.
5. Keep internal AI-BOS / Pizarro operating-system material out of this public website repository.

## Related Repositories

Pizarro Studios products and internal systems live in separate repositories. This repository should remain focused on the **public company website and brand presentation**.

## License

No open-source license is declared in this repository. Unless a license is added, do not assume permission to reuse or redistribute the site code or brand assets.

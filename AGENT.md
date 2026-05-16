# Project Handoff Notes

Last updated: 2026-05-16

## Project Status

This folder is a static personal website workspace intended for GitHub Pages.

The first implementation uses plain static HTML/CSS with no build step. This keeps the site compatible with GitHub Pages branch-based publishing from the repository root.

## User Goal

The user wants to create a personal website. The first discussion focused on buying a domain name before building the site.

Current direction: start with a free GitHub Pages personal webpage before buying a custom domain.

Likely website type is still flexible. The initial page is a personal homepage skeleton with sections for an introduction, work/projects, and current focus.

## Hosting Decision

Use GitHub Pages for the initial version.

Recommended path:

- The user changed the public GitHub username to `cosmoszzc`.
- The public GitHub profile is `https://github.com/cosmoszzc`.
- Do not publish or hard-code the previous username in public-facing site content.
- If the user wants the cleanest personal URL, create a GitHub repository named `cosmoszzc.github.io`.
- Push this folder's files to that repository.
- Enable GitHub Pages from the `main` branch and `/ (root)` if needed.
- The temporary site URL will be `https://cosmoszzc.github.io/`.
- A custom domain can be added later with a `CNAME` file and DNS changes.

Current static files:

- `index.html`: homepage content and structure.
- `styles.css`: responsive visual design.
- `404.html`: GitHub Pages fallback error page.
- `.nojekyll`: disables Jekyll processing.
- `README.md`: deployment and editing notes.

## Domain Discussion So Far

Key conclusion: domains are not truly permanent. They are registered and renewed by year. To approximate "permanent", buy multiple years up front, enable auto-renewal, and keep the payment method valid.

Current recommendation:

- Use `.com` if the user wants a general, long-term personal website domain.
- Use `.cn` only if the site is mainly for mainland China audiences and the user is comfortable with a more China-specific domain identity.
- Avoid very cheap first-year promotional suffixes such as `.xyz`, `.online`, `.site`, etc. because renewal prices may be much higher.

Discussed registrar options:

- Cloudflare Registrar: usually strong for long-term cost, but requires using Cloudflare DNS.
- Porkbun: usually cheap and straightforward for international domains.
- Namecheap: beginner-friendly, but long-term renewal may be higher.
- Alibaba Cloud or Tencent Cloud: better fit if hosting in mainland China and needing ICP filing workflow support.

Approximate China cloud registrar prices discussed on 2026-05-16, final checkout page should always be treated as authoritative:

| TLD | Alibaba Cloud | Tencent Cloud |
| --- | ---: | ---: |
| `.com` first-year registration | about CNY 85/year | about CNY 83/year |
| `.com` renewal | about CNY 95/year | about CNY 90/year |
| `.com` transfer-in | about CNY 85/year | about CNY 80/year |
| `.cn` first-year registration | about CNY 38/year | about CNY 33/year |
| `.cn` renewal | about CNY 42/year | about CNY 38/year |
| `.cn` transfer-in | about CNY 38/year | about CNY 33/year |

If hosting on a mainland China server, ICP filing is required before the website can be publicly served. If hosting outside mainland China, ICP filing is generally not needed, but mainland access speed may vary.

## Open Decisions

- GitHub username is set to `cosmoszzc`.
- Repository still needs to be created or connected: `cosmoszzc.github.io`.
- Final domain name text has not been chosen.
- Registrar has not been chosen because the project will start on GitHub Pages.
- Final site copy, name, projects, and contact details have not been provided.
- Whether the user wants a blog/CMS is unknown.
- Whether ICP filing is acceptable/desired is unknown.

## Working Instructions For Future AI Agents

- The workspace-level instruction references `C:\Users\79389\.codex\RTK.md`.
- That instruction says shell commands should be prefixed with `rtk`.
- The current folder is `D:\Claude\MyWeb`.
- There was no Git repository in this folder when this note was updated.
- Do not assume an existing project structure. Inspect files first before making implementation decisions.
- Keep the site simple and static unless the user asks for interactive features, a blog engine, or a CMS.
- Avoid adding a JavaScript framework until there is a concrete need.

## Suggested Next Steps

1. Create or connect the GitHub repository `cosmoszzc.github.io` if publishing setup is requested.
2. Replace placeholder content in `index.html` with the user's real display name, bio, projects, and contact details.
3. Create or connect a Git repository, then push to GitHub.
4. Enable GitHub Pages and verify the public URL.
5. Help choose and bind a custom domain later if the user wants a more formal address.
6. Record future technical decisions in this file as the project evolves.

## 2026-05-16 Session: Content direction & first real draft

### User profile confirmed
- Name: Zhang Zichao (张子超)
- GitHub: cosmoszzc
- PhD candidate, Electrical Engineering, Universiti Malaya
- Research: post-operative longitudinal glioma segmentation (deep learning)
- Supervisors: Dr. Anis, Dr. Liew

### Career direction (discussed, not final)
- Target: AI-related roles in Beijing (prefer East 2nd Ring to 4th Ring area — Haidian/Zhongguancun or Chaoyang/Wangjing)
- Interested sectors: AI + manufacturing / industrial vision, AI + medical, ML engineering, AI + education
- Work style: prefer engineering/product over pure lab research; wants hands-on, build-and-ship roles
- "钱多事少离家近" — half serious, half joke; priority is reasonable commute from East Second Ring

### Background highlights
- Mechanical engineering undergrad (BIPT), exchange at BUCT
- Co-founded two companies (Dream Maker Tech 2016, Yingsheng Education 2018)
- Non-standard industrial machinery, VR teaching aids, K12 STEM, 3D simulation
- Mechanical technician at NAURA subsidiary (Beijing 718, military semiconductor equipment)
- 1 invention patent, 3 utility model patents
- Multiple national/provincial competition awards (mechanical design, innovation, entrepreneurship)
- M.Eng. System Engineering, Universiti Malaya

### Website decisions
- Audience: future employers / collaborators
- Tone: professional but personal, highlight cross-disciplinary journey
- Narrative: "hands-on engineer who moved from mechanical design to AI — builds things that work"
- Keep existing design; update content only

### Files changed
- index.html: replaced all placeholder content with real bio, work history, education, awards, and contact
- styles.css: added .project-list, .award-list, .edu-list styles for new card content

### Still open
- Final domain name not chosen
- GitHub repo "cosmoszzc.github.io" not yet created/connected
- No custom domain yet (deploy to GitHub Pages first)
- PhD-era projects not yet listed (can add as they mature)
- No blog/CMS decision

## 2026-05-16 Design refresh: Framer-style

Switched from serif / hand-crafted aesthetic to Framer-inspired clean modern style:
- Sans-serif: Inter / SF Pro / PingFang stack
- Large negative space, strong typographic hierarchy
- Minimal colour: off-white bg, near-black ink, blue accent, subtle border lines
- Cards now white with soft hover shadow, rounded 14px
- Portrait panel simplified to flat circle mark (no decorative grid)
- Eyebrow labels in muted uppercase
- Full responsive breakpoint at 860px

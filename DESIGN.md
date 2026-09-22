# DESIGN.md — SBM Field Brand

## 1. Objective

Make every public surface (GitHub profile, portfolio, playground/lab) unmistakably one person: Shadrack Baraka Mwahanga, engineer and LLB student who ships for Kenyan field constraints. Job of the brand: a stranger trusts the work in thirty seconds and wants to stay.

## 2. Product context

Surfaces: `shadrackb1/shadrackb1` profile README · `shadrack-portfolio` (Vercel) · `playground` + `lab.html` (Pages). Audience: hiring managers, collaborators, campus and client leads in Kenya and remote. Physical analog: a legal field notebook and case file on warm paper, not a neon dashboard.

## 3. Visual foundations

| Token | Value | Use |
| --- | --- | --- |
| `--paper` | `#F3EDE2` | page ground |
| `--ink` | `#1C1917` | primary text, diagrams |
| `--pencil` | `#5C5346` | secondary notes |
| `--mute` | `#6B6358` | meta, mono labels |
| `--red` | `#C23B22` | margin rule, stamps, annotation |
| `--blue` | `#2F5D8C` | links, secondary ink |
| `--green` | `#3D6B4F` | checkmarks only |
| `--rule` | `#D9D0C0` | hairlines, ruled lines |
| `--tape` | `#C4B8A0` | tape strips |

Type scale: display Georgia 28–45 / 700; body system-ui 16–17 / 400; mono Menlo 10–13 / 400–600. No webfonts required.

Layout: single column max 920px; red margin rule at 3.25rem (1rem mobile); sections as docket rows with hairlines; 28px ruled-line rhythm on paper.

Signature: FIELD COPY rubber stamp (red, rotated −8°, presses and breathes). Living ink: pen-draw strokes, bleed dots, pulsing county ticks.

## 4. Accessibility

Body ≥ 4.5:1 on paper; large display ≥ 3:1. Focus-visible red ring. Tap targets ≥ 44px. `prefers-reduced-motion: reduce` freezes stamp/pen/pulse.

## 5. Voice & tone

Constraint-first. Concrete numbers and named constraints over adjectives. Contractions fine. Active voice. Max one em dash per 500 words. No hype words (see anti-ai-slop banned list). Tagline: **Constraint is the brief.**

## 6. Implementation practices

One HTML file for portfolio; forge script for profile SVGs (`scripts/forge_svg.py`, seeded RNG). Dual light/dark SVG pairs via `<picture>`. Lab is vanilla canvas, no CDN. Prefer CSS/SVG motion over JS animation for chrome.

## 7. Anti-patterns

No trophy widgets, typing SVG, skill-icon rows, gradient heroes, glassmorphism neon, attractor/Fourier “math flex” as brand, emoji headers, rounded shadow card grids, purple-cyan AI palette.

## 8. Decision-making

When a new surface appears: match this palette and voice first; invent only inside the notebook metaphor. Prefer imperfect ink over polished tech chrome.

## 9. Workflow

Generate SVG via forge (seed 1931). Review copy against banned words. Ship profile via short-lived branch → main (metrics bot races: rebase). Portfolio and playground push to main for auto-deploy.

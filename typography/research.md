# Typography Research — mrsandman.ai

## Brand Qualities
Smart, witty, quick, candid, good vibes, dreamy.
Dark theme (#0a0a0a), purple-to-blue gradient accent (#c9a0ff to #7eb8ff).

## Problem
All-monospace (SF Mono, Fira Code) is one-dimensional. Monospace should be an accent, not the whole system.

---

## Expert Principles

### Erik Spiekermann
Warmth comes from open letterforms and generous spacing, not decorative flourishes. For a personal tech brand, use a grotesque with enough quirk to avoid feeling corporate — "built by a person, not a committee."

### Tobias Frere-Jones
Use different optical approaches at different scales: more personality at large sizes, workhorse readability at small sizes. On dark backgrounds, letterforms need to be slightly heavier — light text on dark creates halation (letters appear thinner).

### Jessica Hische
Headlines should have a point of view. Don't choose something "safe" for display text — that's where personality lives.

### Dark Theme Rules
- Weight needs to increase. Regular on white = Light on black. Use Medium (500) as body default.
- Letter-spacing should open slightly for body text.
- Avoid pure white (#fff) — use off-white (#e0e0e0) for body to reduce eye strain.
- Gradient-colored type works best at large sizes. Use solid color from the gradient at small sizes.

---

## Font Candidates Evaluated

### Display / Headlines

| Font | Personality | Verdict |
|------|-------------|---------|
| **Bricolage Grotesque** | Quirky, human, warm. Subtle irregularities = "crafted not engineered." | **CHOSEN.** Best balance of personality + credibility. |
| Space Grotesk | Retro-futurist, techy. Evolved from Space Mono. | Strong runner-up. Safer choice. |
| Syne | Artistic, dramatic. French art-world origins. | Too artsy for tech. Hot sauce, not ketchup. |
| Cabinet Grotesk | Bold, editorial, impactful. | Great but display-only. Fontshare hosting. |
| Fraunces | Dreamy, wonky serif. WONK axis is unique. | Most "dreamy" but serif breaks tech convention. |

### Body Text

| Font | Personality | Verdict |
|------|-------------|---------|
| **Plus Jakarta Sans** | Clean, optimistic, warm. Generous x-height. | **CHOSEN.** Warmth aligns with "good vibes." |
| General Sans | Confident, warm, versatile. | Excellent but Fontshare (not Google Fonts). |
| DM Sans | Geometric, neutral. Optical sizing. | Good but becoming ubiquitous. Less warmth. |
| Inter | The Helvetica of screens. | Too anonymous. "Zero personality." |
| Outfit | Friendly, soft, rounded. | Leans consumer/lifestyle over tech. |
| Geist Sans | Sharp, developer-native. | Too associated with Vercel. Not warm enough. |

### Monospace Accent

| Font | Personality | Verdict |
|------|-------------|---------|
| **JetBrains Mono** | Precise, functional, slightly rounded. | **CHOSEN.** Best readability at small sizes. |
| Space Mono | Retro-futurist, characterful. | More personality but less readable at 12-14px. |
| Geist Mono | Clean, modern. | Self-host only. Vercel association. |

---

## Pairing Strategies Considered

### A: "Dreamy Tech" — Fraunces + General Sans + JetBrains Mono
Boldest. Serif display is unusual for tech. Memorable but risky.

### B: "Refined Builder" — Space Grotesk + Plus Jakarta Sans + JetBrains Mono
Balanced. Safe lane. Space Grotesk increasingly popular.

### C: "Warm Machine" — Bricolage Grotesque (all sizes) + Space Mono
Simple two-font system. Less hierarchy contrast.

### D: "Night Mode Native" — Syne + Geist Sans + Geist Mono
Maximum drama. Syne-to-Geist jump is jarring.

### E: "Smart Play" — Bricolage Grotesque + Plus Jakarta Sans + JetBrains Mono **SELECTED**
Best balance for brand. Three fonts = three personality zones (quirky, warm, precise).

---

## Type Scale (Perfect Fourth — 1.333)

| Role | Size | Weight | Font |
|------|------|--------|------|
| Hero / Brand | clamp(2.5rem, 2rem + 2.5vw, 4rem) | 700-800 | Bricolage Grotesque |
| Subheading | clamp(1.1rem, 1rem + 0.25vw, 1.25rem) | 400 | Plus Jakarta Sans |
| Body | clamp(0.95rem, 0.9rem + 0.2vw, 1.05rem) | 500 | Plus Jakarta Sans |
| Small / Meta | clamp(0.75rem, 0.7rem + 0.15vw, 0.85rem) | 400 | JetBrains Mono |
| Button | 0.85rem | 600 | Plus Jakarta Sans |

---

## Implementation Notes
- All three fonts on Google Fonts — single `<link>` tag, no self-hosting
- Load only needed weights: Bricolage 700/800, Plus Jakarta 400/500/600, JetBrains Mono 400
- Use `font-display: swap` (Google Fonts default)
- Body weight 500 (Medium) on dark backgrounds — 400 looks anemic
- Preload body font for fastest render

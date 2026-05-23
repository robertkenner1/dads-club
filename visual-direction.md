# Dad's Club — Visual Direction

Direction: **Quiet Confidence** (editorial · restrained · photo-led), with color held back. The warmth comes from photography, type, and space — not from saturated fills.

Pairs with `content.md`, `ia.md`, and `/images/`.

---

## North-star feel

A thoughtful, slow-magazine sensibility. Calm pages, strong photography, careful type. The site looks like it was built by someone who cares, not by someone selling something. Color is used like punctuation — present, but rarely.

Tone-check sentence: *"Come as you are. Leave with connection."* — the design has to feel as unhurried as that line reads.

## Color system

Restrained. One ink, one paper, one warm accent — used sparingly. No color blocks behind content, no full-bleed color sections.

| Role | Value | Notes |
|---|---|---|
| Paper | `#F6F2EA` | Warm off-white. The site's default background. |
| Ink | `#1B1714` | Warm near-black for text. Never pure `#000`. |
| Accent (warm) | `#A24E2B` | Terracotta / warm rust. The *only* saturated color on the page. Used for: link underlines on hover, the primary CTA word ("Join Dad's Club" in nav), tiny mark accents, mascot-mark eye/highlight if reused. |
| Rule line | `#D9CFBE` | Hairline dividers, form borders, image borders. |
| Muted ink | `#6B6258` | Captions, metadata, dates. |

Usage rules:
- Body and headlines are always Ink on Paper.
- Accent never exceeds ~3% of the surface area of any view.
- No accent button fills. CTAs are typographic with a thin rule underline or a small caret.
- No gradients, no shadows beyond the lightest image cards.

## Typography

Two faces. The serif does the work; the sans does the labels.

**Display + body serif:** Tiempos Text (or GT Sectra / Source Serif as substitutes).
- Used for: H1–H4, body copy, blockquotes, the wordmark itself.
- Oldstyle figures (`tnum off`) for inline numbers; tabular only in event lists.

**Utility sans:** Inter (or Söhne if available).
- Used for: nav, captions, form labels, metadata (date/time/location chips), small caps eyebrows.

**Type scale (desktop):**

| Token | Size / line | Use |
|---|---|---|
| Display | 64 / 1.05 | Hero headline only |
| H1 | 44 / 1.15 | Page titles |
| H2 | 32 / 1.2 | Section headings |
| H3 | 22 / 1.3 | Sub-sections |
| Body L | 20 / 1.55 | Long-form (About, event description) |
| Body | 17 / 1.55 | Default |
| Caption | 13 / 1.4 | Small caps, captions, eyebrows |

**Rules:**
- Measure (line length) caps at ~62ch for body L, ~70ch for body.
- Eyebrows above section headings are sans, small caps, letter-spaced (`+8%`), muted ink.
- Italics OK for emphasis and pull quotes. No bold inside body — use the serif's natural weight contrast.

## Wordmark + mascot

No real wordmark exists yet. Build one in this direction:

- **Wordmark:** "Dad's Club" set in the display serif, optical-sized, slight letter-spacing tightening. Optional small-caps "EST. 2025" sits beneath, separated by a hairline rule. Avoid script, avoid sign-painter — that's a different direction.
- **Mascot demotion:** the beaver doesn't headline. It appears as:
  - a small mark (≤24px equivalent) in the footer, or
  - a single decorative spot inside the About page, in line with body copy.
  - Never in the hero. Never larger than the wordmark.
- The cartoon-animals-feast illustration is too thematically loud for this direction — retire it, or use only as a small section ornament in a holiday post.

## Photography

This direction lives or dies on the photos.

**Selection bias:**
- Faces, candid, mid-conversation. Not posed group shots in front of a logo.
- Show *attention* between people, not the camera.
- Wide air around subjects — don't tightly crop.

**Treatment:**
- Natural color. No warm filter, no orange-and-teal grade.
- Slight desaturation (~−8%) so skin tones read first.
- Subtle grain only on hero images (keeps detail in grid photos).
- B&W treatment allowed for one image per page as an editorial accent — sparingly.

**Hero strategy:**
- Hero photo is single, large, generous margin. Headline sits *beside* or *below* the image, not on top of it.
- The `sunset-dock-gathering.jpeg` is the strongest hero candidate by composition. `pickleball-team-group.jpeg` works for `/about` or `/events` index.
- `dad-fuel-beer-can.jpeg` is product-y — fine for a single editorial spot, don't hero it.

**Captions:**
- Every editorial photo gets a caption in muted-ink sans, ≤80 chars. Cite location/event if known. Captions are a feature, not an afterthought.

## Responsive behavior

Mobile-first. Designed at three breakpoints; everything between flexes fluidly.

**Breakpoints:**
- `S` ≤ 640px (phones)
- `M` 641–1024px (tablets, small laptops)
- `L` ≥ 1025px (desktop)

**Type scale on mobile (S):**

| Token | Desktop | Mobile |
|---|---|---|
| Display | 64 / 1.05 | 40 / 1.1 |
| H1 | 44 / 1.15 | 30 / 1.2 |
| H2 | 32 / 1.2 | 24 / 1.25 |
| H3 | 22 / 1.3 | 19 / 1.35 |
| Body L | 20 / 1.55 | 18 / 1.55 |
| Body | 17 / 1.55 | 16 / 1.55 |
| Caption | 13 / 1.4 | 12 / 1.4 |

**Layout adaptations:**
- Asymmetric grid collapses to single-column under M. No squeezed two-column blocks on mobile.
- Hero photo stacks above headline on mobile, with same generous margins (≥24px sides).
- Nav collapses to wordmark + hamburger at S. The "Join Dad's Club" CTA stays visible *outside* the hamburger (top-right) — it's the primary conversion and shouldn't be hidden.
- Event cards stack with full-width hairlines between, instead of side-by-side.
- Footer columns stack vertically at S, kept at 2-up at M, 3-up at L.
- Newsletter block: input + button stack vertically at S; inline at M/L.

**Touch targets:** all interactive elements ≥44×44px hit area, even when the visible mark is smaller (e.g., the IG footer icon).

**Images:** serve responsive `srcset` — 2-3 sizes per image, Wix already does this for the source URLs we extracted.

## Layout principles

- **Generous white space, asymmetric grids.** 12-column underlying grid; most content sits in 7 or 8 columns offset, not centered.
- **One idea per section.** Don't stack a headline + body + photo grid + CTA in the same band — let things breathe across the scroll.
- **Hairline dividers** in Rule color separate sections rather than background changes.
- **No card shadows.** If a card needs separation, use a 1px Rule border or just spacing.
- **Edge-to-edge images** allowed but rare — reserve for the hero and one mid-page break.

## Components

- **Nav:** Wordmark left, three text links + "Join Dad's Club" CTA right. CTA is a text link with a small caret `→` and accent underline on hover. No pill button.
- **CTAs (body):** typographic with thin underline, accent color on hover only. Caret optional.
- **Forms:** input borders in Rule color, no fills, label sits above field in caption sans. Submit button matches CTA treatment.
- **Event card:** date (oldstyle figures) + event name (serif H3) + location (caption sans), separated by hairlines. No image inside the card by default; the index page leads with one editorial photo at top instead.
- **Newsletter block:** single line — eyebrow ("Join our Movement") + serif statement + email field + Sign Up text-link. No colored container.
- **Footer:** small wordmark, three columns of utility links, IG icon as a small accent mark.

## Motion

Calm and short.

- Fades: 200ms ease-out.
- Subtle text reveals on first paint only (≤16px translate). No scroll-jacking, no parallax.
- Hover states: underline-in (left→right) on links, accent color appears, ink stays the same.
- No autoplay video. If video is added later, muted, looped, and stop-on-scroll-out.

## What this direction is NOT

To keep us honest:
- Not warm-and-fuzzy storybook (that was Heritage Community — different direction).
- Not athletic/varsity (that was Varsity Brotherhood — different direction).
- Not a startup landing page. No big colored hero, no oversized CTA pill, no "social proof" logo bar.
- Not minimal-because-empty — there should be a *lot* of content and photography, just calmly arranged.

## Risks (and mitigations)

| Risk | Mitigation |
|---|---|
| Reads cold / aloof for a "all dads welcome" community | Lean hard on warm photography and warm-toned ink/paper; never use pure black or gray. Copy stays plainspoken. |
| Mascot fans miss the beaver | Keep one charming mascot moment per primary page (footer + one editorial spot on /about). Don't kill it. |
| Designers/devs default to colored buttons | Spec the typographic CTA treatment with examples in the build doc; don't leave it to interpretation. |
| Photography quality becomes the bottleneck | Curate aggressively — better to repeat 6 great images than dilute with 20 okay ones. |

## Open questions for next pass

- Final type license: Tiempos Text + Inter, or a free pairing (Source Serif 4 + Inter)?
- Do we name a specific terracotta brand color and lock the hex, or commission a custom one?
- Mascot redraw: keep the existing illustration scaled down, or commission a minimal one-color version that fits this direction?
- Wordmark: in-house using the display serif, or briefed out as a custom letterform?

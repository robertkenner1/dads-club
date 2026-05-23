# Dad's Club — /about Wireframe

Long-form story page. Follows `ia.md` (section order, content sources) and `visual-direction.md` (restrained palette, asymmetric editorial grid, mascot lives here in one small spot).

Nav and footer are identical to Home — see `home-wireframe.md`. This doc shows only the page body.

---

## Desktop (L ≥ 1025px)

```
─────────────────────────────────────────────────────────────────────────────
[ nav — same as home ]
─────────────────────────────────────────────────────────────────────────────

   THE STORY

        Dad's Club exists to build
        belonging, community, and
        brotherhood among Dads.

─────────────────────────────────────────────────────────────────────────────

   FOUNDING

        Dad's Club was founded by a husband and wife duo
        who saw a gap—and decided to do something about it.
        They believed that Dads deserved a place where they
        could gather, connect, and belong.

        We realized that many dads are carrying a lot,
        often quietly, and not always with the community
        they deserve. We wanted to change that.

        Whether you're a new dad or have been doing this
        for years, there's a seat at the table for you.

        Come as you are.
        Leave with connection.
        All Dads are welcome.

                                                       🦫
                                  (small mascot spot, in-line with the copy)

─────────────────────────────────────────────────────────────────────────────

   THE FOUNDERS

   ┌──────────────────────────────┐    ┌──────────────────────────────┐
   │                              │    │                              │
   │  [founder portrait 1]        │    │  [founder portrait 2]        │
   │  (or 'photo forthcoming'     │    │                              │
   │   placeholder — see gaps)    │    │                              │
   │                              │    │                              │
   └──────────────────────────────┘    └──────────────────────────────┘
   Name · role · one-line bio          Name · role · one-line bio

─────────────────────────────────────────────────────────────────────────────

   IN PRACTICE

        A Dads Club event is a relaxed, welcoming gathering
        where fathers connect, share experiences, and build
        community. It's a mix of conversation, support, and
        fun—whether through group discussions, activities with
        kids, or just unwinding with other dads who get it.

   ┌──────────────────────────────┐  ┌────────────────────┐
   │                              │  │  [photo]           │
   │  [editorial hero photo]      │  │                    │
   │                              │  └────────────────────┘
   │                              │  ┌────────────────────┐
   │                              │  │  [photo]           │
   │                              │  └────────────────────┘
   │                              │  ┌────────────────────┐
   │                              │  │  [photo]           │
   └──────────────────────────────┘  └────────────────────┘
   caption                            captions

─────────────────────────────────────────────────────────────────────────────

        Take a seat at the table.

        Join Dad's Club  →

─────────────────────────────────────────────────────────────────────────────
[ footer — same as home ]
```

## Mobile notes

- Everything stacks single-column.
- Founder portraits stack vertically, full-width with captions below each.
- Photo grid in "In Practice" collapses to one column, full-width.
- Mascot spot stays inline with the body copy (same position in the reading order).
- Closing CTA gets the same generous vertical breathing room as on desktop.

---

## Section-by-section notes

### The Story
- Typographic hero. **No photo here.** The mission line *is* the page-opener.
- Eyebrow "THE STORY" small-caps sans.
- Mission line in display serif, set tight, ranged left, narrow measure.
- Don't repeat the line later — once this hits, it's done.

### Founding (long-form)
- Body L copy, indented to roughly cols 2–8. Right side breathes.
- Eyebrow "FOUNDING" left-aligned.
- The final stanza ("Come as you are. / Leave with connection. / All Dads are welcome.") sets on three lines as a closing beat — slightly larger than body, italic optional.
- **This is the one editorial spot for the mascot.** Small (≤72px wide), in-line with the right margin of the closing stanza. Not centered, not heroic — a moment, not a graphic.

### The Founders
- Two portraits side-by-side at L, stacked at S.
- Caption beneath each: name · role · one-line bio.
- **Gap to fill:** site doesn't currently publish founder names or photos. If launch is before content is ready, replace with a single "Founder bios forthcoming" line in muted ink + hairline divider — don't show empty placeholders.

### In Practice (event description + photo grid)
- Reuses the same canonical paragraph from Home (`content.md` §4). Intentional repetition — Home introduces it, About goes deeper.
- Asymmetric photo grid: one large + three smaller. Different photo selection from Home so a visitor who's seen both gets variety.
- Recommended photos for About (different from Home): `sunset-dock-gathering.jpeg` (large) + `two-dads-park-bench.jpg`, `indoor-gathering-blue-cap.jpg`, `dads-club-meeting-banner.jpg`. (The two low-res files are OK here at the smaller sizes.)

### Closing CTA
- One sentence + the primary CTA. No section divider above — it sits as a quiet outro.
- Indented to match the body copy above (cols 2–8).
- The CTA is the same Join Dad's Club text-link with caret used everywhere else.

## States / edge cases

- **No founder content yet:** show a single muted-ink line "Founder bios forthcoming" and skip the portraits row entirely. Don't ship empty image frames.
- **One founder vs two:** layout adapts; a single portrait sits in col 2–6, right side breathes.

## Open questions

- Founder names + bios + portraits — needed before final layout.
- Do we add a "Where we gather" line naming a home region (Verplanck/Hudson Valley)? Currently the site is silent on this. Recommend yes, one line under the closing stanza.
- The mascot spot: keep the existing illustration scaled down, or commission a quieter single-color version? Per `visual-direction.md`, probably the latter.

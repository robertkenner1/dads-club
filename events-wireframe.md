# Dad's Club — /events Wireframe

Events index page. Follows `ia.md` (events lead with the canonical event description, then list upcoming, optionally past gatherings) and `visual-direction.md` (restrained palette, hairline-divided list rows over cards).

Nav and footer match Home — see `home-wireframe.md`.

---

## Desktop (L ≥ 1025px)

```
─────────────────────────────────────────────────────────────────────────────
[ nav — same as home ]
─────────────────────────────────────────────────────────────────────────────

   UPCOMING EVENTS

   ┌──────────────────────────────────────────────────────────────────────┐
   │                                                                      │
   │                                                                      │
   │   [editorial photo — pickleball-team-group or sunset-dock]           │
   │                                                                      │
   │                                                                      │
   └──────────────────────────────────────────────────────────────────────┘
   caption · gathering, season year

        A Dads Club event is a relaxed, welcoming gathering
        where fathers connect, share experiences, and build
        community. It's a mix of conversation, support, and
        fun—whether through group discussions, activities with
        kids, or just unwinding with other dads who get it.

─────────────────────────────────────────────────────────────────────────────

   Thu, May 14, 2026 · 7:30 PM
   Dad's Club Gathering
   Location TBD
                                                                  RSVP →

─────────────────────────────────────────────────────────────────────────────

   Thu, May 28, 2026 · 7:30 PM
   Dad's Club Gathering
   Location TBD
                                                                  RSVP →

─────────────────────────────────────────────────────────────────────────────

   Thu, Jun 11, 2026 · 7:30 PM
   Dad's Club Gathering
   Location TBD
                                                                  RSVP →

─────────────────────────────────────────────────────────────────────────────

   (... rest of the list ...)

─────────────────────────────────────────────────────────────────────────────

   PAST GATHERINGS

   ┌──────────────────┐  ┌──────────────────┐  ┌──────────────────┐
   │                  │  │                  │  │                  │
   │  [photo]         │  │  [photo]         │  │  [photo]         │
   │                  │  │                  │  │                  │
   └──────────────────┘  └──────────────────┘  └──────────────────┘
   Halloween Pop Up      Pickleball Night      Summer at the Dock
   Oct 30, 2025          Spring 2026           Aug 2025

   ┌──────────────────┐  ┌──────────────────┐  ┌──────────────────┐
   │  [photo]         │  │  [photo]         │  │  [photo]         │
   └──────────────────┘  └──────────────────┘  └──────────────────┘
   Caption · Date         Caption · Date         Caption · Date

─────────────────────────────────────────────────────────────────────────────
[ footer — same as home ]
```

## Mobile notes

- Hero photo stays full-width with caption below.
- Event list rows stack identically; the `RSVP →` link drops to a new line below the location at S, ranged left.
- Past gatherings collapses to 2-up at M, 1-up at S.
- Date/time/location chips on a single line at L become a wrapping line at S — don't truncate.

---

## Section-by-section notes

### Page heading
- Eyebrow + display serif: **UPCOMING EVENTS** in small-caps sans above; not strictly necessary to have a separate H1 — the eyebrow does the page-titling work in this layout. Keep it semantic with an `<h1>` on the eyebrow for accessibility.

### Intro photo + canonical paragraph
- Single full-bleed-within-column editorial photo at the top — sets tone before any event details.
- Caption underneath in muted sans.
- Below the photo: the canonical "A Dads Club event is…" paragraph, indented to cols 2–8.
- Hairline divider separates intro from the list.

### Event list (list rows, not cards)
- Each upcoming event is a single row, not a card. Hairline rules between rows.
- Row structure: date · time (small caps eyebrow line) → event name (serif H3) → location (muted sans) → RSVP link on the far right (or below at S).
- Series events (the recurring Dad's Club Gathering) **expand into individual rows** — one per scheduled date through June 19, 2026. Don't collapse "Multiple Dates" into one row; people need to RSVP per instance.
- RSVP link goes to the Wix Events URL for that specific instance.
- Hover state on a row: subtle accent underline on the event name; whole row is clickable (clicks anywhere take you to the event detail page, not directly to RSVP — preserve information scent).

### Past gatherings
- Photo grid, 3-up at L, captions beneath each in muted sans.
- Recommended photos: `pickleball-team-group.jpeg`, `dad-daughter-pumpkin-festival.jpeg`, `sunset-dock-gathering.jpeg`, `guy-laughing-string-lights.jpeg`, `two-dads-park-bench.jpg`, `indoor-gathering-blue-cap.jpg`.
- Each tile links to the event detail page if one exists, or a lightbox if it's just photo evidence.
- **Optional section.** If there's no clear connection between photos and named past events, drop the section entirely rather than ship orphaned photos.

## States / edge cases

- **No upcoming events (off-season):**
  - Hide the event list entirely.
  - Show a single line under the intro paragraph: *"No gatherings scheduled right now. **Join the list →** to hear when the next one drops."* → links to the Google Form.
  - Keep "Past gatherings" visible to provide social proof.
- **One upcoming event only:** layout still works — just one row, no awkwardness.
- **Recurring series spans far into the future:** show the next 6 instances by default; "Show all" text link below the list reveals the rest.

## CTA hierarchy on this page

| Tier | CTA | Where |
|---|---|---|
| Primary (page-level) | RSVP → (per row) | Each event row |
| Secondary | Join Dad's Club | Nav only — no extra Join CTA on this page |
| Tertiary | (past gathering tile) | Past gatherings grid |

Deliberate: this page is about *attending*, not *joining*. Resist adding a "Join" section mid-page.

## Open questions

- Wix Events RSVP URLs — do we have one per series instance, or one for the whole series? If the latter, the row's RSVP link goes there and the detail page handles instance selection.
- Past gatherings: do you have date-tagged photos for past events, or is this section more aspirational right now?
- Filtering by event type (Gathering / Pop Up / Pickleball / etc.) — not in v1, but worth a placeholder slot if more event types appear.

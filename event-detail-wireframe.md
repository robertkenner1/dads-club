# Dad's Club — /events/[slug] Wireframe

Per-event detail page. Each event in the events list links here; this page hands off to Wix Events for actual RSVP.

Nav and footer match Home — see `home-wireframe.md`.

---

## Desktop (L ≥ 1025px)

```
─────────────────────────────────────────────────────────────────────────────
[ nav — same as home ]
─────────────────────────────────────────────────────────────────────────────

   ←  All events

   GATHERING

   Dad's Club Gathering

   ┌──────────────────────────────────────────────────────────────────────┐
   │                                                                      │
   │                                                                      │
   │   [event hero photo — series photo if no instance-specific image]    │
   │                                                                      │
   │                                                                      │
   └──────────────────────────────────────────────────────────────────────┘
   caption (optional)

   Date              Time             Location
   May 14, 2026      7:30 PM          TBD

   ──────────────

        A Dads Club event is a relaxed, welcoming gathering
        where fathers connect, share experiences, and build
        community. It's a mix of conversation, support, and
        fun—whether through group discussions, activities with
        kids, or just unwinding with other dads who get it.

        RSVP  →

─────────────────────────────────────────────────────────────────────────────

   NEXT UP

   Thu, May 28, 2026 · 7:30 PM
   Dad's Club Gathering · Location TBD                            See →

   Thu, Jun 11, 2026 · 7:30 PM
   Dad's Club Gathering · Location TBD                            See →

─────────────────────────────────────────────────────────────────────────────
[ footer — same as home ]
```

## Mobile (S ≤ 640px)

Mobile adds a **sticky bottom-of-viewport RSVP bar**. This is the one place the page breaks the "no fills, no chrome" rule — RSVP is the page's whole purpose, and on mobile it should always be one tap away.

```
┌──────────────────────────────┐
│  Dad's Club    ☰    Join →   │
├──────────────────────────────┤
│                              │
│  ← All events                │
│                              │
│  GATHERING                   │
│                              │
│  Dad's Club Gathering        │
│                              │
│  ┌────────────────────────┐  │
│  │   [hero photo]         │  │
│  └────────────────────────┘  │
│  caption                     │
│                              │
│  Date                        │
│  May 14, 2026                │
│                              │
│  Time                        │
│  7:30 PM                     │
│                              │
│  Location                    │
│  TBD                         │
│                              │
│  ──────────                  │
│                              │
│  A Dads Club event is a      │
│  relaxed, welcoming          │
│  gathering where fathers     │
│  connect, share experiences, │
│  and build community.        │
│                              │
│  ...                         │
│                              │
│  RSVP →                      │
│                              │
├──────────────────────────────┤
│  NEXT UP                     │
│                              │
│  Thu, May 28, 2026 · 7:30 PM │
│  Dad's Club Gathering        │
│  See →                       │
│                              │
│  ...                         │
│                              │
├──────────────────────────────┤
│  [ footer ]                  │
└──────────────────────────────┘

═══ sticky bar ═══════════════
  Thu, May 14    RSVP →
══════════════════════════════
```

The sticky bar appears once the user scrolls past the in-flow RSVP link. It's a single thin row, Ink on Paper with a hairline top border. Dismissible? **No** — RSVP is the page's purpose.

---

## Section-by-section notes

### Back link
- `← All events` text link at the top of the content area, muted ink, small.
- Returns to `/events`. Not a browser-history `back` — always go to the events index.

### Event header
- Eyebrow: event series category (`GATHERING`, `POP UP`, `PICKLEBALL`, etc.) in small-caps sans.
- Event name in display serif, narrow measure, ranged left.

### Hero photo
- One image, full-width within content column.
- Falls back to a generic series photo if the specific instance doesn't have one — never show a broken or missing image frame.
- Caption optional — only include if it adds context.

### Meta row (Date / Time / Location)
- Three columns at L, each with a small-caps sans label above the value.
- Values in body L serif.
- At S, stacks to single column with the same label-above-value structure.
- TBD locations: show "TBD" plainly. Don't dress it up. (Optionally add a one-liner: "Location announced 48 hours before.")

### Description + RSVP
- Indented body L copy. Uses the canonical paragraph if instance-specific copy isn't provided.
- RSVP text-link with caret follows the paragraph — not a button.
- Link target: Wix Events URL for *this specific instance*.

### Next up
- Up to 3 upcoming events from the same series, sorted by date.
- Single-line rows with `See →` link to that event's detail page.
- If this is the last event in a series, hide the section entirely.

## States / edge cases

- **Past event:** show a "PAST EVENT" eyebrow chip in muted ink under the date row. Replace RSVP link with photo grid of the actual gathering (if photos exist) + "See upcoming events →" text link. Hide the sticky bar on mobile.
- **No hero image available:** show a typographic header block instead — large date in display serif against Paper, no image frame.
- **Cancelled or postponed:** banner at the top of the content area in Ink-on-Paper with a hairline border, no accent color. Plain language: "This gathering has been postponed. **Find the next one →**"
- **Same-day event (today):** the meta row's date adds "Today" in italic muted sans. No countdown timer — that's anxious energy, wrong tone.

## Open questions

- Series category taxonomy — what eyebrows are valid? (`GATHERING`, `POP UP`, etc.) Need a small fixed list so styling stays consistent.
- Whether to embed a map for non-TBD locations or just text the address. Recommend text-only at v1; calm tone, less third-party loading.
- Whether the sticky mobile RSVP bar should also appear on desktop. Recommend no — desktop has the visible CTA in the flow and a viewport-height window large enough not to need it.

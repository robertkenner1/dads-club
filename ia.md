# Dad's Club — Information Architecture (Redesign)

Source: synthesis of current officialdadsclub.com site map + decisions made 2026-05-23. Pair with `content.md` (copy inventory) and `/images/` (asset inventory).

---

## Site map

```
Dad's Club
├── /              Home          (narrative landing — hero, mission, next event, IG proof, join CTA)
├── /about         The Why       (founders, mission long-form, "what a gathering is")
├── /events        Upcoming      (canonical event description as intro + list)
│   └── /events/[slug]           Per-event detail + RSVP (Wix Events)
├── /contact       Contact       (form + direct email)
└── footer-only links:
    ├── Instagram (external)
    ├── Email (mailto:)
    └── Privacy / Terms (future)
```

## On-domain vs. external

| Function | Lives where | Notes |
|---|---|---|
| Identity, story, photos | **On domain** | Owned narrative across `/`, `/about` |
| Events index + detail | **On domain** | SEO + shareable URLs per event |
| Event RSVP / ticketing | **External** — Wix Events | Already works; don't rebuild |
| Join / membership signup | **External** — Google Forms | Decision locked: keep current form; `/join` button opens it in new tab |
| Social proof feed | **External** — Instagram embed | Don't host; mirror the live feed |
| Newsletter capture | **On domain** — Wix native | Owned email list, separate from join form |
| Search | Drop | Wix default; not useful at this size |

## Routes the current site has that are NOT in the redesign

- `/blog-feed` — **dropped**. Currently 404s. Not coming back in this redesign.
- `/search` — drop from public nav.
- `/shop` or `/merch` — **not added**. The DAD FUEL beer can is one-off lifestyle imagery, not a product line.

## Primary nav (top of every page)

1. About
2. Events
3. Contact
4. **Join Dad's Club** ← visually distinct CTA button, opens Google Form in new tab

Home is reached via the wordmark/logo, not a "Home" link.

## Home page section order (recommended)

1. **Hero** — mascot or hero photo (`sunset-dock-gathering.jpeg` is the strongest candidate) + tagline *"Dad's Club exists to build belonging, community, and brotherhood among Dads."* + primary CTA: *Join Dad's Club*
2. **What we are** — short version of the mission, link to `/about` for the long story
3. **Next gathering** — pulled from `/events`, single card with date/location + *See all events* link
4. **What a gathering feels like** — photo grid (community event photos) + the canonical "A Dads Club event is…" paragraph
5. **Instagram feed** — live embed of `@officialdadsclub`
6. **Newsletter signup** — "Join our Movement" / email field / Sign Up
7. **Footer** — email, IG, future legal links

## /about page

- Founding story (husband-and-wife duo gap-spotting → "seat at the table" closer)
- Long-form mission
- Founder photo(s) — *not currently on site, gap to fill*
- Photo grid of past gatherings (re-use community photos from `/images/`)
- Secondary CTA: *Join Dad's Club*

## /events page

- Heading: **Upcoming Events**
- Intro: canonical "A Dads Club event is…" copy (from `content.md` §4)
- List of upcoming events as cards (date, location, short blurb, RSVP button → Wix Events)
- Optional: "Past gatherings" section below the fold with photo links

## /contact page

- Simple form (First name, Last name, Email, Message → Send)
- Direct email link: aladds@officialdadsclub.com
- IG link
- Drop the current "Dad's Club Community Events" heading — it's misleading. Use "Get in touch."

## Conversion / CTA hierarchy

1. **Primary, repeated:** Join Dad's Club (external Google Form)
2. **Secondary:** RSVP to next event (per-event detail page → Wix Events)
3. **Tertiary:** Email newsletter signup (on-domain)
4. **Tertiary:** Contact form / direct email

Every page should have the primary CTA reachable in the nav. Home and About should end with it as a section.

## Build requirements (non-negotiables)

These apply across the whole build, not any single page.

- **Responsive at every breakpoint.** Mobile-first. Three breakpoints defined in `visual-direction.md` (S/M/L). No "desktop only" sections — including the nav, hero, event cards, and footer.
- **All links work.** Every internal route resolves (no `/blog-feed`-style 404s carried over). Every external link (Google Form, Wix Events RSVP pages, Instagram, mailto) is tested before launch and opens correctly. External links open in a new tab with `rel="noopener noreferrer"`.
- **Link inventory to verify before launch:**
  - Nav: About, Events, Contact, Join (external Google Form)
  - Footer: Instagram, mailto:aladds@officialdadsclub.com, (future) Privacy/Terms
  - Per-event "RSVP" buttons → correct Wix Events URL per event
  - Newsletter form submits to a real list (not a dead handler)
- **Accessibility floor:** WCAG 2.1 AA minimum. Color contrast checked (the restrained palette in `visual-direction.md` already passes). Alt text on every image. Keyboard navigable. Focus states visible.
- **Performance floor:** LCP < 2.5s on a mid-tier mobile over 4G. Responsive `srcset` on every image (Wix source URLs already support this).

## Open IA questions to revisit later

- A real wordmark/logo asset doesn't exist yet — affects nav (logo slot) and footer.
- Region/locale is unstated on the live site (only "Verplanck, NY" appears, in a past event). Should `/about` name a home region?
- Founder names — currently anonymous on the public site. Worth adding to `/about`?

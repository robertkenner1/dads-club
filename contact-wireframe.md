# Dad's Club — /contact Wireframe

Minimal contact page. Follows `ia.md` (drop the misleading "Dad's Club Community Events" heading, replace with "Get in touch") and `visual-direction.md` (no fill buttons, hairline form borders, restrained).

Nav and footer match Home — see `home-wireframe.md`.

---

## Desktop (L ≥ 1025px)

```
─────────────────────────────────────────────────────────────────────────────
[ nav — same as home ]
─────────────────────────────────────────────────────────────────────────────

   GET IN TOUCH

        Questions, ideas, or want to host a gathering?
        Drop a line.

─────────────────────────────────────────────────────────────────────────────

        First name                       Last name
        ┌──────────────────────┐         ┌──────────────────────┐
        │                      │         │                      │
        └──────────────────────┘         └──────────────────────┘

        Email
        ┌────────────────────────────────────────────────────────┐
        │                                                        │
        └────────────────────────────────────────────────────────┘

        Message
        ┌────────────────────────────────────────────────────────┐
        │                                                        │
        │                                                        │
        │                                                        │
        │                                                        │
        └────────────────────────────────────────────────────────┘

                                                          Send →

─────────────────────────────────────────────────────────────────────────────

   OR REACH US DIRECTLY

        Email       aladds@officialdadsclub.com
        Instagram   @officialdadsclub  →

─────────────────────────────────────────────────────────────────────────────
[ footer — same as home ]
```

## Mobile (S ≤ 640px)

```
┌──────────────────────────────┐
│  Dad's Club    ☰    Join →   │
├──────────────────────────────┤
│                              │
│  GET IN TOUCH                │
│                              │
│  Questions, ideas, or want   │
│  to host a gathering? Drop   │
│  a line.                     │
│                              │
├──────────────────────────────┤
│                              │
│  First name                  │
│  ┌────────────────────────┐  │
│  │                        │  │
│  └────────────────────────┘  │
│                              │
│  Last name                   │
│  ┌────────────────────────┐  │
│  │                        │  │
│  └────────────────────────┘  │
│                              │
│  Email                       │
│  ┌────────────────────────┐  │
│  │                        │  │
│  └────────────────────────┘  │
│                              │
│  Message                     │
│  ┌────────────────────────┐  │
│  │                        │  │
│  │                        │  │
│  │                        │  │
│  └────────────────────────┘  │
│                              │
│  Send →                      │
│                              │
├──────────────────────────────┤
│                              │
│  OR REACH US DIRECTLY        │
│                              │
│  Email                       │
│  aladds@officialdads...      │
│                              │
│  Instagram                   │
│  @officialdadsclub →         │
│                              │
├──────────────────────────────┤
│  [ footer ]                  │
└──────────────────────────────┘
```

---

## Section-by-section notes

### Get in touch (intro)
- Eyebrow "GET IN TOUCH" small-caps sans + an `<h1>` for accessibility.
- Two-line intro in serif body L, indented to cols 2–8 at L.
- Recommended intro copy: *"Questions, ideas, or want to host a gathering? Drop a line."* — open-ended, signals what kinds of messages welcome.

### Form
- Indented to cols 2–8 at L, full-width with side margins at S.
- Two columns at L for First/Last name; stacked at S.
- Email and Message are always full-width.
- Labels sit above each field in small-caps sans (not floating, not placeholder-only — accessibility).
- Borders 1px in Rule color (`#D9CFBE`). No fills. On focus, border darkens to Ink.
- Required fields marked with a hairline asterisk in muted ink, not red.
- Submit: typographic "Send →" text-link right-aligned at L, left-aligned at S. No pill, no fill.
- Success state: form area replaced with a single line in serif italic — *"Thanks. We'll be in touch."* Don't keep the form visible after submit.

### Or reach us directly
- Eyebrow "OR REACH US DIRECTLY" small-caps sans.
- Two rows: label (small-caps sans) left, value (serif) right.
- Email is a plain `mailto:` link.
- Instagram link opens in new tab with `rel="noopener noreferrer"`.
- This section exists for visitors who don't want to fill out a form. Don't bury it.

## States / edge cases

- **Validation error:** field border shifts from Rule to muted ink (not red), error message in small-caps sans muted ink directly under the field. Wording is plain: *"Email looks off — try again?"* Not aggressive.
- **Submission failure (network error):** form stays visible; banner above Send button: *"Couldn't send. Try again or email us directly →"* with mailto link inline.
- **Spam protection:** invisible honeypot field, no captcha. Captchas break the tone.

## CTA hierarchy on this page

| Tier | CTA | Where |
|---|---|---|
| Primary (page-level) | Send | Form submit |
| Secondary | Email (mailto) | Reach us directly section |
| Secondary | @officialdadsclub | Reach us directly section |
| Background | Join Dad's Club | Nav only |

This page intentionally does **not** push Join. Contact is for existing or curious people; the nav handles the conversion path.

## Open questions

- Where does the form actually submit? Wix has native forms — recommend using that (data lands in Wix dashboard, no extra integration). If you need email forwarding, configure to forward to `aladds@officialdadsclub.com`.
- Is there a phone number to add? Not currently on the live site. Probably keep it email-only — fits the calm tone.
- Hours / response time line under the intro? Could add *"We usually reply within a few days."* — sets expectation, signals it's a community not a help desk.

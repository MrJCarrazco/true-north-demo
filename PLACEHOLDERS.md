# PLACEHOLDERS — true-north-collective demo (must resolve BEFORE commissioning)

Prospect: **True North Collective LLC**, 14301 E Soapstone Rd, Palmer, AK 99645 · (907) 795-4106
Repo: `MrJCarrazco/true-north-demo` · Live: https://mrjcarrazco.github.io/true-north-demo/

## VERIFIED — safe to show (sourced, not invented)

| Item | Value on page | Source |
|---|---|---|
| Legal name | True North Collective LLC | thematsualaska.com listing title |
| Phone | (907) 795-4106 | thematsualaska.com listing + Facebook page "Intro" block |
| Address | 14301 E Soapstone Rd, Palmer, AK 99645 | thematsualaska.com listing (matches AK business registry per prospect research) |
| Email | TrueNorthCollectiveAK@gmail.com | Facebook page Intro + listing `mailto:` link |
| **Line of business** | Mat-Su Valley guide / trip planning + brewery & winery tasting tours + excursion transfers | thematsualaska.com listing **About copy, written by the business** |
| Service area (Palmer, Wasilla, Talkeetna, Willow, Houston, Sutton) | 6 chips + marquee + "6 Valley communities served" | listing About copy, verbatim town list |
| Tour format: small-group, small bus or van | feature card + tags | listing About copy, verbatim |
| Private parties up to 4 ride directly | trust band "up to 4" + tag | listing About copy, verbatim |
| Remote-excursion round-trip rides | service card 03 | listing About copy, verbatim |
| Pull-quote ("Most people drive right past…") | quote band, attributed with live source link | listing About copy, **verbatim quote of their own words** |
| Facebook categories: Community Organization · Business Consultant · Travel & Transportation | informed tone/positioning only, not stated as a claim | facebook.com/TrueNorthCollective |

## PLACEHOLDERS / UNVERIFIED — visible on page as placeholders or omitted

| Item | Status on page | Action before live |
|---|---|---|
| **Business hours** | **Visible dashed placeholder box** reading "Office hours and the seasonal tour schedule go here… nothing invented" | Owner supplies hours + season |
| **Tour schedule / departure times** | Not shown (same placeholder box) | Owner supplies |
| **Pricing** | Not shown anywhere | Owner decides whether to publish |
| **Star rating / review count** | **Deliberately omitted.** Facebook shows "Not yet rated (3 reviews)" — there is no rating to display | Do not add until a real rating exists |
| **Years in business** | **Deliberately omitted** — newly registered LLC | Omit, or owner states a real founding year |
| **Certifications / licences / permits** (tour operator, USDOT, commercial passenger) | **Deliberately omitted** — none found in any public source | Owner confirms; add badge only if real |
| **Owner name** | Not shown. FB copy is first-person ("At the heart of everything I do…") so it appears owner-operated, but no name is published | Confirm before any personalisation |
| Map pin | OSM street-level geocode of **East Soapstone Road** (61.6662, -149.1226). House number 14301 did **not** geocode. Caption states it is approximate | Owner confirms exact pin |
| Vehicle fleet detail | Only "small bus or van" (their words). No capacity/make/photos | Owner supplies |
| Logo / brand colours | Text + generic compass SVG. No logo used (no permission) | Request logo + colours |
| Photography | **Zero photos** — all visuals are hand-coded SVG/canvas (aurora, mountain ridge, compass, tasting glasses). No stock photos implying their trips | Swap in the owner's real Valley photos |
| Inquiry form | Disabled (JS `alert`) | Wire `action="https://formsubmit.co/TrueNorthCollectiveAK@gmail.com"` on commission |
| `robots noindex` | **ON** | Remove ONLY after commissioning + owner approval |
| Domain | none; demo on github.io | Check availability on commission |

## Disambiguation warning (important)
Web search for "True North Collective" returns **several unrelated businesses** that must NOT be
blended into this page: a leadership/career coaching firm (truenorthcollective.info, Dr. Alicia
Reddin), a food-systems consultancy in Erwinna PA (tncollective.com), a sustainability consultancy
in Monona WI, a Michigan cannabis operation, a Seattle leadership consultancy (Rachel Ligtenberg),
and a podcast. An Instagram "16 BARS" performance series under a similar handle
(truenorthcollective.co) is also **not** confirmed to be this business. Only
`thematsualaska.com/listing/true-north-collective-llc/` and
`facebook.com/TrueNorthCollective` (Palmer AK, 907-795-4106) were used.

## No fabricated claims
No reviews, no ratings, no years in business, no certifications, no testimonials, no customer
counts, no "award-winning", no stock photos of other people's tours. Every number on the page is
either derived from their own published copy (6 towns, up to 4 passengers) or a factual status
(registered Alaska LLC, direct line to owner).

## Agency identity
Visible agency credit is **"Digital Consulting Studios"** only. No personal human byline appears
anywhere in the page copy (verified by grep for "Juan"/"Carrazco" against the served bytes).

## Pitch hooks surfaced by this research
- Their "Visit Website" button on the Mat-Su visitor directory points at **Facebook**, not a site —
  the directory sends them traffic that lands on a social page with no booking path.
- Facebook page is **"Not yet rated"** with 3 reviews — no review engine working for them yet.
- They sell **logistics and planning**; an inquiry form with dates + group size is the single
  highest-value thing a one-pager can give them.

## Bugs found and fixed during this build (all verified live)
1. **Blank hero for reduced-motion users.** Hero elements start at `opacity:0` and rely on a CSS
   entrance animation, while `@media (prefers-reduced-motion: reduce){*{animation:none!important}}`
   disables that animation — so the headline, CTAs and phone number never appeared. Fixed with a
   reduced-motion override forcing the end state.
2. **Artwork overlapped the feature heading** on narrow phones. The absolutely-positioned tasting-
   glasses SVG sat on top of "Brewery & Winery Tasting Tours". Fixed by returning it to normal flow
   below 560px.
3. **Counter displayed "0"** until its animation finished, and would have stayed "0" permanently if
   JS were throttled — i.e. "0 Valley communities served", a false statement. The real value now
   lives in the HTML and is only animated when motion is allowed.
4. **Aurora canvas animated forever**, including when scrolled off-screen or in a background tab.
   Now paused via IntersectionObserver + `visibilitychange` (mobile battery).

### ⚠ Same bug #1 exists in other demos in this folder — NOT fixed here (out of scope)
`master-auto-repair/index.html` has **6** hero elements at `opacity:0;animation:rise…` and **zero**
reduced-motion override. Any prospect whose phone has "Reduce Motion" on (common on iOS for battery
and accessibility) sees a **blank hero** — no headline, no CTA, no phone number. That demo is
already deployed at `mrjcarrazco/master-auto-demo`. Recommend applying the same override block
before it is shown to that owner. `ohana-grindz` appears to already carry an override;
`er-automotive` does not use the pattern.

## Deploy gate
Deploy pre-approved per demos model (precedent: `master-auto-repair` → mrjcarrazco/master-auto-demo)
and explicit task approval. Pages repo: `mrjcarrazco/true-north-demo`, main / root.

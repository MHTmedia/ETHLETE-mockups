# ETHLETE Design System

A working design system for **ETHLETE** (ethlete.com), rebuilt from the storefront capture in
the attached Figma file. It exists so CRO mockups, test variants and client-review sections can
be produced at production fidelity without re-deriving the brand each time.

---

## The brand

ETHLETE was founded by husband-and-wife duo Shelbi and Geoff around authenticity, transparency
and science-backed wellness. Family-owned, based in Dallas, TX. The product is an electrolyte
stick formulated with Ivy-League scientists: clinical doses of electrolytes, creatine and
essential vitamins (B6, B12, C), no artificial colours or fillers, positioned to support
hydration, muscle recovery, mental focus and cellular hydration.

The proprietary delivery system is branded **E-CELL™**.

### Products in the source

| Product | Price |
| --- | --- |
| ETHLETE Starter Kit (3 bags + bottle + frother) | $109.00 — merchandised at $99 vs $299 |
| Electrolytes + Creatine (3-Pack Bundle) | $99.00 |
| Electrolytes + Creatine (30 sticks) — Peach Mango / Raspberry Lemon / Lemon Lime | From $48.00 |
| 12 Stick Variety Pack (4 of each flavor) | $35.00 |
| Frother | $29.00 |
| NAD+ (NMN + Resveratrol) | From $38.00 (was $64.00) |

### Surfaces

One product: the **Shopify storefront**. Four page types exist in the source — homepage,
collection (PLP), product (PDP) and cart — at 1440w desktop and 414w mobile, plus a mobile
navigation frame.

### Sources given

- **Figma file:** `ETHLETE Design System.fig`, mounted as a virtual filesystem. Pages: `HP`
  (Desktop, Mobile, Mobile-Navigation), `PLP` (1440w, 414w), `PDP` (1440w, 414w), `Cart`.
  The file is an html-to-design capture of the live site, so its component sets carry
  auto-generated names (`Component 1` … `Component 21`, `variant=N`) rather than designer names.
  All values in this system were transcribed from that file's JSX, not from memory of the brand.
- **Company description:** supplied in the brief (quoted above).
- No codebase, repository or slide deck was provided.

---

## Content fundamentals

**Voice: plain, imperative, second person.** The site talks *to* you and rarely about itself.
"Drink water like you mean it." "Make it count." "Upgrade your hydration." Where it does use
first person it is inclusive and short — "Join us." — never corporate "we at ETHLETE believe".

**Claims are structural, not adjectival.** The core pitch is a negative-space argument: name
what competitors leave out, then list what ETHLETE adds.

> **Your Electrolytes Are Incomplete.**
> ETHLETE goes further.
> · Electrolytes to support fluid balance
> · Creatine to support strength and muscle energy
> · B Vitamins to support mental focus and fatigue reduction
> · C Vitamins to support immune function
>
> No sugar. No artificial fillers. No crash.

That closing triplet is the brand's signature rhythm: three short negations, full stops between
them, no conjunction.

**Casing.** Sentence case for headlines and body. UPPERCASE only for buttons, nav, eyebrows and
micro-badges — always with letter-spacing (1.2px on eyebrows, 1.4px on buttons, 1px on badges).
Never uppercase a headline.

**Punctuation.** Headlines take full stops ("Join us.", "Your Electrolytes Are Incomplete.").
Benefit bullets do not.

**Numbers are specific and unrounded.** "5g Creatine", "Vitamin B12 (10mcg)", "4.96 ★ (4,483)",
"Free shipping on orders over $29", "Delivered every 90 days", "SAVE $13.00". The precision is
the proof; never round these in a mockup.

**Emoji: exactly one place.** The announcement ticker, one emoji per claim, always leading:
💧 Hydrate Faster · 💪 Train Stronger · 🧠 Think Sharper · 🔋 Fight Fatigue · ⚡ Recover Better.
Emoji appear nowhere else — not in body copy, buttons, headings or product text.

**Trademarks and seals are stated flatly** — "E-CELL™", "Third Party Tested", "Vegan and
Non–GMO" (note the en-dash in Non–GMO as the site sets it).

**Vibe:** clinical confidence with a consumer-sport edge. Lab language ("clinically studied",
"third party tested") sitting next to gym language ("Train Stronger"). Not wellness-soft, not
bro-y.

---

## Visual foundations

**Colour.** Seven colours, and that is the whole system — set by Brand Guidelines v1.1, which read
its values straight out of the live theme. **Volt** `#E5FF01` is the only accent: high-intent
buttons, badges, highlights, always with black text. **Ink** `#000000` and **Charcoal** `#212121`
carry the wordmark, headlines, primary buttons and every border. **White** is the default page —
the packaging is white, so the site should feel like the product. **Mist** `#F7F9FA` and **Bone**
`#F3F3E4` are the two alternate grounds (cards, inputs, alternating and warm section bands).
**Confirm Green** `#035B00` covers sale badges, in-stock, savings and quick-add confirmation.

Distribution is **60 / 30 / 10** — 60% white and near-white, 30% Ink and Charcoal for type and
structure, 10% Volt for the things you actually want clicked. Volt loses all of its power the
moment it is used for decoration; if it appears twice on a screen it has stopped meaning anything.

Three flavour triads (Peach Mango, Lemon Lime, Raspberry Lemon) sit alongside for selectors,
swatches and PDP accents. They are photo-sampled, not lifted from the print artwork — confirm
against the print files before using one as a large flat fill.

There are no gradients in the UI except two near-invisible black scrims over the hero (10% opacity).

**Type.** Two faces. **Eurostile Bold** for display — the same squared geometric construction as
the wordmark, used for hero headlines, section headers and short high-impact statements only.
**Poppins** for everything else: body, subheads, navigation, buttons, product detail and legal
lines, shipping at Light 300, Regular 400, Medium 500 and Bold 700.

Hero runs 60–72px desktop / 40–50px mobile, section headlines 40–46 / 28–30, sub-headlines 28–34 /
22–24, card titles 18–22 / 18. Body is **16px everywhere and never lower** — 83% of traffic is
mobile. Line length caps around 70 characters at 1.5–1.6 line-height. All-caps is for eyebrows,
buttons and badges only. Two weights per screen; a third means the hierarchy is wrong.

Inter and Instrument Sans, which the live storefront still serves, are **not** brand fonts and are
no longer referenced anywhere in this system. Eurostile is licensed and not yet purchased — see
*Open item: typeface* below.

**Spacing and layout.** 1440px canvas, 34px page gutter (50px on wide editorial bands), 50px
vertical section padding. The 76px header is white and sticky, with the wordmark absolutely
centred and the menu and account/cart flanking it. Product info panes are exactly 10px 20px.
Grids are 3-up on desktop and use 0 or 32px gaps — the PLP grid tiles butt against nothing, each
in its own 1px black box.

**Backgrounds and imagery.** Photography does all the atmospheric work; there are no patterns,
textures or illustrations anywhere. Two image registers: bright, high-key product stills on
near-white sweep with the real fruit alongside the pouch, and warm daylight lifestyle photography
of real people. Colour is warm and saturated, never graded cool or desaturated, never grain.
Flavour cards crop their imagery to a perfect circle. The comparison section ships as a single
flattened image on the live site.

**Corners.** Deliberately near-square. 0 on cards, images and grid tiles; 3px on buttons, inputs
and selects; 2px on micro-chips and breadcrumb pips; 10px on purchase-option cards, savings
badges and radios; 50% only on flavour crops and the sale disc. There is no pill radius in the
system.

**Cards.** A card is a 1px solid black box with no radius and no shadow — the PLP tile is a black
rectangle split by a rule between the image and the info pane. The only card that carries a
shadow is the *selected* purchase option (`0 2px 4px rgba(0,0,0,0.22)`). Nothing floats.

**Shadows.** Four, all short and low-opacity: `0 2px 4px rgba(0,0,0,.22)` (selected option),
`0 2px 4px rgba(0,0,0,.15)` (sticky bar, promo tab), `0 4px 12px rgba(0,0,0,.09)` (popouts),
`0 0 20px rgba(0,0,0,.2)` (drawer overlay). No inner shadows in layout; the one `inset` in the
source is a rendering artefact of a radio dot.

**Borders.** Two weights only. 1px black is the structural rule — cards, inputs, accordions,
toolbars. 1px `#D1D1D1` is the hairline used for dividers and the footer supporting bar.

**Hover.** Buttons **invert** rather than darken: solid black flips to white-on-black-border;
the lime accent deepens to `#CFE700`. Links drop to ~60% opacity. Product images cross-fade to a
second shot over 400ms and reveal a blurred quick-add strip (`backdrop-filter: blur(5px)`) across
the bottom 40.5px. Everything transitions at 200ms `cubic-bezier(.25,.1,.25,1)`.

**Press.** No scale, no bounce, no spring anywhere. Pressed state is the hover state.

**Transparency and blur.** Used twice: the quick-add strip's 5px backdrop blur, and the 36%
black scrim behind the cart drawer. Otherwise everything is opaque.

**Fixed elements.** Three persist across every page: the sticky 76px header, the lime "15% OFF"
disc pinned lower-left, and a back-to-top control lower-right. On the PDP a fourth appears — the
bottom add-to-cart bar.

**Motion.** One continuous animation: the announcement ticker, ~30s linear, infinite. Everything
else is a state transition. No parallax, no scroll-triggered reveals, no entrance animations.

---

## Iconography

**A single 24px line set, extracted from the source file** and shipped as
`assets/icons/icon-data.js` (29 semantic glyphs) with a React wrapper at `components/core/Icon.jsx`.
These are the site's own glyphs, not a substitute library — the stroke weight is light
(~0.5–1.2px at 24px), corners are square, and everything paints with `currentColor`.

Sizes in use: **14** (review stars), **18** (footer socials), **20** (accordion +, PDP
reassurance lines), **24** (header account and cart), **25** (PDP icon columns).

Glyph roles: `account` · `cart` · `cart-outline` · `cart-add` (quick add) · `menu` · `plus`
(accordion, rotates 45° to close) · `chevron-down/left/right` · `arrow-up` (back to top) ·
`arrow-left/right` (carousel) · `instagram` `facebook` `x` `tiktok` (footer socials) · `flag-us`
(currency selector) · `verified` · `check-circle` · `play` (UGC tiles) · `star` `star-half`
`star-empty` · `truck` `shield` `leaf` `sparkle` `zero-sugar` (reassurance and PDP columns) ·
`wordmark`.

**Emoji as iconography:** only in the announcement ticker (see Content fundamentals).
No unicode characters are used as icons; no icon font is loaded. **No CDN icon library is used
and none should be added** — if a mockup needs a glyph the set does not have, flag it rather
than mixing in Lucide or Heroicons.

**Certification seals** (`assets/badge-*.png`) are bitmap illustrations, not icons — NO SUGAR,
PLANT BASED, LAB TESTED, NON GMO, FEMALE FOUNDED. Use the files; never redraw them.

---

## Index

| Path | What it is |
| --- | --- |
| `styles.css` | Global entry point — `@import` list only |
| `tokens/` | `colors.css`, `typography.css`, `space.css`, `base.css`, `fonts.css` — the shipped token set |
| `reference/` | Raw Figma-Variable dump (`figma-variables.css`, `figma-text-styles.css`), kept as provenance and deliberately **not** imported |
| `assets/` | Wordmarks, product photography, lifestyle imagery, certification seals, `icons/icon-data.js` |
| `components/` | The reusable library (below) |
| `guidelines/` | 21 foundation cards (Colors · Typography · Spacing · Brand · Voice · Commerce rules) |
| `ui_kits/storefront/` | Clickable four-screen recreation of ethlete.com |
| `ui_kits/sections/` | 12 standalone, client-reviewable CRO sections |
| `templates/` | Two starting templates consuming projects can copy: **Landing page** and **CRO variant review** |
| `SKILL.md` | Agent Skills entry point |

### Components

**`components/core/`** — `Button`, `Badge`, `SaleBubble`, `SectionLabel`, `Divider`, `Eyebrow`, `Icon`

**`components/forms/`** — `TextField`, `TextInput`, `Select`, `PopoutSelect`, `Radio`, `Checkbox`, `NewsletterForm`

**`components/commerce/`** — `ProductCard`, `Price`, `PurchaseOptions`, `PurchaseOption`, `ProductGallery`, `StickyAddToCart`, `PromoTab`

**`components/navigation/`** — `Header`, `NavLink`, `IconButton`, `Breadcrumbs`, `CollectionToolbar`, `Footer`, `BackToTop`

**`components/content/`** — `Hero`, `BrickSection`, `AnnouncementBar`, `Accordion`, `AccordionItem`, `StarRating`, `ReviewTile`, `FeatureColumns`, `IconColumn`, `FlavorCard`, `TrustBadges`, `FeatureLine`

Each directory carries `<Name>.jsx`, `<Name>.d.ts`, `<Name>.prompt.md` and one `@dsCard` HTML.

---

## Notes on the source, and intentional additions

### Coverage against the Figma kit — 40 built, 14 intentionally skipped

**On the component inventory.** The `.fig` reports 54 "component families", but they are
html-to-design artefacts: every family is named `Component N` and every variant `variant=N`,
and the great majority are *icon glyph variants* of three large sets (68, 66 and 40 variants
respectively) plus per-link hover pairs. They do not describe a designed component library. The
inventory in `components/` is instead derived from the **UI those frames actually render** — one
component per repeated storefront pattern, with every value transcribed from the source JSX.
Nothing here was invented from a generic design-system checklist; there is no Tooltip, Toast,
Avatar, Tabs or Dialog because the storefront has none.

**Every built component is an intentional rename.** All 42 named exports (`Button`, `ProductCard`,
`PurchaseOption`, `AnnouncementBar`, …) carry semantic names because the kit's own vocabulary —
`Component 1`, `Component 12`, `variant=3,:hover=false` — is not usable by a designer or an
agent. The mapping from kit family to built component is:

| Kit family (node) | Built as |
| --- | --- |
| `Component 6` / `Component 5` (button symbols, 4–14 variants × hover) | `Button` |
| `Component 2` (logo lockup symbol) | wordmark bitmaps in `assets/` + `Header` / `Footer` |
| `Component 5` / `Component 12` (nav + footer link symbols) | `NavLink`, `Footer` links |
| `Component 15` / `Component 9` (46×34 header targets) | `IconButton` |
| `Component 3` (68 + 66 variants), `Component 2` (40 variants), `Component 10` (star, 3 variants) | `Icon` + `assets/icons/icon-data.js` (29 semantic glyphs) |
| `Component 8` + `Component 9` (product image pane + title/price pane) | `ProductCard`, `Price` |
| `Component 13` / `Component 14` (newsletter input + submit) | `TextField`, `NewsletterForm` |
| `Component 16` (currency popout), `Component 17` / `Component 18` (supporting-menu links) | `PopoutSelect`, `Footer` supporting bar |
| `Component 20` (accordion toggle), `Component 21` (btn plus) | `Accordion`, `AccordionItem` |
| `Component 1` (in-page skip links), `Component 4` (visually-hidden mask groups) | *skipped* |
| `Component 7` (product image link with hover swap) | folded into `ProductCard` |
| `Component 11` / `Component 19` (per-page link hover pairs, no geometry) | folded into `NavLink` |

#### All 54 kit families and their disposition

The importer scoped components per page, so most families appear three times — once under
`/HP/external`, once under `/PLP/external`, once under `/PDP/external`. Every row below is one
family as `/METADATA.md` lists it.

| # | Kit family (variants) | Disposition |
| --- | --- | --- |
| 1 | `Component 1` (15) | **Skipped** — 1×1px in-page "skip to content" link, no visual design |
| 2 | `Component 1` (7) | **Skipped** — duplicate of #1, PLP-scoped |
| 3 | `Component 1` (7) | **Skipped** — duplicate of #1, PDP-scoped |
| 4 | `Component 10` (17) | Built → `Icon` (glyph variants) |
| 5 | `Component 10` (4) | Built → `NavLink` (hover twin) |
| 6 | `Component 10` (3) | Built → `Icon` `star` / `star-half` / `star-empty` |
| 7 | `Component 11` (6) | **Skipped** — per-page link hover pair, geometry identical to `NavLink` |
| 8 | `Component 11` (4) | **Skipped** — duplicate of #7 |
| 9 | `Component 11` (19) | Built → `Footer` quicklinks |
| 10 | `Component 12` (27) | Built → `NavLink`, `Footer` links |
| 11 | `Component 12` (17) | Built → duplicate of #10, folded in |
| 12 | `Component 12` (7) | Built → duplicate of #10, folded in |
| 13 | `Component 13` (10) | Built → `TextField` (newsletter input) |
| 14 | `Component 13` (2) | Built → `TextField` hover twin |
| 15 | `Component 13` (4) | Built → `TextField` duplicate |
| 16 | `Component 14` (2) | Built → `NewsletterForm` submit |
| 17 | `Component 14` (4) | **Skipped** — no decodable geometry (legal-link mask) |
| 18 | `Component 14` (4) | **Skipped** — duplicate of #17 |
| 19 | `Component 15` (7) | Built → `IconButton` (header account) |
| 20 | `Component 15` (17) | Built → `Icon` glyph variants |
| 21 | `Component 16` (4) | Built → `PopoutSelect` (currency) |
| 22 | `Component 16` (1) | **Skipped** — 1×1px visually-hidden heading mask |
| 23 | `Component 17` (17) | Built → `Icon` (PDP column glyphs) |
| 24 | `Component 17` (2) | Built → `Footer` supporting-menu link |
| 25 | `Component 18` (1) | Built → `Icon` `arrow-up` / `BackToTop` |
| 26 | `Component 18` (4) | Built → `Icon` boxed arrow variants |
| 27 | `Component 19` (2) | **Skipped** — no decodable geometry, link hover twin |
| 28 | `Component 2` (7) | Built → wordmark lockup → `assets/logo-ethlete*.png`, `Header`, `Footer` |
| 29 | `Component 2` (40) | Built → `Icon` (40-glyph set) |
| 30 | `Component 2` (3) | Built → `Icon` divider rules |
| 31 | `Component 20` (1) | Built → `Accordion` toggle, `Icon` `plus` |
| 32 | `Component 21` (2) | Built → `AccordionItem` plus/close state |
| 33 | `Component 3` (68) | Built → `Icon` (primary 68-glyph set, PDP-scoped) |
| 34 | `Component 3` (1) | **Skipped** — single 1×1px mask node |
| 35 | `Component 3` (66) | Built → `Icon` (66-glyph set, HP/PLP-scoped) |
| 36 | `Component 4` (1) | **Skipped** — visually-hidden mask group, no geometry |
| 37 | `Component 4` (2) | **Skipped** — duplicate of #36 |
| 38 | `Component 4` (1) | **Skipped** — duplicate of #36 |
| 39 | `Component 5` (2) | Built → `NavLink` (menu item) |
| 40 | `Component 5` (1) | Built → `NavLink` duplicate |
| 41 | `Component 5` (2) | Built → `NavLink` duplicate |
| 42 | `Component 6` (2) | Built → `Button` |
| 43 | `Component 6` (28) | Built → `Button` (14 fills × hover) |
| 44 | `Component 6` (14) | Built → `ProductCard` image pane (PLP) |
| 45 | `Component 7` (4) | Built → `Button` link variant |
| 46 | `Component 7` (66) | Built → `ProductCard` image link with hover swap |
| 47 | `Component 7` (2) | Built → `ProductCard` title/price pane (PLP) |
| 48 | `Component 8` (4) | Built → `ProductCard` image pane (HP) |
| 49 | `Component 8` (2) | Built → `FeatureLine` icon slot |
| 50 | `Component 8` (20) | Built → `ProductCard` variants |
| 51 | `Component 9` (3) | Built → `IconButton` (header cart) |
| 52 | `Component 9` (7) | Built → `ProductCard` title/price pane (HP) |
| 53 | `Component 9` (12) | Built → `Price` |
| 54 | `sticky child` (standalone) | Built → `StickyAddToCart` / `PromoTab` |

**14 skipped, and why.** Rows #1–3, #7–8, #17–18, #22, #27, #34, #36–38 — accessibility
scaffolding (1×1px skip links and visually-hidden mask groups with no visual design), per-page
duplicates the importer created three copies of, and link hover twins whose only variant axis is
`:hover: 2` over a family already built (hover is a prop on the built component, not a separate
export). None of them describes a visible storefront pattern.

**No storefront pattern visible in any frame is missing from `components/`.**

#### The 42 built components, each an intentional rename

`Button` · `Badge` · `SaleBubble` · `SectionLabel` · `Divider` · `Eyebrow` · `Icon` ·
`TextField` · `TextInput` · `Select` · `PopoutSelect` · `Radio` · `Checkbox` · `NewsletterForm` ·
`ProductCard` · `Price` · `PurchaseOptions` · `PurchaseOption` · `ProductGallery` ·
`StickyAddToCart` · `PromoTab` · `Header` · `NavLink` · `IconButton` · `Breadcrumbs` ·
`CollectionToolbar` · `Footer` · `BackToTop` · `Hero` · `BrickSection` · `AnnouncementBar` ·
`Accordion` · `AccordionItem` · `StarRating` · `ReviewTile` · `FeatureColumns` · `IconColumn` ·
`FlavorCard` · `TrustBadges` · `FeatureLine` · `Video` · `VideoHero` · `VideoRail`

Every one maps to a row in the table above, except the three media components — the kit has no
video at all (an html-to-design capture cannot carry a `<video>` element), so they are additions
rather than renames. See the media-library section at the end of this file.

Every other one maps to a row in the table above. None is named after the kit because the kit has no
names to borrow — `Component 12`, `variant=3,:hover=false` is not a vocabulary a designer or an
agent can use. **These renames are intentional and are the public API of this system.**

**Intentional additions** (things not present as a named component in the source, added because
the system is unusable without them):

- `Icon` — a wrapper over the extracted glyph set, so consumers reference `name="cart"` instead
  of inlining path data.
- `Checkbox` — the source has radios but no checkbox; added in the same idiom for form mockups.
- `TextInput` — a boxed variant of the footer's underline field, for checkout-style forms.
- `Video` / `VideoHero` / `VideoRail` — the kit carries no video whatsoever, but the brand's
  media library is roughly half video and CRO tests lean on it heavily. One primitive with a
  `mode` prop (`ambient` / `ugc` / `gallery` / `testimonial`) so pages never hand-roll a
  `<video>` tag and lose the playback contract. See `components/media/Video.prompt.md`.
- `Cart` drawer (in the storefront kit) — the source's Cart page is a flattened screenshot with
  no measurable structure, so the drawer is composed from existing primitives. Flagged in
  `ui_kits/storefront/README.md` as a proposal rather than a recreation.

**No logo file beyond the wordmark.** ETHLETE has one mark and no icon, monogram or alternate
lockup. This kit holds bitmap lockups only (`assets/logo-ethlete.png` light,
`assets/logo-ethlete-footer.png` dark, plus the `wordmark` glyph). The guidelines ship SVG
(currentColor, black, white) plus four PNG sizes — drop those into `assets/` and repoint
`guidelines/logo.card.html`. Aspect ratio is **6.575:1** and must never be distorted; minimum
width 110px on screen; clear space equals the cap height of the "E" on all four sides; keep the ®.
Never retype the wordmark in a similar font, recolour it, or let an image model draw it. Note that
even the guidelines' SVG was traced from PNG rather than original artwork — if the designer still
has the .ai or .eps, that is the file to use.

**Fonts.** Poppins is loaded from Google Fonts in `tokens/fonts.css` at 300/400/500/700 — free,
confirmed, the whole site's range in a small payload. Eurostile is licensed and not bundled, so
`--font-display` declares it first and falls through to **Saira**, the closest free squared-
geometric stand-in, so display type renders in the right spirit without pretending the licence
exists. Buy the licence, drop the webfont files in, and the stack picks them up with no other
change.
**On the raw Figma variables.** The importer emitted 225 "variables" that are almost entirely
scraped geometry — `--width-224-93`, `--height-399-88`, `--opacity-97-74`, one per measured node.
They are not a token system, and one of them (`--font-family-font-3: "Hiragino Sans"`) is the
macOS system fallback the browser resolved while scraping, not an ETHLETE typeface. That whole
dump now lives at `reference/figma-variables.css` and is **deliberately not imported** by
`styles.css`, so consumers get the 134 curated tokens instead of 359 mixed ones. The file is kept
as a provenance record; if you need to trace a value back to the capture, it is there. **No font
should be uploaded for `Hiragino Sans`** — the three real families are Inter, Instrument Sans and
Poppins, all loaded in `tokens/fonts.css`.


---

## Brand Guidelines v1.1 alignment (Aug 2026)

`uploads/ETHLETE_Brand_Guidelines.pdf` is now the authoritative source for logo, colour, voice and
imagery. Where it disagreed with the storefront capture this system was built from, the guidelines
won. What changed:

**Removed — stale values the guidelines name explicitly.** Blue is not an ETHLETE colour. Gone:
`--eth-blue` `#061C81`, `--eth-navy` `#192F5D`, `--eth-teal` `#3EB2A2`, plus the two off-palette
limes `--eth-lime-bright` `#CCFE3F` and `--eth-lime-soft` `#D8ED7D`. `Badge` (lime tone) and
`StickyAddToCart` moved onto Volt; both were the only consumers.

**Focus rings got their own treatment.** They previously borrowed the blue. Now `--focus-ring`
(Ink, with a white spacer ring so it reads on Mist, Bone and Volt alike) and
`--focus-ring-inverse` (Volt, on Ink or dark photography, via `.on-dark` /
`[data-surface="inverse"]`).

**Renamed to the guidelines' vocabulary,** with the old names kept as aliases so all 42 shipped
components keep resolving: `--eth-volt`, `--eth-bone`, `--eth-confirm-green`, `--eth-charcoal`.
`--eth-mist` `#F7F9FA` is new and `--eth-grey-92` `#F7F7F7` now points at it, moving components
onto the brand value. `--eth-green-deep` `#03682D` folded into Confirm Green — the palette has one
green.

**Type moved onto the brand faces.** `--font-ui` is Poppins; `--font-display` is Eurostile with a
Saira fallback. `--font-editorial` and `--font-accent` survive as deprecated aliases. A role-based
scale (`--fs-hero` … `--fs-legal`) replaces the scraped sizes, which are kept in a clearly marked
legacy block. Body defaults moved 14px → 16px per the mobile floor, which shifts some component
metrics slightly — that is the guidelines' rule, not drift.

**New cards.** *Core palette*, *Flavour accents*, *60 / 30 / 10*, *Feedback & focus*, *Type scale*,
*Open item: typeface*, *How ETHLETE sounds*, *Writing for the site*, *Claim guardrails*,
*Subscription & ARL*, *Web & CRO notes*. Logo and Imagery were rewritten with the do/don't rules.
Voice and Commerce rules are new groups.

### Open items — do not design around a guess

1. **Typeface.** Brand standard is Eurostile Bold + Poppins; the live site ships Inter and
   Instrument Sans. Eurostile carries a licence cost. Either the site moves or the standard
   changes. Confirm with Geoff before wireframes go to design.
2. **A true vector wordmark.** The guidelines' SVG was traced from PNG. Prefer the original .ai/.eps.
3. **No error colour is specified.** The palette has Confirm Green and no failure state.
   `--eth-red` `#BD3D44` is carried over from the theme and is **not** brand-approved.
4. **Flavour accents are photo-sampled**, accurate to within a shade. Confirm against print files
   before any large flat fill.
5. **Favicon / app-icon source** is a separate mark, not supplied.
6. **Packaging explorations** in the Figma file may be a forthcoming redesign or superseded work.
   Until settled, all creative uses the currently shipping white pouch.
7. **No icon system is defined by the brand.** This kit ships the storefront's own extracted
   24px line set, which satisfies the guidelines' "single consistent library, squared and
   geometric" requirement. Don't mix in Lucide or Heroicons.

### Rules that constrain the build, not just the look

**Subscription is a legal surface.** ETHLETE's subscription copy was rewritten for California's
ARL after a subscription-related suit. Auto-renewal terms must sit adjacent to the purchase button
(never in a tooltip or accordion), consent to the recurring charge must be affirmative and
separate from the purchase itself, and cadence, renewal price and cancellation must be visible at
the point of decision in legible type. Making subscription the higher-converting choice is the
goal; making it the *accidental* choice is exposure. Applies to `PurchaseOptions`,
`PurchaseOption` and `StickyAddToCart`.

**Claims are non-negotiable.** Never state or imply the product diagnoses, treats, cures or
prevents anything. The FDA disclaimer stays on every product page and must survive the PDP
redesign. Doses must match the current label exactly — never round. Reviews come live from
Judge.me; never hard-code, round up, or write a testimonial.

**Accessibility floor.** WCAG AA on all text. Volt is black-text-only (white on Volt is 1.1:1).
Visible focus on every interactive element. Tap targets 44px minimum (`--tap-min`). Alt text
describes the product, not the file name.

---

## Media library

Images and video ship **inside** the system — a design system cannot reference a local folder or a
Figma file at runtime, so every asset a component uses is copied into `assets/`.

```
assets/media/
  photography/editorial/   20  brand shoot (ETHLETE_-*)
  photography/product/     11  studio pack shots (PRODUCT2-*, Product4-*)
  photography/studio/      18  photographer set (JMA*)
  photography/lifestyle/   60  on-location and UGC stills (IMG_*)
  graphics/                 6  generated and social graphics
  video/ugc/                7  creator and code clips
  video/brand/              9  brand and social cuts
  video/raw/               31  unsorted camera clips
  media-manifest.json          full index, plus what didn't import and why
```

**115 images, 47 clips.** Filenames keep their source stems (`jma08600.jpg`, `sequence-147.mp4`) so
any asset can be traced back to the original shoot folder. Two `@dsCard` pages under the **Assets**
group make them browsable: *Photography* and *Video* (hover any clip to preview it).

### Video is a component, not a file reference

Never hand-roll a `<video>` tag in a page — mount `Video` and pick a `mode`
(`ambient` / `ugc` / `gallery` / `testimonial`). The mode carries the playback contract
(autoplay, mute, loop, controls) and a fixed-ratio wrapper that reserves space before metadata
loads, so clips never cause layout shift. See `components/media/Video.prompt.md`.

### Two things to know before using video in production

**18 of the 47 clips are HEVC in a QuickTime container** — straight off an iPhone. They play in
Safari and fail in Chromium. `Video` catches the decode failure and falls back to the `poster`,
so pages degrade quietly rather than showing a black box, but these files need re-encoding to
H.264 MP4 before they go live. The list is in `media-manifest.json` under `needsReencode`, and the
*Video* asset card flags them in red.

**No clip has a poster frame yet.** Posters can't be generated here (no video decoder), so they're
currently borrowed stills. Export a real frame per clip at some point — `poster` is the first
paint and the codec fallback.

### Where the source assets live

Two Google Drive folders are the system of record, both recorded in `CLAUDE.md` so they don't have
to be looked up again:

| Folder | Contents |
| --- | --- |
| [Video archive](https://drive.google.com/drive/folders/1dMTRw-mhmsnPFp2V7ZQCikFPEfsTmUwk) | ~27 clips, 24–230 MB each. Creator/ad cuts (named by discount code), `Pool c11–c13`, `Align c2`, `Alex c1`, raw UUID clips. Essentially all above the 30 MiB import limit. |
| [Shoot archive](https://drive.google.com/drive/folders/1dHqdwIl_9i2nhCyJzuyPLbs6M1_HxqSp) | Photography (`IMG_*`, `JMA*`, `ETHLETE_-*`), `Sequence 01_*`, generated graphics. Same archive as the local folder — already imported. |

The video archive is the one worth returning to: it holds the named creator clips this system has no
copy of. It needs an H.264 pass first — the files are 2–8× the import ceiling.

### Not imported

**28 video files exceeded the 30 MiB per-file limit**, including all six `Ethlete Social — Pool`
cuts, the three `Ethlete x Pool` clips, the Poppi founder review, and 14 raw camera clips. **Two
`.heic` photos** can't be decoded in-browser and no converter is available. **Two images** were
rejected on filename characters. Every omission is listed in `media-manifest.json` under
`notImported`. To bring the large clips in, compress them to H.264 MP4 under 30 MiB first — which
is the same step they need for the web anyway.

# Exhibitors.ai Design System V2

> Cross-platform design language for web app, React Native mobile app, and marketing site.
> Source of truth for all visual and interaction decisions.
>
> **Version:** 2.1 | **Updated:** September 2026 | **Jira:** EB-192
>
> **v2.1 — Balanced Blend expressive layer.** Adds light branding and "quiet flair"
> to the functional base: soft geometric decoration in header corners, two-tone
> serif headlines, tonal row surfaces and chips, a count-tile vs. avatar shape
> distinction, and gradient header/hero washes. Everything additive — dense screens
> stay calm. First applied in the mobile app refresh; promoted here for web +
> marketing parity. Two value reconciliations (`--primary-dark` shade, muted-text
> warming) and the text-on-tint contrast set are pending an accessibility review.

---

## Table of Contents

1. [Principles](#principles)
2. [Color Palette](#color-palette)
3. [Typography](#typography)
4. [Spacing](#spacing)
5. [Border Radius](#border-radius)
6. [Elevation & Shadows](#elevation--shadows)
7. [Decoration & Brand Mark](#decoration--brand-mark-balanced-blend)
8. [Components](#components)
9. [Navigation](#navigation)
10. [Interaction Patterns](#interaction-patterns)
11. [Platform-Specific Guidelines](#platform-specific-guidelines)
12. [Implementation](#implementation)

---

## Brand Voice

Exhibitors.ai's visual language projects confident calm in the middle of chaos. Trade shows are loud, overwhelming, and relentless. The warm cream palette, generous whitespace, and serif headings ground users with the steady presence of a plan already in motion. This is a tool built by people who understand what it feels like to come home with 200 contacts and no system. Teal sits at the intersection of composure and conviction. Steady enough to trust with your pipeline, sharp enough to feel like a competitive edge. Inter keeps the interface precise when pressure is real, and the four-accent classification system turns raw contact lists into a clean, considered editorial layout. Restrained shadows and purposeful spacing are not decorative. They say: we will be the calm part of your post-show week.

---

## Principles

1. **Editorial warmth** — Serif headings, cream backgrounds, and generous spacing create authority without sterility.
2. **Intentional color** — Every accent color has a meaning. Teal is the brand. Clay, sage, and slate classify contacts.
3. **Platform-adaptive** — Same design language, adapted to each platform's native patterns. No forcing web patterns onto mobile.
4. **Breathing room** — When in doubt, add more space. The editorial style favors openness over density.
5. **Expressive restraint (Balanced Blend)** — Branding lives at the edges: decoration stays in header corners and behind avatars, never under body copy; the accent shows through two-tone headlines and tonal surfaces rather than heavy chrome. Flair earns its place only where the screen can afford it — dense list and table screens stay essentially undecorated.

---

## Color Palette

### Primary

| Token | Hex | Usage |
|-------|-----|-------|
| `--primary` | `#2A9D8F` | Primary brand, buttons, links, active states |
| `--primary-hover` | `#249185` | Hover state for primary elements |
| `--primary-light` | `#E0F3F0` | Badges, light backgrounds, focus rings |
| `--primary-dark` | `#1E7A6F` | Pressed state, dark-on-dark contexts |

### Accents (Classification System)

| Token | Hex | Light | Meaning |
|-------|-----|-------|---------|
| `--clay` | `#C2783A` | `#F5ECE0` | Existing customers, warm leads, follow-up due |
| `--sage` | `#3D9960` | `#E2F2E6` | Post-engagement, completed, success states |
| `--slate` | `#6882A0` | `#E8EDF3` | Research, informational, neutral |

### Neutrals

| Token | Hex | Usage |
|-------|-----|-------|
| `--ink` | `#1A1A1A` | Primary text, headings |
| `--ink-secondary` | `#444444` | Body text, descriptions |
| `--ink-muted` | `#777777` | Metadata, captions, helper text |
| `--ink-subtle` | `#AAAAAA` | Placeholders, disabled text |

### Backgrounds

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-page` | `#FAF8F4` | Page background (warm cream) |
| `--bg-warm` | `#F5EFE6` | Section backgrounds, hero right panel |
| `--bg-card` | `#FFFFFF` | Card surfaces, modals |
| `--bg-hover` | `#F7F5F1` | Hover state for list items, table rows |

### Borders

| Token | Hex | Usage |
|-------|-----|-------|
| `--border` | `#E0DBD2` | Default borders, dividers |
| `--border-light` | `#EFECE6` | Subtle borders, card outlines |

### Navigation

| Token | Hex | Usage |
|-------|-----|-------|
| `--nav-bg` | `#1A1A1A` | Sidebar background |
| `--nav-hover` | `#2A2A2A` | Nav item hover |
| `--nav-text` | `#999999` | Default nav text |
| `--nav-text-active` | `#FFFFFF` | Active nav text |
| `--nav-label` | `#555555` | Section labels |

### Semantic

| Token | Hex | Light | Usage |
|-------|-----|-------|-------|
| `--success` | `#3D9960` | `#E2F2E6` | Success states, positive changes |
| `--warning` | `#C2783A` | `#F5ECE0` | Warnings, attention needed |
| `--error` | `#C25050` | `#FDE8E8` | Errors, destructive actions |
| `--info` | `#6882A0` | `#E8EDF3` | Informational messages |

### Tonal Row Surfaces (Balanced Blend)

Soft tinted fills for list-row and tonal cards — one step warmer than the `*-light` chip tints — keyed to each item's accent color. Use for list rows, the profile identity card, and tonal action surfaces. Chip tints stay the existing `*-light`.

| Token | Hex | Pair with |
|-------|-----|-----------|
| `--teal-row` | `#E5F1EE` | teal / brand entities |
| `--clay-row` | `#F6EFE4` | existing customers |
| `--sage-row` | `#E6F1E9` | post-engagement |
| `--slate-row` | `#EAEEF4` | research / neutral |

### Text-on-Tint (Tonal Chips)

Darker, same-hue text for a tonal chip (tinted background + accent text of the same family). Pair each with its `*-light` (chip) or `*-row` (surface) tint.

| Token | Hex | On tint |
|-------|-----|---------|
| `--primary-deep` | `#144A43` | `--primary-light` / `--teal-row` |
| `--clay-deep` | `#A85F27` | `--clay-light` / `--clay-row` |
| `--sage-deep` | `#2F6B45` | `--sage-light` / `--sage-row` |
| `--slate-deep` | `#4A5E75` | `--slate-light` / `--slate-row` |

> **Pending accessibility review:** these text-on-tint pairings are the primary thing the v2.1 a11y pass must verify against WCAG AA (4.5:1 for body-size chip text). Adjust the `*-deep` values here — at the token level — if any pair falls short.

### Surfaces (Balanced Blend)

| Token | Hex | Usage |
|-------|-----|-------|
| `--bg-field` | `#EFE8DC` | Search / untinted input fill (alt. to white + border) |
| `--bg-group-header` | `#F2EDE4` | Collapsible group headers (e.g. All Contacts) |

### Gradients

Decoration only — **never** place body copy directly on a gradient; titles and controls sit on the calm areas or on an overlapping card.

| Token | Value | Usage |
|-------|-------|-------|
| `--gradient-header` | `linear-gradient(165deg, #EAF4F0 0%, #FAF8F4 70%)` | Primary-header wash (login, My Lists, contact list) |
| `--gradient-hero` | `linear-gradient(150deg, #2A9D8F 0%, #1A6F64 100%)` | Mobile contact-detail hero (with white/clay decoration circles) |

### Decoration

Soft translucent shapes that bleed from header corners and sit behind avatars. Kept at low opacity and **off the text**.

| Token | Value | Usage |
|-------|-------|-------|
| `--decor-teal` / `--decor-clay` / `--decor-slate` | brand hexes | Fill colors for decorative circles |
| `--decor-opacity-min` → `--decor-opacity-max` | `0.06` → `0.14` | Opacity range for background shapes |

> **Open reconciliation (for the a11y pass):** the mobile refresh proposed a slightly deeper primary (`#1A6F64`, used as the hero endpoint) and a warmer muted text (`#7A736A`) than the shipped `--primary-dark #1E7A6F` / `--ink-muted #777777`. These are intentionally **not** adopted as token changes yet — decide during the accessibility review whether to collapse `--primary-dark` to one value and warm the neutrals system-wide.

---

## Typography

### Font Families

| Purpose | Family | Fallbacks |
|---------|--------|-----------|
| Display / Headings | Source Serif 4 | Georgia, serif |
| Body / UI | Inter | system-ui, -apple-system, sans-serif |

### Type Scale

| Name | Size | Weight | Letter-spacing | Line-height | Font | Usage |
|------|------|--------|----------------|-------------|------|-------|
| Display 1 | 56px | 300 | -0.02em | 1.12 | Serif | Hero headlines |
| Display 2 | 44px | 300 | -0.01em | 1.15 | Serif | Section titles |
| Headline 1 | 36px | 400 | -0.01em | 1.2 | Serif | Page titles |
| Headline 2 | 32px | 400 | -0.01em | 1.4 | Serif | Content headers |
| Headline 3 | 18px | 400 | -0.01em | 1.2 | Serif | Card titles, names |
| Body Large | 16px | 400 | 0 | 1.7 | Sans | Marketing copy |
| Body | 14px | 400 | 0 | 1.6 | Sans | Default app text |
| Body Small | 13px | 400 | 0 | 1.5 | Sans | Meta, email previews |
| Caption | 12px | 400 | 0 | 1.5 | Sans | Helper text, footnotes |
| Label | 11px | 600 | 0.06em | 1.2 | Sans (uppercase) | Section headers, badges |

### Font Pairing Rules

- **Serif (Source Serif 4):** Headings, display text, contact/company names, pull quotes, metric values, brand wordmark. Conveys editorial authority.
- **Sans (Inter):** Body text, form labels, button text, nav items, table cells, badges, metadata. Conveys functional clarity.
- **Rule of thumb:** If the text establishes hierarchy or identity, use serif. If the text is actionable or informational, use sans.

### Serif-only titling (Balanced Blend — hard rule)

Source Serif 4 is reserved for **screen titles, headlines, display text, and identity** (contact/company names, brand wordmark). Everything else — body, labels, list-row titles, buttons, chips, metadata, and even *card* section headers ("Details", "Classification") — is Inter, regardless of size. A small heading inside a card is titling-adjacent but still sans. When the webfont fails to load, sans falls back to the system stack so body text never degrades to serif.

### Two-Tone Headlines (Balanced Blend)

Serif headlines carry one accent word. The key word — usually the last — is set in `--primary` (teal); the rest stays `--ink`. This is the lightest-touch way the brand color enters a screen.

- Examples: My **Lists** · Verify it's **you** · Generation **profile** · Your first **contacts** start here
- One accent word per headline; never color the whole line.
- Implementation: wrap the accent word in its own inline span/`<Text>` with `color: var(--primary)`.

---

## Spacing

Base unit: **4px**

| Token | Value | Usage |
|-------|-------|-------|
| `--space-1` | 4px | Icon-to-text gap, badge padding |
| `--space-2` | 8px | Tight element groups, inline spacing |
| `--space-3` | 12px | List item spacing, nav item padding |
| `--space-4` | 16px | Card padding, input padding, grid gap |
| `--space-5` | 24px | Card separation, form field spacing |
| `--space-6` | 32px | Section padding (small) |
| `--space-7` | 40px | Feature block padding |
| `--space-8` | 48px | Content area padding, sidebar padding |
| `--space-9` | 64px | Page section dividers |
| `--space-10` | 80px | Hero padding, major section spacing |
| `--space-11` | 120px | Landing page section spacing |

### Layout

| Property | Value |
|----------|-------|
| Sidebar width (expanded) | 220px (xl breakpoint: ≥1280px only) |
| Sidebar width (collapsed) | 56px (icon-only, below xl) |
| Content max-width | 1200px |
| Dashboard grid | 12-column, 16px gap |
| Email masonry | 3-column, 24px gap |
| Mobile touch target | 44px minimum |

**Sidebar responsive behavior:**
- **≥1280px (xl):** Sidebar auto-expands to 220px with labels and section headers visible
- **<1280px:** Sidebar collapses to 56px icon-only mode — nav items show icon only, tooltips on hover, no section labels

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-xs` | 3px | Badges, status indicators, inline tags |
| `--radius-sm` | 4px | Email cards, data-dense cards, code blocks |
| `--radius-md` | 8px | Buttons, inputs, nav items, tooltips |
| `--radius-lg` | 16px | Dashboard metric cards, bento grid items |
| `--radius-xl` | 18px | Marketing sections, hero visual containers |
| `--radius-full` | 9999px | Avatars, pill buttons, toggle switches |

### Refreshed component radii (Balanced Blend)

The refresh softens interactive controls a step beyond the base scale. Use these on refreshed surfaces; they supersede `--radius-md` for buttons and inputs there (`--radius-md` still applies to nav items, tooltips, and web-dense cards).

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-input` | 10px | Text inputs, selects, textareas |
| `--radius-button` | 12px | Buttons |
| `--radius-tile` | 14px | Count tiles (list/event entities) + tonal cards |
| `--radius-search` | 20px | Search fields |
| `--radius-sheet` | 22px | Bottom-sheet top corners |

**Shape distinguishes entities (hard rule):** list/event entities use **rounded-square** count tiles (`--radius-tile`, 14px); people/contacts use **round** avatars (`--radius-full`). Never round a count tile to a circle or square off an avatar — the shape is how the two read apart at a glance.

---

## Elevation & Shadows

| Level | Value | Usage |
|-------|-------|-------|
| 1 | `0 1px 3px rgba(0,0,0,0.04)` | Resting state for interactive cards |
| 2 | `0 4px 20px rgba(0,0,0,0.06)` | Hover state, dropdowns, popovers |
| 3 | `0 10px 40px rgba(0,0,0,0.06)` | Slide-out panels, toasts |
| 4 | `0 20px 60px rgba(0,0,0,0.08)` | Hero visuals, modals |

**Guidance:** The editorial style relies more on borders and spacing than shadow depth. Use sparingly.

### Component shadows (Balanced Blend)

Warmer, slightly deeper lifts for the refreshed mobile surfaces.

| Token | Value | Usage |
|-------|-------|-------|
| `--shadow-card` | `0 8px 22px rgba(26,26,26,0.1)` | Tonal cards, overlapping detail card |
| `--shadow-fab` | `0 6px 16px rgba(42,157,143,0.4)` | Teal capture FAB |
| `--shadow-modal` | `0 12px 40px rgba(0,0,0,0.3)` | Bottom sheets, center alerts |

---

## Decoration & Brand Mark (Balanced Blend)

The expressive layer. All of it is **background** — it must never sit under or reduce the legibility of text.

### Geometric decoration
- **Circles:** absolutely positioned, `border-radius: 50%`, filled `--decor-teal` / `--decor-clay` / `--decor-slate` at opacity `0.06–0.14`, bleeding off the top corners of headers and behind avatars.
- **Header wash:** `--gradient-header` (`165deg`, teal-tinted → cream) on primary headers.
- **Contact-detail hero (mobile):** `--gradient-hero` (`150deg`, teal → deep teal) with white circles at `.07–.1` and one clay circle at `~.22`; the round avatar breaches the hero's lower edge with a 4px white ring.
- **Restraint:** dense list/table screens carry no decoration; a single header wash at most.

### Hinted brand mark
A placeholder mark until a real logo exists: a small teal **quarter-circle** (16–22px square, `border-radius: 0 0 0 N`) with a 5–7px **clay dot** at its inner/top corner. Appears on primary headers beside an uppercase eyebrow. CSS-drawn; swap for a real logo mark when designed.

---

## Components

### Buttons

| Variant | Background | Text | Border | Usage |
|---------|-----------|------|--------|-------|
| Primary | `--primary` | White | None | Main action per view |
| Dark | `--ink` | White | None | Secondary emphasis |
| Outline | Transparent | `--ink-secondary` | 1px `--border` | Tertiary actions |
| Ghost | Transparent | `--ink-secondary` | None | Low-emphasis actions |
| Danger | `--error` | White | None | Destructive actions |

**Sizes:** Small (32px height, 12px font), Medium (40px height, 14px font), Large (48px height, 15px font)

**States:** Default → Hover (darken 8%) → Active (darken 12%) → Disabled (border-light bg, subtle text)

### Email Cards (Left-Accent Pattern)

The signature component. A card with a 3px left border in an accent color indicating classification.

```
┌──────────────────────────────┐
│▍ Name (serif 18px)           │  ← 3px left accent stripe
│▍ Company (sans 12px)        │
│▍ Role · Classification      │
│──────────────────────────────│
│  Email preview text (sans    │
│  13.5px, line-height 1.8)   │
│  truncated to ~4 lines...   │
│──────────────────────────────│
│  ● Tone    [copy][edit][send]│  ← 30x30px action targets
└──────────────────────────────┘
```

**Accent color mapping:**
- Teal → Pre-engagement (new contacts)
- Clay → Existing customers
- Sage → Post-engagement (follow-up sent)
- Slate → Research / informational

### Metric Cards

```
┌──────────────────────────┐
│  LABEL (11px uppercase)  │
│                          │
│  247 (serif 48px)        │
│  +18% from last week     │
│  (12px sage/error)       │
└──────────────────────────┘
```

Border-radius: 16px. Padding: 24px. Border: 1px `--border-light`.

### Form Elements

| Element | Height | Radius | Focus State |
|---------|--------|--------|-------------|
| Text input | 40px | 8px | 1px teal border + 3px teal-light ring |
| Textarea | min 100px | 8px | Same as input |
| Select | 40px | 8px | Same as input |
| Toggle | 24px tall, 44px wide | Full | Teal when active |

**Error state:** Red border + red-light focus ring + 11px error message below.

### Badges

| Variant | Background | Text |
|---------|-----------|------|
| Primary | `--primary-light` | `--primary` |
| Clay | `--clay-light` | `--clay` |
| Sage | `--sage-light` | `--sage` |
| Slate | `--slate-light` | `--slate` |
| Error | `--error-light` | `--error` |

Style: 10px font, 600 weight, uppercase, 0.06em letter-spacing, 3px radius, 3px 8px padding.

### Tonal Chips (Balanced Blend)

The refreshed, larger classification/status/priority chip: a tinted background with darker same-hue text (the `*-deep` on `*-light` pairing), pill-shaped.

| Variant | Background | Text |
|---------|-----------|------|
| Teal / new lead | `--primary-light` | `--primary-deep` |
| Clay / existing | `--clay-light` | `--clay-deep` |
| Sage / done | `--sage-light` | `--sage-deep` |
| Slate / research | `--slate-light` | `--slate-deep` |

- **Selected (single-select groups):** solid accent fill + white text. **Unselected:** tonal (tint bg + `*-deep` text).
- Detail-view chips: 12px / 600. List-row status chips: 10px / 700 uppercase.
- Radius `--radius-full`. Contrast of every tonal pair is the focus of the v2.1 accessibility review.

### Tonal List Row (Balanced Blend)

A list/event row rendered as a tonal card: `--radius-tile` (14px), background `--*-row` keyed to the item's accent. Contains a **rounded-square count tile** (`--radius-tile`) with the contact count, the list name (sans 15/600), a date range (sans 12, muted), and a chevron. Reserved for browsable entity lists (My Lists); dense contact rows stay flat on paper.

### Count Tile vs. Avatar

The shape distinction, as components:
- **Count tile** — rounded-square (`--radius-tile`), tinted accent background, holds a number (a list's contact count). Represents a *list/event*.
- **Avatar** — round (`--radius-full`), accent-tinted with initials (no raster images). Represents a *person*.

Keep these visually distinct everywhere they co-occur.

### Gradient Hero (mobile — contact detail)

A full-bleed `--gradient-hero` header holding the status bar + back control, with decorative white/clay circles. A white card overlaps upward (≈ −56px) so the round avatar breaches the hero edge (4px white ring). The serif name and role·company sit on the card, not the gradient. Below: "Details" and "Classification" cards. This is the boldest expressive moment in the system — used on exactly one screen.

### Tables (Web Only)

- Header: 11px uppercase, 600 weight, muted color, 2px bottom border
- Rows: 13px, 12-16px padding, 1px bottom border (border-light)
- Hover: bg-hover background
- Name column: 500 weight, ink color (emphasize the person)

### Toasts

| Variant | Background | Text |
|---------|-----------|------|
| Success | `--sage` | White |
| Error | `--error` | White |
| Info | `--ink` | White |

Shadow: Level 3. Border-radius: 8px. Auto-dismiss: 4 seconds. Position: bottom-right (web), top (mobile).

---

## Navigation

### Web Sidebar

**Responsive behavior:**
- **≥1280px (xl):** Expanded — 220px wide, labels and section headers visible
- **<1280px:** Collapsed — 56px wide, icon-only, tooltips on hover, no section labels

#### Expanded (≥1280px)

```
┌─────────────────────┐
│  [E] Exhibitors      │  ← Teal icon, serif brand name
│─────────────────────│
│  MAIN                │  ← 10px uppercase label
│  ● Dashboard         │  ← Active: white text, #2a2a2a bg
│    Lists             │  ← Default: #999 text
│    Contacts          │
│    Emails            │
│                      │
│  SETTINGS            │
│    Profiles          │
│    Settings          │
│─────────────────────│
│  [avatar] Chris L.   │  ← 28px avatar, 12px name
│  Exhibitors.ai       │  ← 10px org name, muted
└─────────────────────┘
```

#### Collapsed (<1280px)

```
┌──────┐
│ [E]  │  ← Teal icon only, no brand text
│──────│
│  ◇   │  ← Icon only, tooltip on hover shows label
│  ●   │  ← Active: white icon, #2a2a2a bg
│  ◇   │
│  ◇   │
│──────│
│  ◇   │
│  ◇   │
│──────│
│ [av] │  ← Avatar only, no name/org text
└──────┘
```

Nav item: 9px 12px padding, 8px radius, hover: #2a2a2a bg + #ccc text.

### Mobile Bottom Tabs

4 tabs maximum: **Home** | **Lists** | **Scan** | **Profile**

- Tab height: 56px (includes safe area)
- Icon: 24px, centered above 10px label
- Active: teal color. Inactive: muted.
- No more than 4 tabs — additional views accessed via stack navigation.

### Marketing Nav (Sticky)

64px height, frosted glass (rgba(250,248,244,0.9) + 16px blur). Serif brand left, sans links right, teal CTA button.

---

## Interaction Patterns

### Navigation: Web ↔ Mobile

| Web | Mobile |
|-----|--------|
| 220px sidebar, always visible | Bottom tab bar (4 tabs) |
| Section labels in sidebar | Stack navigation with back arrow |
| Click to navigate | Tap to navigate, swipe back |

### Data Display: Tables ↔ List Cards

| Web | Mobile |
|-----|--------|
| Full data table with sortable columns | Stacked list cards (name + company + badge) |
| Row hover highlights | Tap to expand detail view |
| Batch selection via checkboxes | Swipe for quick actions (edit, delete) |

### Modals & Overlays

| Web | Mobile |
|-----|--------|
| Centered modal (max 560px) | Full-screen modal for forms |
| Slide-out panel (420px) from right | Bottom sheet (drag to dismiss) for options |
| Click overlay to close | Swipe down to dismiss |

### Hover ↔ Touch

| Web | Mobile |
|-----|--------|
| Hover reveals secondary actions | Visible action buttons always shown |
| Tooltips on hover | Long-press for context menu |
| Cursor pointer for clickable | Haptic feedback on destructive actions |

### Forms

| Property | Web | Mobile |
|----------|-----|--------|
| Input height | 40px | 44px (touch target) |
| Validation | Inline, real-time | On blur (not on keystroke) |
| Keyboard | N/A | Type-appropriate (email, tel, number) |
| Error display | Below field, immediate | Below field, on submit or blur |

### Destructive Actions

Always require confirmation:
- **Web:** Centered modal with "Cancel" (outline) + "Delete" (danger)
- **Mobile:** Bottom sheet with red destructive button + "Cancel"
- **Never** use swipe-to-delete without an undo option

### Loading States

- **Page load:** Skeleton screens (shimmer animation, 1.5s ease infinite)
- **Actions:** Inline spinner in button (replaces text)
- **Multi-step:** Progress bar (import, generation)
- **Never** use a full-page spinner

### Empty States

Every empty view must have:
1. Headline (serif 18px)
2. Description (sans 13px, muted)
3. Primary action button

Tone: warm and encouraging. "Your first list starts here" not "No data found."

### Transitions

| Speed | Duration | Easing | Usage |
|-------|----------|--------|-------|
| Fast | 0.15s | ease | Hover states, toggles, button press |
| Base | 0.2s | ease | Dropdowns, tooltip appear |
| Slow | 0.25s | ease | Slide-out panels, accordion expand |
| Panel | 0.3s | ease | Modal overlays, page transitions |

---

## Platform-Specific Guidelines

### Web App (React + Tailwind)

- Update `tailwind.config.js` with all tokens from this system
- Replace `--bg: #e6e7e9` (cool gray) with `--bg-page: #faf8f4` (warm cream)
- Replace `--brand: #2a6ca4` (blue) with `--primary: #2a9d8f` (teal)
- Sidebar: 220px expanded at ≥1280px (xl), 56px collapsed icon-only below xl. Transition between states with 0.2s ease
- Update all heading sizes to match the type scale (current are too small)
- Add shadow levels to replace generic `shadow-sm`
- Retrofit existing components (Button, SearchInput, tables, modals)

### Mobile App (React Native)

- Create a `theme.ts` file exporting all tokens as a JavaScript object
- Use React Native's `StyleSheet.create` with token references
- Implement a `ThemeProvider` that wraps the app
- Safe area handling: use `react-native-safe-area-context`
- Keyboard avoidance: `KeyboardAvoidingView` with platform-specific behavior
- Gesture handling: `react-native-gesture-handler` for swipe actions
- Font loading: use `expo-font` or `react-native-asset` for Source Serif 4 + Inter
- Touch targets: enforce 44px minimum via style linting or wrapper component

### Marketing Site

- Apply V3 editorial direction from comps
- Hero: 50/50 split layout, serif headlines, warm cream palette
- Feature blocks: 3-column grid with 1px gap, 18px container radius
- Pull quotes: dark background, serif italic, 36px
- CTAs: teal buttons everywhere (consistency with product)
- Product screenshots: real captures in 16px radius frames with shadow level 4

---

## Implementation

### CSS Variables Template

```css
:root {
  /* Colors */
  --primary: #2a9d8f;
  --primary-hover: #249185;
  --primary-light: #e0f3f0;
  --primary-dark: #1e7a6f;
  --clay: #c2783a;
  --clay-light: #f5ece0;
  --sage: #3d9960;
  --sage-light: #e2f2e6;
  --slate: #6882a0;
  --slate-light: #e8edf3;
  --ink: #1a1a1a;
  --ink-secondary: #444444;
  --ink-muted: #777777;
  --ink-subtle: #aaaaaa;
  --bg-page: #faf8f4;
  --bg-warm: #f5efe6;
  --bg-card: #ffffff;
  --bg-hover: #f7f5f1;
  --border: #e0dbd2;
  --border-light: #efece6;
  --nav-bg: #1a1a1a;
  --nav-hover: #2a2a2a;
  --success: #3d9960;
  --warning: #c2783a;
  --error: #c25050;
  --info: #6882a0;

  /* Balanced Blend (v2.1) */
  --teal-row: #e5f1ee;
  --clay-row: #f6efe4;
  --sage-row: #e6f1e9;
  --slate-row: #eaeef4;
  --primary-deep: #144a43;
  --clay-deep: #a85f27;
  --sage-deep: #2f6b45;
  --slate-deep: #4a5e75;
  --bg-field: #efe8dc;
  --bg-group-header: #f2ede4;
  --gradient-header: linear-gradient(165deg, #eaf4f0 0%, #faf8f4 70%);
  --gradient-hero: linear-gradient(150deg, #2a9d8f 0%, #1a6f64 100%);
  --radius-input: 10px;
  --radius-button: 12px;
  --radius-tile: 14px;
  --radius-search: 20px;
  --radius-sheet: 22px;
  --shadow-card: 0 8px 22px rgba(26,26,26,0.1);
  --shadow-fab: 0 6px 16px rgba(42,157,143,0.4);
  --shadow-modal: 0 12px 40px rgba(0,0,0,0.3);

  /* Typography */
  --font-serif: 'Source Serif 4', Georgia, serif;
  --font-sans: 'Inter', system-ui, -apple-system, sans-serif;

  /* Spacing */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 24px;
  --space-6: 32px;
  --space-7: 40px;
  --space-8: 48px;
  --space-9: 64px;
  --space-10: 80px;
  --space-11: 120px;

  /* Radius */
  --radius-xs: 3px;
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 16px;
  --radius-xl: 18px;
  --radius-full: 9999px;

  /* Shadows */
  --shadow-1: 0 1px 3px rgba(0,0,0,0.04);
  --shadow-2: 0 4px 20px rgba(0,0,0,0.06);
  --shadow-3: 0 10px 40px rgba(0,0,0,0.06);
  --shadow-4: 0 20px 60px rgba(0,0,0,0.08);

  /* Transitions */
  --transition-fast: 0.15s ease;
  --transition-base: 0.2s ease;
  --transition-slow: 0.25s ease;
  --transition-panel: 0.3s ease;

  /* Layout */
  --sidebar-width: 220px;
  --content-max-width: 1200px;
}
```

### React Native Theme Object

```typescript
export const theme = {
  colors: {
    primary: '#2a9d8f',
    primaryHover: '#249185',
    primaryLight: '#e0f3f0',
    clay: '#c2783a',
    clayLight: '#f5ece0',
    sage: '#3d9960',
    sageLight: '#e2f2e6',
    slate: '#6882a0',
    slateLight: '#e8edf3',
    ink: '#1a1a1a',
    inkSecondary: '#444444',
    inkMuted: '#777777',
    inkSubtle: '#aaaaaa',
    bgPage: '#faf8f4',
    bgWarm: '#f5efe6',
    bgCard: '#ffffff',
    bgHover: '#f7f5f1',
    border: '#e0dbd2',
    borderLight: '#efece6',
    success: '#3d9960',
    warning: '#c2783a',
    error: '#c25050',
    info: '#6882a0',
    // Balanced Blend (v2.1)
    tealRow: '#e5f1ee',
    clayRow: '#f6efe4',
    sageRow: '#e6f1e9',
    slateRow: '#eaeef4',
    primaryDeep: '#144a43',
    clayDeep: '#a85f27',
    sageDeep: '#2f6b45',
    slateDeep: '#4a5e75',
    bgField: '#efe8dc',
    bgGroupHeader: '#f2ede4',
  },
  // Balanced Blend gradients — consume with expo-linear-gradient / react-native-linear-gradient.
  // Each is [angleDeg, stops]; map to the gradient component's colors/locations/start-end.
  gradients: {
    header: { angle: 165, colors: ['#eaf4f0', '#faf8f4'], locations: [0, 0.7] },
    hero: { angle: 150, colors: ['#2a9d8f', '#1a6f64'], locations: [0, 1] },
  },
  decor: { opacityMin: 0.06, opacityMax: 0.14, teal: '#2a9d8f', clay: '#c2783a', slate: '#6882a0' },
  fonts: {
    serif: 'SourceSerif4',
    sans: 'Inter',
  },
  spacing: {
    xs: 4, sm: 8, md: 12, base: 16,
    lg: 24, xl: 32, '2xl': 40, '3xl': 48,
    '4xl': 64, '5xl': 80, '6xl': 120,
  },
  radius: {
    xs: 3, sm: 4, md: 8, lg: 16, xl: 18, full: 9999,
    // Balanced Blend component radii
    input: 10, button: 12, tile: 14, search: 20, sheet: 22,
  },
  shadows: {
    sm: { shadowOffset: { width: 0, height: 1 }, shadowRadius: 3, shadowOpacity: 0.04, elevation: 1 },
    md: { shadowOffset: { width: 0, height: 4 }, shadowRadius: 20, shadowOpacity: 0.06, elevation: 3 },
    lg: { shadowOffset: { width: 0, height: 10 }, shadowRadius: 40, shadowOpacity: 0.06, elevation: 6 },
    xl: { shadowOffset: { width: 0, height: 20 }, shadowRadius: 60, shadowOpacity: 0.08, elevation: 10 },
    // Balanced Blend component lifts
    card: { shadowColor: '#1a1a1a', shadowOffset: { width: 0, height: 8 }, shadowRadius: 22, shadowOpacity: 0.1, elevation: 6 },
    fab: { shadowColor: '#2a9d8f', shadowOffset: { width: 0, height: 6 }, shadowRadius: 16, shadowOpacity: 0.4, elevation: 8 },
    modal: { shadowColor: '#000000', shadowOffset: { width: 0, height: 12 }, shadowRadius: 40, shadowOpacity: 0.3, elevation: 12 },
  },
  touchTarget: 44,
} as const;
```

---

## Visual Reference

Open `design-system.html` in a browser to see all components rendered live with real colors, typography, and interaction states.

Page comps applying this system:
- `dashboard-v2.html` — Dashboard with bento grid, sidebar, metric cards
- `email-cards-v2.html` — Email cards with left-accent stripe pattern
- `landing-v2.html` — Marketing landing page with editorial hero
- `mobile-screens-v2.html` — Mobile screen comps

**v2.1 (Balanced Blend):** the token/spec layer above is authoritative and is what web (`tokens.css`) and mobile (theme object) consume today. The gallery and page comps above still render the v2.0 look — refreshing them to show tonal rows, two-tone headlines, the gradient hero, and the count-tile/avatar distinction is a follow-up. Until then, the mobile app's `Exhibitors — Balanced Blend` design reference is the visual source for the expressive layer.

# Exhibitors.ai Design System

Cross-platform design language for the Exhibitors.ai web app, React Native mobile app, and marketing site.

## What's here

- **[design-system.md](./design-system.md)** — the full spec: colors, typography, spacing, components, interaction patterns. **This is the source of truth for humans.**
- **[tokens.css](./tokens.css)** — the same tokens as CSS custom properties. **This is the source of truth for machines** (web-side consumers).
- **`*.html`** — interactive visual references. Open in a browser to see components rendered live.
  - `design-system.html` — component gallery
  - `dashboard-v2.html`, `email-cards-v2.html`, `landing-v2.html`, `mobile-screens-v2.html` — page comps

## Consuming from a web project

Install from GitHub:

```sh
bun add github:Exhibitors-AI/DesignSystem
# or: npm install github:Exhibitors-AI/DesignSystem
```

Import once at the top of your root stylesheet:

```css
@import "@exhibitors-ai/design-system/tokens.css";
```

All tokens are now available as CSS variables (`var(--primary)`, `var(--space-4)`, etc.) and can be referenced from Tailwind via `hsl(var(--primary))` / direct `var()` usage.

## Consuming from React Native

Tokens for React Native are documented in [design-system.md § Implementation § React Native Theme Object](./design-system.md#react-native-theme-object). A published RN theme package may follow; for now, copy the theme object into your app's `theme.ts`.

## Updating

The markdown spec is authoritative. When tokens change in `design-system.md`, update `tokens.css` to match in the same commit, then tag a new version. Consumers pull updates with `bun update @exhibitors-ai/design-system`.

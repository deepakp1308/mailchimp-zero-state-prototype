# Mailchimp Marketing Dashboard — Zero-State Prototype

Two concept treatments for the Mailchimp Marketing dashboard zero state, built strictly to the Mailchimp design system.

**Persona**: beauty / skincare SMB · 19 contacts · no campaigns · no store connected.

## Concepts

- **Concept B — Benchmarks-led.** Every empty widget shows the industry median for beauty/skincare SMBs in your revenue band. Benchmarks render in a subtle desaturated teal so they read as reference, not real data. One contextual CTA per card ("Send first campaign →" / "Connect Shopify →").
- **Concept C — Sample-data-led.** Default to a fully populated dashboard with realistic data from a fictional "Aurora Beauty Co." Sample numbers render in muted gray so they unambiguously read as not-yours-yet. Each card has a "Make this real → [specific action]" CTA mapped to the upstream action that would populate it.

## Design system

- Brand yellow `#FFE01B` — sidebar accent only
- Primary CTA / link / active teal `#007C89`
- Chart palette blue `#0070D2` → purple `#A78BFA` → pink `#EC4899` → teal `#00B2A9`
- Industry benchmark line in desaturated teal `#7fb8b9`
- Sample data text in muted gray `#7a8088`, sample chart strokes `#c8ccd1`
- Previous-period dotted red `#D13438`
- Helvetica Neue font stack

## CTA animation

Triple subtle effect on every contextual CTA:
1. **Load shimmer** — left-to-right gradient sweep on first render (1.4s, runs once)
2. **Idle pulse halo** — gentle teal box-shadow that pulses every 6s (CSS `@keyframes`, low opacity)
3. **Hover arrow slide** — `→` translates 4px right on hover

## Live URL

GitHub Pages: https://deepakp1308.github.io/mailchimp-zero-state-prototype/

## Behavioral spine

- **B**: Reciprocity (Cialdini · Regan 1971) · Social proof (Goldstein/Cialdini 2008) · Curiosity gap (Loewenstein 1994). Inspired by Klaviyo Benchmarks and HubSpot inline industry medians.
- **C**: Curiosity gap · IKEA effect (Norton/Mochon/Ariely 2012) · Goal gradient (Hull · Duolingo) · Peak-end on first send (Kahneman 1993). Inspired by Stripe sandbox, Notion templates, Duolingo streaks, ActiveCampaign Smart Start.

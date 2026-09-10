<div align="center">

# Hey, I'm Yotam Faraggi

**Senior Product Engineer turning fuzzy ideas into polished, AI-enabled products people genuinely enjoy using.**

Berlin, Germany · EU citizen · Open to Senior Product & Full-Stack Engineering roles

[Wake My Way](https://github.com/yotamon/WakeMyWay) · [CartShift Studio](https://cart-shift.com/en) · [Portfolio & CV](https://cart-shift.com/en/cv) · [Atlas Irwin](https://atlasirwin.com) · [Say hello](mailto:yotamon@gmail.com)

</div>

---

> I like making complex things feel obvious.

I'm happiest when a messy workflow, a half-formed idea, or a pile of disconnected tools turns into a product that feels clear, calm, and surprisingly easy to use.

I work across the whole product surface: UX, frontend architecture, backend services, data models, AI workflows, integrations, auth, operations, and the unglamorous details that make software dependable in the real world.

| What I'm drawn to | What I tend to own |
| --- | --- |
| AI-native workflows · e-commerce · creative tools · operational products · systems that reduce cognitive load | Product direction · UX decisions · frontend · backend · data · integrations · security · shipping |

## The kind of problems I love

- **Turning complexity into momentum.** I design flows that help people get to the next useful action instead of drowning in options.
- **Connecting the real world to the product.** OAuth, APIs, webhooks, payments, data sync, permissions, and all the edge cases in between.
- **Building AI that belongs in the workflow.** Useful assistance, not a chatbot bolted onto the side.
- **Making systems future-friendly.** Clear boundaries, migrations, observability, sensible defaults, and code a team can keep evolving.

## Things I've built

### [Wake My Way](https://github.com/yotamon/WakeMyWay)
**Local-first conversational Android alarm · Founder dogfood · Public code**

Wake My Way treats waking up as a state transition, not a notification. It starts with a reliability-first native Android alarm, then layers deterministic behavioral guidance, on-device speech, motion evidence, private night-before context, and local learning without letting AI own the critical wake path.

**Why it stands out**
- A Deep Alarm Kernel built around exact alarms, Direct Boot recovery, durable foreground playback, reconciliation, and safe Stop/Snooze behavior
- A pure-Kotlin deterministic Wake Runtime that owns engagement, activation, escalation, capability degradation, and completion
- A production local voice loop using offline Android TTS and on-device speech recognition, with bounded alarm ducking and no transcript persistence
- Physical activation evidence from pickup, orientation change, and sustained movement without persisting raw sensor streams
- Deterministic Wake Learning v0, a private Tomorrow Contract, an Adaptive Dawn Compose design system, and curated Roborazzi visual regression
- Provider-neutral realtime voice experiments isolated from the critical alarm path so experimental AI can fail without breaking wake reliability

`Kotlin` · `Jetpack Compose` · `Android AlarmManager` · `Direct Boot` · `SpeechRecognizer` · `TextToSpeech` · `Roborazzi` · `GitHub Actions` · `TypeScript` · `Vercel`

[Explore the project →](https://github.com/yotamon/WakeMyWay) · [Read the architecture →](https://github.com/yotamon/WakeMyWay#architecture-in-one-picture)

### [CartShift Studio](https://github.com/CartShift/CartShift-Studio)
**Independent e-commerce product studio · Live platform · Public code**

CartShift is the product ecosystem I built around a simple idea: e-commerce teams should not have to jump between a marketing site, scattered emails, audit tools, and delivery workflows just to move a project forward.

It brings the customer journey and the delivery operation into one connected product: a conversion-focused public site, free diagnostics that create a useful first interaction, and a portal where clients and the agency can manage the work together.

**What I built**
- A multilingual Next.js platform spanning a public website and a multi-role agency/client portal
- Consultation, request, client, workboard, and billing workflows in one operational surface
- A free Store Analyzer that evaluates performance, SEO, accessibility, best practices, product pages, cart actionability, structured data, AI readiness, and competitors
- Visual analysis with mobile/desktop screenshots, plus graceful fallbacks when browser-based analysis is unavailable
- A reusable UI system with component variants, motion, RTL support, i18n, validation, optimistic server-state updates, and resilient error handling
- A production architecture using Firebase Auth, Firestore, Storage, Cloud Functions, and Vercel

`TypeScript` · `Next.js 16` · `React` · `Firebase` · `TanStack Query` · `Tailwind` · `Framer Motion` · `Zod` · `Puppeteer` · `Vercel`

[Explore CartShift →](https://cart-shift.com/en) · [View the source →](https://github.com/CartShift/CartShift-Studio)

### [Atlas Irwin](https://github.com/yotamon/Atlas-Irwin)
**Artist website + private release-operations studio · [Live](https://atlasirwin.com) · Public code**

What began as an artist homepage became a full creator-operations product: a public catalog on one side and **Atlas Release Engine** on the other, planning releases, managing media, orchestrating campaigns, tracking performance, and connecting artist platforms.

**Highlights**
- Live Supabase catalog that updates the public player without a redeploy (`revalidateTag`)
- Private Studio: Command Center, release workspaces, campaigns, media library, data health, analytics
- SoundCloud & Spotify OAuth 2.1 with PKCE, private token storage, and intentional reconciliation (no silent catalog invention)
- Security-first: Supabase RLS, studio route guards, CSP/HSTS, rate-limited APIs, Studio `noindex`
- Import/migration tooling that turned legacy release folders into a maintainable product system

`TypeScript` · `Next.js 16` · `React 19` · `Supabase` · `PostgreSQL` · `OAuth 2.1 / PKCE` · `Zod` · `Tailwind 4` · `Vercel`

[Explore the live product →](https://atlasirwin.com) · [Read the README →](https://github.com/yotamon/Atlas-Irwin)

### [Liquid Loom](https://github.com/yotamon/Liquid-Loom)
**Open-source Shopify theme development framework · Public code**

Liquid Loom is a source-first workshop for building Shopify Online Store 2.0 themes without giving up modern frontend ergonomics. Developers organize Liquid and JSON by feature; the framework deterministically maps that source into Shopify's deployment structure while Vite and Tailwind handle the asset pipeline.

**Why it stands out**
- Feature-oriented theme source compiled into a clean, Shopify-ready output directory
- SHA-256 incremental caching, preflight filename-collision detection, atomic manifests, and guarded clean operations
- A merchant-neutral, accessible reference theme spanning home, product, collection, cart, search, page, and 404 surfaces
- A complete quality gate: 15 tests, 96%+ line coverage, Prettier, clean builds, Shopify Theme Check, and a public-readiness scan
- Open-source maintenance built in with CI, Dependabot, issue forms, contribution guidance, security reporting, and a protected main branch

`JavaScript` · `Shopify Liquid` · `Online Store 2.0` · `Vite 8` · `Tailwind CSS 4` · `PostCSS` · `Node.js` · `pnpm`

[Explore the framework →](https://github.com/yotamon/Liquid-Loom) · [Read the architecture →](https://github.com/yotamon/Liquid-Loom#the-build-in-one-picture)

### StarLinker
**Private SaaS · A visual workspace for people who think in maps, not endless lists**

StarLinker turns goals, tasks, notes, habits, and relationships into an interactive visual system. The product is designed around spatial context: seeing what matters, what connects, and what to do next.

**What makes it interesting**
- Real-time collaboration, role-based access, offline-aware sync, and shareable workspaces
- Rich graph interactions: keyboard-first flows, templates, undo/redo, and connected entities
- AI-assisted planning, task breakdown, graph-aware recommendations, and MCP access
- Subscription billing, account lifecycle, audit logs, admin workflows, and monitoring
- Web, PWA, and Capacitor mobile surfaces

`TypeScript` · `Next.js` · `PostgreSQL` · `Drizzle` · `Supabase` · `Replicache` · `React Flow` · `Vercel AI SDK` · `Stripe` · `Sentry` · `Playwright`

The source is private, but I'm always happy to talk through the architecture, trade-offs, and the product decisions behind it.

## My working toolkit

| Build | Connect | Ship |
| --- | --- | --- |
| TypeScript · React · Next.js · Kotlin · Jetpack Compose · Tailwind · React Query · Zustand | PostgreSQL · Firebase · Supabase · Drizzle · Prisma · REST APIs · OAuth 2.1 / PKCE · Stripe · LLM APIs · MCP | Vercel · Docker · Playwright · Jest · Android instrumentation · GitHub Actions · Sentry · analytics · security headers |

## A little more human

I'm a builder, a music maker, and someone who notices when a product has too many steps.

Outside of software, I create electronic music and build creative tools around it. It keeps me close to the kind of user experience I care most about: expressive enough to feel inspiring, structured enough to be useful.

---

### Let's build something people want to come back to.

Start with [Wake My Way](https://github.com/yotamon/WakeMyWay), explore [CartShift Studio](https://cart-shift.com/en), browse my [portfolio & CV](https://cart-shift.com/en/cv), or [email me](mailto:yotamon@gmail.com).

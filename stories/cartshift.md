# CartShift Studio — building the system around the client journey

[Source](https://github.com/CartShift/CartShift-Studio) · [Live website](https://cart-shift.com/en) · [Back to my profile](../README.md)

## The problem
A commerce studio needs to attract suitable clients, discover store issues, coordinate work and retain a record of requests, billing and delivery. Those activities are usually scattered across a marketing site and disconnected operational tools.

## My scope
I built and operate the platform as a full-stack product: multilingual public website (English/Hebrew with RTL), diagnostics, and multi-role agency/client workspace. It uses Next.js/React/TypeScript with Firebase Auth, Firestore, Storage and Functions and a Vercel deployment surface. Product decisions, UX, domain workflows, integration boundaries, security rules and release work are visible in the repository.

## Engineering decisions worth discussing
- **Keep lead acquisition and delivery connected:** the free store review/analyzer creates a useful entry point to the agency workflow. This is an architecture/product design decision, **not** a claim that acquisition is already proven.
- **Authorization belongs to every operation:** agency/client roles, account boundaries and Firebase security rules matter more than hiding buttons in the UI.
- **Internationalization is structural:** localized routes, validation, accessible form behavior and RTL are part of the functional product, not a final translation pass.
- **Failures should be observable and recoverable:** production fixes, CI and tests are tracked explicitly, including known CV PDF rendering and PWA/locale issues.

## What evidence exists
- Public source and a live marketing website.
- Technical documentation, CI and issue/PR records.
- [CV rendering issue](https://github.com/CartShift/CartShift-Studio/issues/103) and [mitigating implementation](https://github.com/CartShift/CartShift-Studio/pull/104).
- [Review funnel verification gate](https://github.com/CartShift/CartShift-Studio/issues/95) and [permission-backed case study requirement](https://github.com/CartShift/CartShift-Studio/issues/96).

## What I will not overclaim
The existence of a production deployment or a completed feature does **not** demonstrate end-to-end lead conversion, a specific revenue lift, or production reliability across all flows. Real client metrics require consent, attribution and evidence.

## Next proof to collect
1. Confirm CV/locale/asset flows on production after releases; inspect actual results.
2. Run one approved internal review-funnel test with durable event evidence.
3. Publish two permission-backed customer cases with a before/after workflow or measured outcome.
4. Show a short portal walkthrough using safe synthetic data.

**Interview discussion:** designing coherent user journeys across website, diagnostics and operational SaaS while handling authentication, localization, errors and live operations.

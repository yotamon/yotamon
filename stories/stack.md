# STACK

**A tactile card game, engineered for digital multiplayer.**

STACK is a personal product-engineering project that takes an original 54-card tabletop game and builds it into a browser experience for friends, families and remote players. It combines a physical deck, a responsive card table, bots, and private rooms with real-time interactions.

**Role:** product design, game mechanics, full-stack engineering, interactive UI, testing and infrastructure.

## What makes it interesting

### The experience

The digital table needs to feel understandable in the same way physical cards do. Players see the pile change, learn what BURN or DUMP actually did, and can react quickly with SNAP or SLAM. The UX has to work on a narrow phone screen without misrepresenting hidden cards or delaying the next player.

### The engineering

- **Canonical deterministic game engine** in JavaScript, with move validation, bots and seeded simulations for edge cases.
- **Server-authoritative multiplayer** using Node.js and Neon PostgreSQL, with room revisions to handle competing actions.
- **Authenticated WebSockets** for live room updates and reactions, plus HTTP fallback and reconnect behavior.
- **Two frontends:** a tactile vanilla JS/CSS Classic tabletop and a React 19 / Next.js 16 / TypeScript tabletop.
- **One deployment:** both frontends statically served by a Node 24 service on Render, with the same-origin room API.
- **Quality safeguards:** rule, privacy, state-concurrency, UX and browser integration tests in CI.

## The interesting trade-off

**Game logic must win over animation.** A player cannot gain or lose a turn because an animation is slow. The rules engine and server decide what happened; the UI renders that committed outcome. This also prevents effects from accidentally exposing another player's hidden cards.

The project has taught me a lot about state consistency, interactive systems, progressive modernisation of an existing product, and the difference between automated tests and true user acceptance.

## Current status

Actively developed playtest product. Automated tests and simulated game balance are useful, but real-device visual QA and hosted two-device sessions are separate release checks.

[Gameplay preview on Render](https://stack-card-game-t7vx.onrender.com/stack) · [Classic tabletop](https://stack-card-game-t7vx.onrender.com/pilehead/index.html)

*These are the project's configured demo URLs. The hosted service may sleep or temporarily be unavailable. The source repository is still private while its publication and asset-rights checks are completed.*

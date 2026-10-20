# Wake My Way — reliability before AI

[Source](https://github.com/yotamon/WakeMyWay) · [Architecture](https://github.com/yotamon/WakeMyWay#architecture-in-one-picture) · [Back to my profile](../README.md)

## The problem
An alarm is a safety-of-experience product: the user must be woken even if network, audio intelligence, the UI, microphone permission or cloud services fail. A conversational assistant can make waking more useful, but it cannot become a single point of failure.

## Architectural decision
Separate **critical alarm delivery** from **behavioral and conversational guidance**.

- The Android Alarm Kernel uses exact scheduling, a persisted wake snapshot, receiver/service execution, recovery and Stop/Snooze semantics.
- A pure Kotlin WakeRuntime consumes typed facts and emits typed behavioral directives.
- Voice and AI adapters are downstream collaborators; they do not get authority over alarm delivery or wake completion.
- Motion and voice provide bounded evidence, never certainty about a person's consciousness.

This boundary trades some flexibility for a predictable failure model.

## What the repository demonstrates
Native Kotlin/Jetpack Compose, Android background and Direct Boot constraints, deterministic state-machine design, audio lifecycle, no-raw-transcript persistence, instrumentation/testing and visual regression practices.

## Release truth
- The product is in **founder dogfood**, not a certified public release.
- The critical Android path and behavioral runtime are implemented according to the repository status/README.
- Direct Realtime is used for the optional conversational layer; local TTS/STT remains available for diagnostic or preview use but is **not** a universal consumer fallback.
- GPT-Live is a **gated migration**; [Issue #194](https://github.com/yotamon/WakeMyWay/issues/194) requires full-duplex audio coordination, Android physical-device validation, cost and UX evidence before rollout.
- [Physical reliability gate #9](https://github.com/yotamon/WakeMyWay/issues/9) remains open.

## What remains to prove
1. Seven or more recorded physical mornings spanning locked screen, Doze, Bluetooth/audio route changes and process lifecycle.
2. Clear failure mode evidence: what happens if speech is unavailable or an AI session disconnects.
3. Perceived voice naturalness plus p50/p95 startup latency and actual session cost.
4. Accessibility and multilingual acceptance on real devices.

No claim of measured 99.9% alarm success or launched audience is made.

**Interview discussion:** platform lifecycle, critical-path isolation, deterministic decision authority, observable failure modes, graceful degradation and responsible AI integration.

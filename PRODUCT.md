# Product

<!-- impeccable:product-schema 1 -->

> Recorded during `/impeccable init` on 2026-11-14. The interview went unanswered ("no preference" on
> every question), so the product, users and stack below are inferred from the repository and marked
> **(assumed)**. Confirm or correct them before they steer design work.

## Platform

web

## Stack

delegated: static HTML/CSS, no build step **(assumed)**. Chosen because the repository has no app or
framework and Taste Skill's own kit (`skills/taste-skill/assets/starter.html`, `system.css`,
`system.js`) is static HTML/CSS. Revisit if a surface needs routing or a CMS.

## Users

**(assumed)** Developers who use coding agents (Claude Code, Codex, Antigravity) to build websites,
and who want a professional company site instead of a generic, templated or "AI-made" landing page.
They install the skill, ask their agent for a site, and judge the result by how it looks in a
browser. Secondary readers: contributors and sponsors of the open-source project.

## Product Purpose

Taste Skill (`design-taste-frontend`, tasteskill 2.5.1) is an Agent Skill that makes coding agents
build company websites at the figma.com and x.ai bar. Success is a page that says plainly what is
sold, shows the real thing on every screen, looks made for that client, and passes the skill's own
real-browser checker and finish gate.

This repository is a fork of `Leonxlnx/taste-skill`. Whether the fork will diverge from upstream is
undecided.

## Positioning

Its rules are enforced, not just suggested: Node scripts deal palettes, type, layouts, photographs
and moments by the client's trade, and a checker (`scripts/consistency.mjs`) plus a finish gate
(`scripts/gate.mjs`, also a Claude Code Stop hook) render the page in headless Chrome at 1440, 1024,
768, 390 and 320 and block the finish until no fixable FAIL is left.

## Operating Context

- Installed with `npx skills add`, as a Claude Code or Codex plugin, or symlinked via `install.sh`.
- Runs inside the user's agent session; needs Node 22+ and Chrome, Edge or Chromium; ffmpeg optional.
- Installs nothing, needs no API keys; bundled Wikimedia Commons photographs work offline.
- Builds in the target project's own stack (static, React, Vue, Svelte, Astro, Tailwind; Next.js as a
  static export).

## Capabilities and Constraints

- Classifies the business as `software`, `gaming`, `tech`, `product`, `service` or `place`.
- One section per screen at 1440x900, equal content edges, fixed nav, single-screen closing footer.
- Shader effects, scroll scenes and 3D only on `software`, `tech` and `gaming` pages, within a
  four-context WebGL cap with phone and reduced-motion fallbacks.
- Every page gets a hero entrance and one or two dealt moments.
- Licensed stand-in photographs only, credited in one footer line, never passed off as the client's.
- Terminology to keep: "deal", "moment", "finish gate", "checker", "trade", "kind".
- MIT licensed.

## Brand Commitments

- Name: **Taste Skill**; version string `tasteskill 2.5.1`; skill install name `design-taste-frontend`.
- Wordmark assets: `assets/taste-skill-wordmark.png`, `assets/taste-skill-wordmark-dark.png`.
- Sibling product: TasteCode (desktop app, tastecode.dev). Website: tasteskill.dev.
- Voice in the docs: plain, factual, specific; no hype.

## Evidence on Hand

- Example builds: `examples/v2/*.webp`, with photo credits in `examples/v2/CREDITS.md`.
- Launch film: GitHub release `v2.0.0` of the upstream repository.
- Sponsors and supporters listed in `README.md`, logos in `assets/sponsors/`.
- Changelog with measured results (for example, the 44-site test behind 2.5.1) in `CHANGELOG.md`.
- Absent: user testimonials, usage numbers, download counts, pricing. Do not invent them.

## Product Principles

1. Enforce, don't advise: every rule a page must meet is checked in a real browser.
2. Show the real thing: real product UI, real photographs, real facts; never fabricate.
3. Fit the trade: palettes, photographs and effects follow what the client actually sells.
4. Plain words: copy says what is sold, in a voice of its own.

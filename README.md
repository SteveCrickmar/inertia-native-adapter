# inertia-native-adapter

> Framework-agnostic npm adapter (core) + React & Vue bindings for Inertia Native: visit interception, screen page-cache & restore, lifecycle reporting, bridge transport.

📋 **Part of the [Inertia Native](https://github.com/users/SteveCrickmar/projects/4) project** — an open-source toolkit for shipping native iOS & Android apps powered by an existing Laravel + Inertia.js application, modelled on (but not depending on) Hotwire Native. Track the cross-repo roadmap on the **[project board](https://github.com/users/SteveCrickmar/projects/4)**.

### Repositories in the Inertia Native project
- **[inp-protocol](https://github.com/SteveCrickmar/inp-protocol)** — spec, JSON Schemas, conformance fixtures, ADRs, and the M0 spike. Coordination point for all Inertia Native repos
- **inertia-native-adapter** ⬅ _this repo_
- **[inertia-native-ios](https://github.com/SteveCrickmar/inertia-native-ios)** — Navigator, shared WKWebView + snapshot cache, path configuration, bridge components, native error/auth/recovery. Models Hotwire Native iOS; zero Turbo dependency
- **[inertia-native-android](https://github.com/SteveCrickmar/inertia-native-android)** — single shared WebView across fragment destinations, AndroidX Navigation, path config, bridge components
- **[inertia-native-laravel](https://github.com/SteveCrickmar/inertia-native-laravel)** — native detection & macros, shared props, signal routes & helpers, path-config authoring/serving, scaffolding & test helpers
- **[inertia-native-demo](https://github.com/SteveCrickmar/inertia-native-demo)** — one Laravel 12 app with switchable React & Vue front ends exercising every feature; error-injection harness; doubles as docs example and UI-test target
- **[inertia-native-docs](https://github.com/SteveCrickmar/inertia-native-docs)** — quick start, navigation, path configuration, signals, bridge components, native screens, auth, protocol reference

## Project documents
- [PRD](https://github.com/SteveCrickmar/inp-protocol/blob/main/docs/01-prd-inertia-native.md)
- [Technical Specification](https://github.com/SteveCrickmar/inp-protocol/blob/main/docs/02-technical-spec-inertia-native.md) (normative)
- [Task Breakdown](https://github.com/SteveCrickmar/inp-protocol/blob/main/docs/03-task-breakdown.md)

## Toolchain baseline (OC-8)
Node 20 LTS, TypeScript 5.x, Vitest, ESLint+Prettier, Changesets. npm workspaces: `packages/core`, `packages/react`, `packages/vue`, `packages/conformance`.

## Working conventions
- **OC-1:** one task → one branch (`task/<ID>-slug`) → one PR; no task touches more than one repo.
- **OC-3:** the [protocol spec](https://github.com/SteveCrickmar/inp-protocol) is law. Conformance fixtures are vendored read-only at the ref in `INP_SPEC_REF`.
- See the [task breakdown](https://github.com/SteveCrickmar/inp-protocol/blob/main/docs/03-task-breakdown.md) §0 for the full operating conventions and Definition of Done (OC-2).

## Tasks tracked in this repo
- **A2.1** — Repo scaffold
- **A2.10** — Bridge core
- **A2.11** — React bindings
- **A2.12** — Vue bindings
- **A2.13** — Conformance runner
- **A2.14** — Web no-op hardening & bundle budget
- **A2.2** — Detection & handshake module
- **A2.3** — Message codec & transports
- **A2.4** — Visit interception engine
- **A2.5** — Screen page-cache & PageRenderer
- **A2.6** — History discipline module
- **A2.7** — Lifecycle reporting
- **A2.8** — Signal detection & emission
- **A2.9** — 409 version flow & error funnel
- **R6.2-web** — Reference bridge components (web + iOS) (web halves)

## Status
Pre-alpha. Names are placeholders pending a trademark check (OC-6). Licensed MIT (proposed).

# Monorepo Starter (Expo + Node)

A pnpm + Turborepo monorepo starter for a cross-platform Expo app and a TypeScript Express backend.

<!-- screenshot here: mobile app running alongside backend -->

## What's inside

```
apps/
  my-app/    Expo SDK 54 · React Native 0.81 · React 19 · Expo Router 6 (tabs + modal)
             NativeWind v4 · Zustand store (store/useStore.ts) · Reanimated 4
  backend/   Express 4 + TypeScript, run with tsx in dev and compiled with tsc
packages/    shared packages go here (in pnpm-workspace.yaml, empty for now)
```

Turborepo runs the `dev`, `build` and `test` tasks across the workspace (`turbo.json`).

## Getting started

Requirements: Node.js and pnpm.

```bash
pnpm install
pnpm dev            # runs every app's dev task (Turbo TUI)
pnpm dev:mobile     # Expo app only
pnpm dev:backend    # API only, on http://localhost:3000 (or $PORT)
pnpm build
```

The backend exposes `GET /`, which returns `{ "message": "Backend API is running" }`.

## Roadmap / TODO

<!-- e.g. shared types package, API client in packages/, tests, CI -->

- [ ] Add a shared `packages/` example (such as types shared by the app and the API)
- [ ] Add tests and CI

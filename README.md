# Autonomous ASIC DRC Platform

A research prototype for parsing ASIC layout data, running technology-aware design-rule checks, visualizing constraint relationships, and evaluating bounded autonomous repair actions.

## Included packages

- `artifacts/asic-drc-platform` — Vite + React web interface
- `artifacts/api-server` — Express API and DRC/repair engine
- `lib/api-client-react` — generated React API client
- `lib/api-spec` — OpenAPI contract
- `lib/api-zod` — shared request/response schemas
- `lib/db` — shared database package scaffold

## Run locally

Requirements: Node.js 20+ and pnpm.

```bash
pnpm install
pnpm --filter @workspace/api-server run dev
# In another terminal
pnpm --filter @workspace/asic-drc-platform run dev
```

The web interface runs on the Vite port and expects the API under `/api`.

## Validate

```bash
pnpm run typecheck
pnpm run build
```

The DRC engine is a research prototype and is not commercial foundry signoff software.
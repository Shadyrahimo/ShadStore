# SRDev

Multi-tenant digital goods store platform. One codebase, many stores.

## Structure

- `artifacts/api-server` — Express 5 + Drizzle ORM backend
- `artifacts/srdev-admin` — Admin control panel
- `artifacts/srdev-store` — Customer-facing storefront
- `artifacts/mockup-sandbox` — UI sandbox
- `lib/db` — Database schema (Drizzle + PostgreSQL)
- `lib/api-spec` — OpenAPI specification + Orval config
- `lib/api-zod` — Generated Zod schemas
- `lib/api-client-react` — Generated React Query hooks
- `packages/deposit-ui` — Shared deposit UI components
- `scripts` — Build and maintenance scripts

## Stack

- **Monorepo**: pnpm workspaces
- **Runtime**: Node.js >= 20
- **Language**: TypeScript 5.9
- **Backend**: Express 5 + PostgreSQL + Drizzle ORM
- **Frontend**: React 19 + Vite + TailwindCSS
- **Validation**: Zod + Drizzle-Zod
- **API codegen**: Orval

## Commands

- `pnpm run build` — build all workspaces
- `pnpm run typecheck` — typecheck all workspaces
- `pnpm --filter @workspace/api-server run dev` — run backend locally
- `pnpm --filter @workspace/srdev-store run dev` — run storefront locally
- `pnpm --filter @workspace/srdev-admin run dev` — run admin panel locally

# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.

## Artifacts

### The Untold Trails (`artifacts/untold-trails`)

- **Kind**: React + Vite web app (frontend-only, no backend needed)
- **Preview path**: `/`
- **Description**: Premium adventure travel website focused on hidden gems, offbeat treks, and unique Himalayan experiences
- **Stack**: React, Vite, Tailwind CSS, framer-motion, wouter, react-hook-form, zod, lucide-react
- **Pages**:
  - `/` — Homepage with hero, featured treks, Trek Suggestion Tool, hidden gems teaser, blog teaser, about, contact
  - `/treks` — Trek Explorer listing all 4 main treks (ABC, EBC, Panch Kedar, Kashmir Lakes)
  - `/treks/abc` — Annapurna Base Camp detailed trek page
  - `/treks/ebc` — Everest Base Camp detailed trek page
  - `/treks/panch-kedar` — Panch Kedar detailed trek page
  - `/treks/kashmir-lakes` — Kashmir Great Lakes detailed trek page
  - `/hidden-gems` — Lesser-known treks showcase grid
  - `/blog` — Travel stories and guides (The Journal)
  - `/about` — Brand story of The Untold Trails
- **Design**: Dark earthy cinematic theme, Playfair Display + DM Sans fonts, amber/burnt sienna accents, framer-motion scroll animations
- **Features**: Interactive Trek Suggestion Tool (filter by budget/difficulty/duration), contact form with validation, glassmorphic sticky navbar, AI-generated images throughout

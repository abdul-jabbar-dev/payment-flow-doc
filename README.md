# Payment Follow-up SaaS

> **Get Paid Faster Without Chasing Clients.**

A Payment Collection Command Center for freelancers, consultants, agencies, and small businesses.

## What This Is

This is not a generic invoice management system. It is a payment collection command center that answers three questions every time you open it:

1. **How much money am I waiting for?**
2. **Who owes me?**
3. **What should I do next?**

## Stack

- **Frontend:** Next.js (App Router) + TypeScript + Tailwind CSS + shadcn/ui
- **Server State:** TanStack Query
- **Forms:** React Hook Form + Zod
- **Charts:** Recharts
- **Backend (coming):** Express.js (`apps/api`)
- **Monorepo:** pnpm workspaces + Turborepo

## Project Structure

```
payment-follow-up/
├── apps/
│   ├── web/        # Next.js frontend
│   └── api/        # Express.js backend (future)
├── packages/
│   ├── shared/     # Shared types and utilities
│   └── typescript-config/
├── package.json
├── pnpm-workspace.yaml
└── turbo.json
```

## Getting Started

```bash
# Install dependencies
pnpm install

# Start development
pnpm dev

# Build
pnpm build

# Lint
pnpm lint

# Type check
pnpm typecheck

# Unit tests
pnpm test

# E2E tests
pnpm test:e2e
```

## MVP Scope

The first sellable version includes:

- Landing page + Pricing
- Authentication (Login / Register)
- Dashboard — outstanding, overdue, due soon, today's actions
- Customer management
- Invoice creation, sending, tracking
- Public invoice page for clients
- Payment recording (full + partial)
- Reminder system
- Collection Center — priority queue

## Development Phases

| Phase | Scope | Status |
|---|---|---|
| 1 | Foundation — monorepo, scaffold, tooling | ✅ |
| 2 | Marketing + Auth + Shell | 🔄 |
| 3 | Dashboard + Customers + Invoices | 🔄 |
| 4 | Payments + Reminders + Collection | 🔄 |
| 🚀 | **First Sellable Version** | — |
| 5 | Analytics + Notifications + Billing | — |
| 6 | AI Follow-up + Payment Intelligence | — |
| 7 | Production hardening | — |
"# payment-flow-doc" 

# Project Architecture Rules

Project:

Payment Follow-up SaaS

Architecture:

Monorepo

apps/api
→ Node.js + Express + TypeScript + MongoDB/Mongoose

apps/web
→ Next.js + TypeScript + Tailwind + shadcn/ui + TanStack Query

## Backend Layering

Route
→ Middleware
→ Controller
→ Service
→ Repository
→ Database

Controllers must remain thin.

Business logic belongs in services.

Database access belongs in repositories.

## Identity Architecture

User
→ Membership
→ Tenant
→ Role

Authentication, authorization, and tenant isolation are separate concerns.

## Tenant Isolation

Every tenant-owned database query must be tenant scoped.

Never trust tenantId directly from client input.

Tenant context must be derived from:

authenticated user
+
verified membership.

## Business Flow

Customer
→ Invoice
→ Payment
→ Reminder
→ Collection

Do not bypass domain boundaries.

## Source of Truth

Database is authoritative for persistent application state.

Frontend state is not authoritative.

Client-provided values must be validated server-side.

## Architecture Preservation

Before changing architecture:

- inspect current implementation
- identify dependency impact
- identify migration requirements
- identify backward compatibility concerns

Prefer incremental evolution over rewrites.
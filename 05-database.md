# Database Safety Rules

MongoDB is the persistent source of truth.

## Never Destructively Modify Data

Never execute:

dropDatabase
drop collection
deleteMany without explicit scope
mass update without verification
database reset

without explicit confirmation.

## Schema Changes

Before changing a model:

1. Inspect existing documents.
2. Check indexes.
3. Check existing queries.
4. Check services/controllers using the field.
5. Consider backward compatibility.
6. Determine whether migration is required.

## Tenant-Owned Data

Tenant-owned models must contain:

tenantId

and queries must scope by tenantId.

## Financial Data

Invoices and payments are sensitive financial records.

Never silently delete or overwrite financial history.

Prefer immutable records / state transitions where appropriate.

## Calculations

Financial calculations must be performed server-side.

Never trust frontend totals.

## Indexes

Before adding an index:

inspect existing indexes.

Avoid duplicate or unnecessary indexes.
# Verification Rules

No feature is complete until verified.

## After Backend Changes

Run appropriate:

- typecheck
- lint
- unit tests
- integration tests
- build

## After Frontend Changes

Run appropriate:

- typecheck
- lint
- tests
- build

## Security-sensitive Changes

Also test:

- authentication
- authorization
- tenant isolation
- invalid input
- unauthorized access
- cross-tenant access
- token/session behavior

## Before Reporting Success

Check actual command output.

Never infer success.

## Regression Protection

Before modifying an existing feature:

identify relevant tests.

After modification:

rerun them.

## Failure Handling

If tests fail:

do not hide the failure.

Report:

- command
- failure
- root cause if known
- affected files
- proposed fix
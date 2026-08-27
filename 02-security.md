# Security Rules

Security is a mandatory requirement.

Never weaken security for convenience.

## Authentication

Use:

- Argon2id for passwords
- short-lived access JWT
- HttpOnly refresh cookie
- refresh token rotation
- refresh token reuse detection

Never:

- store plaintext passwords
- log passwords
- return password hashes
- store refresh tokens in localStorage
- expose refresh tokens to frontend JavaScript

## Authorization

Authentication:
Who is the user?

Authorization:
What can the user do?

Tenant isolation:
Which tenant data can the user access?

Never merge these responsibilities incorrectly.

## RBAC

Roles:

OWNER
ADMIN
MEMBER
VIEWER

Role is determined by Membership.

Never trust role supplied by the client.

## Cross Tenant Protection

Every tenant resource must be queried with:

tenantId
+
resource identifier

Never fetch tenant-owned resources by resource ID alone.

## Sensitive Logging

Never log:

password
JWT
refresh token
token hash
API key
secret
cookie value

## Security Changes

Before changing authentication, authorization, sessions, or tenant isolation:

inspect existing implementation and tests first.

Never simplify security logic without explicit justification.
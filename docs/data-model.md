# Data model

This document records the current model and its intent. The Prisma contract at [`src/prisma/contract.prisma`](../src/prisma/contract.prisma) is the structural source of truth.

## Current scope: staff users

There is one model today: `User`. These are internal support staff, not customers. Customers who contact support through WhatsApp or email will be modeled separately if and when that scope is added.

| Field | Meaning |
| --- | --- |
| `id` | Client-generated CUID v2 identifier |
| `name` | Staff member's display name |
| `email` | Unique email address; intended login identifier |
| `passwordHash` | Password hash, never a plaintext password |
| `role` | One of `AGENT`, `LEAD`, or `MANAGER`; defaults to `AGENT` |
| `createdAt` | Creation timestamp |
| `updatedAt` | Last-update timestamp |

## Role intent

- **AGENT** — handles customer-support conversations.
- **LEAD** — leads agents; likely handles escalations and team oversight.
- **MANAGER** — oversees leads and broader support operations.

These descriptions express the intended organizational levels. Exact permissions and visibility rules have not been designed yet. The current schema does **not** store a reporting line (for example, a `managerId`), so it cannot yet represent which lead manages which agents.

## Deferred modeling decisions

- Whether to represent reporting relationships with a self-relation, teams, or both.
- Whether role permissions are fixed in application logic or configurable.
- Customer/contact identity and linking a person across WhatsApp and email.
- Tickets and channel-specific message threads.
- Audit/activity history and the events needed for KPI calculations.

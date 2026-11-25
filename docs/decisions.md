# Decision log

Short project decisions and their rationale. Update this when a decision materially changes.

## 2026-11-25 — Limit the initial data-model scope to staff users

- The first model is `User`; tickets, customers, and messages are deferred.
- This keeps the first database iteration focused while the user model and database workflow are established.

## 2026-11-25 — Use AGENT, LEAD, and MANAGER as staff role names

- These names express the intended support-team progression.
- Permission rules and specific reporting relationships are not part of the model yet; role labels alone do not encode an org chart.

## 2026-11-25 — Keep external customers separate from staff users

- Planned support conversations arrive through WhatsApp and email.
- External customers are not staff accounts and should not be represented by the staff `User` role enum. Their identity model is deferred until customer/conversation scope begins.

## 2026-11-25 — Use Prisma ORM 8 contract-based schema authoring

- Author the data model in `src/prisma/contract.prisma` and emit generated contract artifacts with `prisma contract emit`.
- Do not hand-edit generated contract files.

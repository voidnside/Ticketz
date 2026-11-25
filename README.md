# Ticketz

Ticketz is a portfolio project exploring a customer-support workflow and KPI tracking. The planned support conversations will come from WhatsApp and email; the current implementation scope is **staff users only**.

## Current status

- Next.js app scaffolded
- Prisma ORM 8 PostgreSQL contract initialized
- User roles: `AGENT`, `LEAD`, and `MANAGER`
- Database schema and migrations are still being developed

## Tech stack

- Next.js 16, React 19, TypeScript
- PostgreSQL (Neon for development)
- Prisma ORM 8 contract-based schema
- Tailwind CSS 4

## Getting started

Install dependencies:

```bash
npm install
```

Create a `.env` file in the project root and set the PostgreSQL connection string:

```env
DATABASE_URL="your-postgresql-connection-string"
```

Keep `.env` private and do not commit database credentials. Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

The Prisma contract source is [`src/prisma/contract.prisma`](src/prisma/contract.prisma). Edit that source, then emit the generated contract with:

```bash
npm run contract:emit
```

Generated contract artifacts in `src/prisma/` are outputs; edit the `.prisma` source rather than generated files.

## Project notes

- [Data model](docs/data-model.md) — current user model and role decisions
- [KPI definitions](docs/kpi-definitions.md) — planned metrics and open definition questions
- [Decision log](docs/decisions.md) — scope and architecture decisions

Ticket, customer/contact, and message models are intentionally out of the current scope. KPI implementation will follow once those concepts and their lifecycle are designed.

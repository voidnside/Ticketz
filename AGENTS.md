<!-- BEGIN:nextjs-agent-rules -->

## This is NOT the Next.js you know

This version has breaking changes — APIs, conventions, and file structure may all differ from your training data. Read the relevant guide in `node_modules/next/dist/docs/` (resolved from this file's directory; in monorepos the `next` package may not be visible from the repo root) before writing any code. Heed deprecation notices.

This block is written and re-added by `next dev` — verify at `node_modules/next/dist/server/lib/generate-agent-files.js`. Removing it from a diff only re-creates the uncommitted change; committing it with your work keeps the tree clean.

<!-- END:nextjs-agent-rules -->

## Commit strategy

- Use Conventional Commits: `type: concise imperative summary` (for example, `feat: add staff user model` or `docs: document user roles`). Use `feat`, `fix`, `docs`, `refactor`, `test`, or `chore` as appropriate; a scope is optional.
- Make each commit one coherent, reviewable change. Keep unrelated features, formatting, and generated-file churn in separate commits.
- Before committing, run the relevant checks for the change and review the staged diff.
- Never commit secrets, `.env` files, or local database credentials.
- Do not create commits unless the user explicitly asks for a commit.

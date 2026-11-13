# Contributing to NadCo repositories

These rules apply to every repository in the organization.

## Repository naming

- Lowercase, words separated by hyphens: `<brand>-<role>`
- Examples: `nadstore-<client-name>`, `famo-panel`, `nadcloud-media`, `template-nextjs-frontend`
- Every repository has a one-line description and at least one topic.
- New repositories are **private** by default.

## Branches

- `main` is protected. Never push to it directly.
- Create a branch for every change: `<type>/<short-description>`
- Examples: `feat/coupon-field`, `fix/order-total-rounding`, `docs/update-readme`

## Commits and PR titles

Format: `type(scope): short description`

| Type | Use for |
|---|---|
| `feat` | A new feature |
| `fix` | A bug fix |
| `docs` | Documentation only |
| `refactor` | Code change with no behavior change |
| `test` | Adding or fixing tests |
| `chore` | Tooling, dependencies, configuration |

Rules:
- Imperative mood: "add coupon field", not "added" or "adds".
- Lowercase, no trailing period, under 72 characters.
- Scope is optional: the area of the code (`cart`, `auth`, `deploy`).

Examples:
```
feat(cart): add coupon field
fix(checkout): round order total to nearest toman
docs: add deployment section to README
```

## Pull requests

1. Open a PR from your branch into `main`. Fill in the PR template.
2. The PR title must follow the commit format above.
3. Review your own diff before merging.
4. Merge with **Squash and merge**. The PR title becomes the commit message.
5. Delete the branch after merging.

## README minimum

Every repository README must include:
- What the project is
- How to set it up and run it locally
- Required environment variables (documented in `.env.example`)
- How to deploy it

## Secrets

- Never commit `.env` files, passwords, API keys, or tokens.
- Commit a `.env.example` with placeholder values only.
- If a secret is committed by mistake, rotate it immediately. Deleting the commit is not enough.

## Time tracking

All work is logged in the timer, under the matching project. Infrastructure and setup work is logged separately from client work.

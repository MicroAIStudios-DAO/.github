# Contributing

Thank you for improving MicroAI Studios DAO projects.

## Before opening a change

1. Read the target repository's README, `AGENTS.md` (when present), and architecture notes.
2. Open or reference an issue for behavior changes, security-sensitive work, or cross-repository contracts.
3. Keep the change focused. Separate cleanup from functional behavior.
4. Never commit credentials, personal data, production exports, or unredacted logs.

## Pull-request standard

Every pull request must explain:

- the problem and root cause;
- the chosen approach and meaningful alternatives;
- user, developer, security, and migration impact;
- commands used to validate the change;
- remaining limitations or follow-up work.

Use tests to demonstrate behavior. If automation is not practical, include a deterministic manual verification path and explain why.

## Engineering principles

- Prefer secure defaults and fail-closed behavior for consequential actions.
- Validate inputs at trust boundaries.
- Keep domain logic independent from UI and infrastructure adapters.
- Make side effects explicit, idempotent where practical, and observable.
- Do not describe mocks, fixtures, or synthetic data as production evidence.
- Update documentation when a public contract or setup path changes.

## Commit and branch conventions

Use a descriptive branch such as `fix/auth-boundary` or `docs/threat-model`. Write imperative commit subjects, keep commits reviewable, and do not mix unrelated changes.

# Portfolio consolidation record

Status: decisions recorded; migrations and archives require repository-specific review. No repository or branch should be deleted solely because it appears in this document.

## Canonical repositories

| Product family | Canonical repository | Sources to inventory before archival | Current action |
|---|---|---|---|
| AI Integration Course | `MicroAIStudios-DAO/ai-integration-course-v2` | `ai-online-course`, `literate-octo-winner`, `combocourse`, `fictional-octo-sniffle`, `Ai_course_react` | Compare curriculum, assets, auth, billing, analytics, and learner-progress code |
| Real-estate AI | `Gnoscenti/realestate-ai` | `realestate-ai-workspace`, `realtorai`, `realestate-ai-ios`, `Buffet-of-love` | Preserve unique mobile and workspace work; verify the paid flow |
| Founder operations | `Gnoscenti/LaunchOpsPro` | `microai-launchops`, `launchops-founder-edition`, `founder-autopilot`, `atlas-launchops`, `launchops-stack` | Import only distinct contracts, deployment assets, or workflows |
| Founder media | `Gnoscenti/founder-media-os` | `local-shorts-engine`; keep `fmo-worker` only if its service boundary remains independent | Convert rendering/provider logic into explicit modules |

## Migration gate

A source repository is ready for archival only when all conditions are met:

1. Default branch and every unmerged branch are inventoried.
2. Unique commits, assets, configuration, and documentation are classified.
3. Preserved work is moved by normal pull request with attribution.
4. Canonical repository builds and tests after the migration.
5. Source README points to the canonical repository and records the final commit.
6. Secrets and tracked environment files are reviewed privately; credentials are rotated when necessary.
7. The owner explicitly approves GitHub archival.

## Secret-review exception

`Gnoscenti/fictional-octo-sniffle` was reported to contain a tracked root `.env`. Do not print, paste, or move its values. Review the file and history privately, remove tracked secret material in a dedicated security change, rotate any real credentials, and consider history rewriting only with an owner-approved incident plan.

## What consolidation is not

- It is not bulk copying one repository over another.
- It is not deleting branches to improve a metric.
- It is not claiming two products are identical because their dependency lists overlap.
- It is not archiving before unique work and deployment dependencies are understood.

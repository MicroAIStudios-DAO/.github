# Branch lifecycle policy

The goal is a readable release history without destroying unmerged work.

## Required protections

- Protect the default branch; require pull requests and passing CI.
- Disallow force-pushes and deletion of the default branch.
- Prefer squash merges for focused changes and descriptive merge titles.
- Use `agent/<scope>`, `fix/<scope>`, `feature/<scope>`, or `docs/<scope>` branch names.
- Keep one purpose per branch and link it to a pull request or issue.

## Triage process for branch-heavy repositories

For `ai-integration-course-v2`, `ai-integration-course`, and `quickstart-testing`:

1. Export branch name, tip SHA, last-commit date, author, and associated pull request.
2. Compare every tip with the default branch; label it merged, patch-equivalent, divergent, or unknown.
3. Assign an owner and disposition: merge, extract selected commits, preserve with a tag, or delete.
4. Open pull requests for valuable divergent work.
5. Wait at least 14 days after publishing the inventory before deleting anything.
6. Delete only branches with explicit owner approval; retain an audit record of deleted tip SHAs.

## Definition of done

A healthy active repository has a protected default branch, fewer than ten unexplained long-lived branches, no abandoned open pull requests, and a release/tag strategy described in its README or release documentation.

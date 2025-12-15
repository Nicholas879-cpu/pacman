# ADR 0001 – Branching Model Decision

## Status
Accepted

## Context
This repository is used for a DevOps Fundamentals hands-on exercise.
I need a simple Git workflow that supports fast feedback, is easy to demo,
and works well with CI/CD pipelines.

## Decision
Use **Trunk-Based Development** with short-lived feature branches.

- `master` is the main/trunk branch.
- New work is done in small branches named like `feature/readme-devops-exercise`.
- Changes are merged back into `master` using pull requests (PRs).
- Branches are deleted after merge to keep the history clean.

## Alternatives Considered
- **GitFlow** (develop, release, hotfix branches):
  - More complex and better for large products with slower release cycles.
  - Too heavy for this small training repository.
- **Committing directly to `master`**:
  - Simple but risky.
  - No pull request review and easy to break the main branch.

## Consequences
- Keeps `master` stable and always releasable.
- Encourages small, frequent changes instead of big risky ones.
- Works nicely with CI/CD because each PR can trigger automated checks.
- Easy to explain and demo as part of DevOps Fundamentals training.

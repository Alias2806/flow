# ADR 0001: Use Flow Before Creating a Dedicated Repository

- **Status:** Accepted
- **Date:** 2026-08-24
- **Decision owners:** Project maintainers
- **Related:** [Contributing Guidelines](../../CONTRIBUTING.md)

## Context

Creating a dedicated repository for every new idea can lead to abandoned repositories when an idea is not validated or no longer actively maintained.

We need a shared place to record decisions, starter documentation, experiments, and lessons learned before creating a dedicated repository or organization.

## Decision

New ideas and project foundations will be documented and tested in the `flow` repository first. The documentation may include:

- Architectural and technical decisions
- Starter guides and reusable templates
- Project structure proposals
- Experiments and validation notes
- Lessons learned and follow-up decisions

## Consequences

### Positive

- Ideas can be explored without creating unnecessary repositories
- Decisions and reasoning remain available for future reference
- Related experiments and starter documentation have one home
- Repository creation becomes an intentional graduation step

### Negative

- This repository may contain projects and topics in different stages
- Contributors need to keep entries organized and clearly labeled
- A project may need to be moved or adapted when it graduates

## Approval and Graduation

An idea can graduate when it has demonstrated enough value, clarity, and maintenance potential to justify its own repository or organization. Graduation should include:

1. A clear project purpose and scope
2. Evidence from the relevant experiment or starter documentation
3. A decision to continue active development
4. A dedicated destination repository or organization
5. Links between the original documentation and the graduated project

If an idea is paused, rejected, archived, or needs further evaluation, its documentation can return to `flow` for future reference or reconsideration.

## Review

This ADR should be revisited if the repository becomes difficult to organize, if projects need a different lifecycle, or if the graduation criteria no longer fit how ideas are developed.

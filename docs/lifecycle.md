# Documentation Lifecycle Guide

This guide defines the lifecycle for ideas, decisions, starter guides, and configuration work in `flow`. Use it when opening or updating an issue so the work has a clear status and next step.

## Lifecycle Stages

### 1. Proposed

The idea or change has been captured, but its scope and value still need discussion.

Expected evidence:

- A clear problem, opportunity, or question
- The intended outcome
- An owner or contributors for the next step

### 2. Under Review

The proposal is being refined through discussion, research, or an experiment.

Expected evidence:

- Relevant context and alternatives
- Open questions and risks
- A small validation plan or concrete acceptance criteria

### 3. Approved

The maintainers agree that the proposal is useful and clear enough to document or implement.

Expected evidence:

- Review feedback has been addressed
- The resulting documentation or configuration is usable
- Follow-up work is recorded in issues where needed

### 4. Ready for Graduation

The idea has demonstrated enough value and maintenance potential to move to a dedicated repository or organization.

Expected evidence:

- A clear purpose and scope
- Evidence from validation or real use
- A decision to continue active development
- A proposed destination and an owner for the move

### 5. Graduated

The work has moved to its dedicated destination. Keep a link here so the original reasoning and history remain discoverable.

### 6. Paused, Archived, or Rejected

The work is not currently moving forward. Record why and what would justify reopening it. Paused or archived work may return to `flow` for reconsideration.

## Moving Between Stages

An issue should have one current stage. When the stage changes:

1. Update the stage checklist in the issue.
2. Add a short note explaining what changed and why.
3. Link related decisions, pull requests, experiments, or destination repositories.
4. Leave unresolved questions visible rather than silently carrying them forward.

Stages do not have to be strictly linear. For example, an item can return from `Under Review` to `Proposed`, or from `Ready for Graduation` to `Paused`.

## Issue Checklist

Use the checklist that matches the current stage:

- [ ] Proposed: problem, scope, and intended outcome are clear
- [ ] Under Review: context, alternatives, risks, and validation are documented
- [ ] Approved: feedback is addressed and the result is usable
- [ ] Ready for Graduation: value, ownership, evidence, and destination are clear
- [ ] Graduated: destination link and ownership are recorded
- [ ] Paused / Archived / Rejected: reason and possible next step are recorded

## Related Guidance

- [Contributing Guidelines](../CONTRIBUTING.md)
- [ADR 0001: Use Flow Before Creating a Dedicated Repository](decisions/0001-use-flow-before-dedicated-repository.md)

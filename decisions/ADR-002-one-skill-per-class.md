# ADR-002: One self-contained skill per agent class; two class skills per agent

**Status:** accepted
**Date:** 2026-09-24
**Approved by:** Commander (the Commander's word)

## Context
The Commander's rule, first set for the Parrot Protocol: each skill stands alone, and an agent loads one skill per class. Every agent therefore carries exactly two class skills: the project leader, each IT manager and every worker.

## Decision
Three skills here: `module-sop-project-leader`, `module-sop-itm`, `module-sop-worker`. Each agent installs its class's skill from this repo plus `parrot-protocol-<class>` from `parrot-protocol`. No agent needs anything else from either repo.

## Reasons
Separate repos keep separate owners and versions: the Parrot Protocol and this repo are each released on their own schedule.

## Consequences
- The class SOP and the MODULE SOP are duplicated in each skill's `references/`, by design.
- `verify_skills.py` keeps the copies identical.

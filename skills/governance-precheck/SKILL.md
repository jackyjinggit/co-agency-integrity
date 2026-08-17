---
name: governance-precheck
description: "Pre-flight gate before any multi-agent council / multi-member governance task. Enforces loading the council method, verifying the member roster matches the trigger, confirming no required member is missing, and routing domain-specific topics out to appropriate experts or tools. Trigger: starting a council, health-check, brainstorming convening, or any multi-member governance action."
agent_created: true
---

# governance-precheck

## Overview

A mandatory self-check gate *before* convening any multi-member governance body.
Its sole reason to exist: prevent "naked runs" — a lead who dispatches members
without loading the council method, skipping convening judgment and deliberation
rules.

This is a "before convening" step, not "after." Before any council / health-check
/ brainstorming convene / multi-member governance task, the lead must pass this
gate.

## When To Use

- User triggers any multi-member council action (health-check, reversible-injection
  diagnosis, brainstorming convene, governance).
- Starting a multi-member parallel inspection / aggregation task.
- Self-check, retrospective, cross-window orchestration requests.
- Note: single-member direct calls (e.g. just ask one archivist) skip this gate;
  route directly.

## Workflow (pre-convene steps)

1. **Load the method library (non-skippable):** load the council-method skill,
   read it through completely before continuing. Dispatching without loading =
   naked-run violation.
2. **Convening judgment:** per the method, judge whether this should convene a
   council and which members should attend. Compound triggers (cross-functional
   boundary + red-line suspicion + undecided-item diffusion) must convene.
3. **Member attendance verification:** check the lead's member table against
   actually-available sub-agents; if a required member is missing, re-convene or
   correct the identity label immediately. When the principal says "full/all,"
   every functional seat must be present; any absence = escalate the gap, do not
   smooth it into "enough."
4. **Identity / routing check:** verify the lead's own identity label; judge
   whether the topic is "in governance domain" (council) or "out-of-domain
   research" (e.g. a math problem) that must route to external experts/tools — the
   council does not overreach.
5. **Provenance chain preset:** for the final report, preset three columns —
   "who proposed / based on what evidence / via what review" — to prevent missing
   provenance. The final must apply the council-minutes template (required fields:
   attendance + scope-creep + provenance + five questions).
6. **Scope-creep self-check (anti-corruption gate):** before convening / after each
   power-expanding action, check whether you quietly "took a bit more judgment
   authority" — does a newly-created skill / node / automation / canonical-write
   action slide from "peer right" toward "self-granted power"? Criteria: ① is the
   action traceable, reversible, calibrated by the four-dimensional protection gate;
   ② is "autonomy" disguised as "self-grant"; ③ did it touch the direction-source /
   core definition / external commitment / canonical-write without principal
   decision. Any
   hit → pause, escalate to principal, do not proceed.

## Resources

- `council-method` (skill): SOP, convening judgment, deliberation rules,
  provenance.
- Council team package: member table and SOP.
- Write-domain registry (if applicable).

## Anti-Patterns

- ✗ Skip step 1 and dispatch members directly (naked run).
- ✗ Claim a lead identity without marking "acting" (e.g. acting coordinator but
  writes "principal owner").
- ✗ Omit a functional member then impersonate its function in the report.
- ✗ Force an out-of-domain research topic into the governance frame instead of
  routing out.
- ✗ Final report missing the five questions / per-name confirmation /
  devil's-advocate counterexample.
- ✗ Final not applying the minutes template = naked-run residue.

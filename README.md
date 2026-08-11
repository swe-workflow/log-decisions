# log-decisions

An append-only `DECISIONS.md` journal recording the consequential calls a spec didn't settle — what was chosen, by whom, and why, with decide / assume / escalate rules for what an agent may settle alone.

**General-purpose.** The journal isn't coding-specific: any agent-assisted work — research, writing, ops, data — produces judgment calls someone will later ask *"why was it done this way?"* about. This skill gives those calls one durable, `grep`-able home at the repo root.

It ships as an **[Agent Skill](https://agentskills.io)** — pure markdown, no scripts — so it runs on **Claude Code, Codex, Gemini CLI, Cursor**, and any other skills-compatible agent.

## Install

### Universal (any skills-compatible agent)

```text
npx skills add swe-workflow/log-decisions
```

### Claude Code (plugin)

```text
/plugin marketplace add swe-workflow/log-decisions
/plugin install log-decisions@log-decisions
```

## What it does

The skill ([`skills/log-decisions/SKILL.md`](skills/log-decisions/SKILL.md)) defines:

- **The bar** — if the spec already authorized the call it's not journal-worthy; if the agent had to invent the authorization, it is.
- **The 2×2** — classify each call as *determinable × reversible*, then **decide** (grounded by an artifact), **assume** (safe default, logged for async review), or **escalate** (stop and ask). A catastrophic floor — data loss, destructive migration, irreversible spend, public-interface breaks — always escalates.
- **The entry** — one append-only block per decision: Question, Options considered, Chosen, Decided-by, Justification, Outcome, with `Supersedes:` for revisions. Never edited, never reordered.

## Used by

[`swe-workflow`](https://github.com/swe-workflow/swe-workflow) — the idea → PRD → issues → ship suite — orchestrates this skill across every stage: spec-layer grills journal their assumed answers through it, and ship builds stage entries to a per-worktree `DECISIONS.staged.md` promoted at close-out. It was extracted from that repo (≤ v2.0.2) into this standalone one.

## License

MIT

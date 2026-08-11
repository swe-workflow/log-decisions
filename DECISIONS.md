<!-- AI-maintained, append-only -->

## 2026-08-11T14:42:55-07:00 — interactive/thariq-prompt — gate-resolution

**Question:** Which elements of Thariq's implementation-notes prompt should the skill absorb?
**Options considered:** adopt its three behaviors into the journal / also adopt its running-HTML-file format / add a separate per-task notes file alongside DECISIONS.md
**Chosen:** Absorb the three behaviors — reader-side significance test ("would the brief's author want to know before accepting?"), log-at-the-moment-of-the-call timing, and an at-handoff review queue of assumed/escalated entries — into the existing journal; the entry format is unchanged.
**Decided-by:** agent
**Justification:** The prompt's value is its framing (reader-facing, running, confirm-or-revise), not its format; a second notes file would split the single source of truth the journal exists to be, and an unchanged entry format keeps existing journals and the swe-workflow suite compatible.
**Outcome:** applied
**Ref:** (pending)

## 2026-08-11T14:43:10-07:00 — interactive/thariq-prompt — gate-resolution

**Question:** What vocabulary replaces the coding-specific terms when generalizing the skill?
**Options considered:** "brief" / "instructions" / "the ask" for the governing document; "project root" / "working directory" for the journal's location
**Chosen:** "brief" (defined once in the intro as instructions, requirements, a prompt, or an ask) and "project root"; the catastrophic floor and the worked example were rewritten domain-neutral (publishing/sending, a report-currency call).
**Decided-by:** agent (the generalization itself was directed by the user mid-session)
**Justification:** "Brief" is the domain-neutral term of art across writing, research, and consulting, and reads naturally for code too; "project root" names the same location without presuming version control.
**Outcome:** applied
**Ref:** (pending)

## 2026-08-11T14:46:24-07:00 — interactive/thariq-prompt — gate-resolution

**Question:** What vocabulary replaces the coding-specific terms when generalizing the skill?
**Options considered:** "brief" / "spec" / "instructions" for the governing document
**Chosen:** "spec", defined once in the intro as instructions, requirements, a prompt, or an ask; "project root" and the domain-neutral floor and example stand.
**Decided-by:** human
**Justification:** User chose the familiar term over "brief"; generality is carried by the inline definition rather than the word itself.
**Outcome:** applied
**Ref:** (pending)
**Supersedes:** 2026-08-11T14:43:10-07:00 — user reversed the agent's word choice

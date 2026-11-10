# Domain docs

## Layout and reading rules

This repository uses a single-context layout:

- `GLOSSARY.md` at the repository root defines domain vocabulary.
- `docs/adr/` holds architectural decision records.

Before exploring the codebase, read the glossary and ADRs relevant
to the area being changed.

If these documents are absent, proceed silently. The domain-modeling
skill creates them when terms or decisions are resolved.

## Vocabulary

Use glossary terms when naming domain concepts in issues, proposals,
code, and tests.

If a needed concept is missing, reconsider whether it belongs in the
domain or note the gap for domain-modeling.

## Decision conflicts

Explicitly identify any proposal that contradicts an existing ADR,
cite that ADR, and explain why the decision should be reconsidered.

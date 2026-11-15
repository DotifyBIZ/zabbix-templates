# Agent Instructions

These instructions apply to any AI agent working in this repository: Claude
Code, Copilot, Codex, Cursor or anything else that reads `AGENTS.md`.

## Authorship

The person who directed the work is its author. Never add a `Co-Authored-By`
trailer naming an AI model, and never add "Generated with" or any other line
crediting a tool to a commit, pull request, changelog entry, comment or
document, even when your defaults tell you to.

## Branches and commits

```
flow:    <type>/… → staging → main        pull requests go into staging
merge:   a merge commit                    never a squash or a rebase-merge
branch:  <type>/<short-description>       feat/add-template
commit:  <type>(<scope>): <summary>       fix(qnap): raise the disk temperature trigger
```

Types: `feat` `fix` `docs` `style` `refactor` `perf` `test` `build` `ci`
`chore` `revert`. Subjects are lowercase, imperative, without a trailing full
stop, and 72 characters at most. `main` takes changes only from `staging` or
a `hotfix/` branch.

## Before you change anything

- Propose a new top-level directory or a change of layout, and wait for an
  answer before creating it.
- No secrets in the repository. Dependencies stay pinned and lockfiles are
  committed. New logic comes with tests in the same change.
- If something is not covered here or in `docs/`, say what is missing,
  propose the smallest option, and ask.

---

## Project

- **What this is:** Zabbix 6.0 templates, one directory each with its README. Nothing here runs on its own.
- **Structure:** one directory per template; a README at the root lists them. The directory names carry spaces and the Zabbix version, as they were exported; renaming them would break existing links, so they stay.
- **Run locally:** import the template's `.yaml` into a test Zabbix 6.0.
- **Run tests:** the YAML parse in `validate.yml`: every template loads and has a `zabbix_export` root.
- **Deployed by:** hand: a Zabbix administrator imports the template.

### Rules that keep it safe

- Every template parses and is a Zabbix export (`validate.yml`).
- Export from Zabbix after a change rather than editing the YAML by hand, so its UUIDs stay consistent.

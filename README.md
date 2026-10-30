# Woodstock

> Part of the [AWITHI](https://github.com/awithi-co) family — *AI with AI*. The stage where the bands play, and the stock of tools you pull from.

A plugin marketplace for Claude Code and Codex. It only lists where each plugin lives; the code stays in each band's own repository.

| Plugin | What it does | Access |
|---|---|---|
| [ACDC](https://github.com/awithi-co/acdc) | Agent Context Delivery Channel. Session handoff between Claude Code and Codex. | Public |
| RHCP | Readable Hangul Composition Partner. Thinking interview and Korean document guide. | Private |
| KISS | Keep It Scalable & Simple. Architecture decision partner for existing systems. | Private |

Private plugins install only with read access to their repository. Without it, that install fails with `not found` and the others still work.

## Install

Claude Code:
```
/plugin marketplace add awithi-co/woodstock
/plugin install acdc@woodstock
```

Codex:
```
codex plugin marketplace add awithi-co/woodstock
codex plugin add acdc@woodstock
```

For private plugins, set up git credentials on that machine first: `gh auth login && gh auth setup-git`.

## Update

Each plugin updates when its version changes.

- Claude Code: `/plugin marketplace update woodstock`, then `claude plugin update <plugin>@woodstock`
- Codex: `codex plugin marketplace upgrade woodstock`

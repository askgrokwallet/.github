# Contributing to AskGrokWallet

Thanks for helping make governed agent spending real.

## What we accept

- Bug reports with a minimal reproduction (policy text + expected vs actual verdict)
- Feature proposals that stay in scope: **the rules/approval/receipt layer** — not another wallet rail
- Documentation and test improvements
- Marketplace packaging fixes (`.grok-plugin` / `.cursor-plugin` manifests, `SKILL.md`)

## Development setup

```bash
# The app + engine live in the project workspace; the plugin package is the repo.
cd projects/grokbotwallet
npm install
npm run dev            # approval inbox at http://localhost:3000/approvals
node scripts/test-policy.mjs
npm run contracts:test # hardhat vault tests
```

## Before opening a PR

- Run the smoke checks: `node scripts/smoke.mjs` (plugin repo)
- Keep the plugin free of secrets and remote code execution patterns (the xAI/Cursor marketplaces audit this)
- One logical change per PR; keep the diff minimal
- Update `CHANGELOG.md` for user-visible changes

## Commit style

- Imperative subject line: `add policy rule for daily budget carryover`
- Keep the pinned marketplace SHA in sync if you touch the plugin repo (see `docs/16-marketplace-pr-prep.md` in the project workspace)

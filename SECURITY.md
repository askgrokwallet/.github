# Security Policy

AskGrokWallet is a governance layer: it sits **in front of money movement**. Security is the product.

## Reporting a vulnerability

Please **do not open a public issue** for security problems. Report privately:

- GitHub private vulnerability reporting: use the "Report a vulnerability" button on
  [askgrokwallet/askgrokwallet](https://github.com/askgrokwallet/askgrokwallet/security/advisories)
- Or email the maintainers via the address listed on the repo

We aim to acknowledge reports within 48 hours and ship a fix for high-severity issues within 7 days.

## Security expectations for this codebase

- The plugin **never** requests private keys, passwords, or credentials
- Policy, budgets, and allowlists are always operator-defined; the skill never invents them
- Blocked actions return a reason and are **never** executed
- Receipts record who, what, how much, verdict, decision, and timestamps
- Marketplace packaging must contain no `curl | bash`, remote code download/exec, or credential exfiltration patterns

## Scope

In scope: the plugin package (`askgrokwallet/askgrokwallet`), the policy compiler, the approval store, and the Boundless vault contracts.

Out of scope: the underlying chains, wallets, and payment rails AskGrokWallet integrates with.

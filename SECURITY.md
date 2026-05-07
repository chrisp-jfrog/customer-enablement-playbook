# Security Policy

## Supported Versions

| Version | Supported |
|---|---|
| `main` | ✅ Actively maintained |
| Older branches | ❌ Not supported |

---

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

If you discover a security vulnerability in this repository — including sensitive data exposure, secrets committed to version history, or unsafe scripts — please report it responsibly:

1. **Email:** Send details to **[INSERT SECURITY EMAIL]**
2. **Subject line:** `[SECURITY] Customer Enablement Playbook — <brief description>`
3. **Include:**
   - A description of the vulnerability and its potential impact
   - Steps to reproduce or a proof-of-concept if applicable
   - Any suggested remediation

---

## What to Expect

| Timeframe | Action |
|---|---|
| Within **2 business days** | Acknowledgement of your report |
| Within **7 business days** | Initial assessment and severity classification |
| Within **30 days** | Resolution or documented remediation plan |

We will keep you informed throughout the process and credit you in the fix (unless you prefer to remain anonymous).

---

## Scope

This policy covers:

- Content, scripts, and templates in this repository
- Accidental exposure of credentials, tokens, or PII in committed files
- Unsafe automation scripts that could cause unintended data access or modification

This policy does **not** cover vulnerabilities in third-party tools or services referenced by this repo. Please report those directly to the respective maintainers.

---

## Security Best Practices for Contributors

- Never commit API keys, tokens, passwords, or PII
- Use `.gitignore` to exclude sensitive local config files
- Run `git log` and `git diff` before pushing to confirm no secrets are staged
- If you accidentally commit a secret, rotate it immediately and contact the maintainers

---

*This project takes security seriously. Thank you for helping keep it safe.*

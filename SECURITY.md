# Security Policy

## Supported versions

Only the latest minor release receives security patches. Always stay on the
current `main` branch in production.

| Version | Supported          |
| ------- | ------------------ |
| 1.x     | ✅ Yes             |
| < 1.0   | ❌ No              |

## Reporting a vulnerability

**Please do not open public GitHub issues for security concerns.**

Instead, email `security@lumen.app` with:
- A clear description of the issue
- Steps to reproduce (curl / network log / repro app preferred)
- Affected version(s)
- Proposed severity (Low / Medium / High / Critical)

We aim to acknowledge the report within **48 hours** and ship a patch within
**14 days** for Critical issues. We will credit you in the release notes unless
you prefer to remain anonymous.

## Safe defaults enforced in this repo

- No inline scripts / styles. Static assets only.
- `.env`, `google-services.json`, `*.keystore`, key materials are gitignored.
- Secrets are never imported by client-side code.
- All network calls in production must use HTTPS; WebView cleartext is disabled.
- Dependencies are kept minimal; `npm audit --production` is part of CI.

# Security Policy — JudgeForge

## Public demo warning

The hosted public deployment at https://judgeforge.onrender.com/ is an **evaluation demo**. In demo mode, sample accounts, static demonstration credentials, and predictable test tokens may be available. This is intentional for testing and is **not production authentication**.

**Do not** upload confidential hackathon submissions, real participant personal information, private judging remarks, or sensitive attachments to the public demonstration service.

## Production hardening checklist

- Set `DEMO_MODE=false` and remove or rotate all shared demonstration credentials.
- Configure strong private secrets and protected production identities.
- Apply HTTPS, secure cookies, access controls, rate limiting and appropriate audit-log retention.
- Use persistent storage, proper backups and tested database migrations for real events; free ephemeral hosts may lose SQLite data.
- Verify role isolation and cross-judge confidentiality using the existing tests.
- Review [THREAT-MODEL.md](THREAT-MODEL.md) and [RELEASE-CHECKLIST.md](RELEASE-CHECKLIST.md) before any production rollout.

## Vulnerability reporting

Avoid filing public GitHub issues containing exploitation instructions, credentials, or personal data. Contact the maintainer privately through their [GitHub profile](https://github.com/rajsalonia) or GitHub's private vulnerability reporting feature if available. Provide a minimal reproducible example using synthetic records and allow coordinated remediation.

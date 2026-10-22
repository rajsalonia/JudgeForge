# Contributing to JudgeForge

JudgeForge is a self-hosted platform for hackathon submissions, role-isolated judging, and auditable results.

## Developer workflow
1. Review [ARCHITECTURE.md](ARCHITECTURE.md), [DATA-MODEL.md](DATA-MODEL.md), and [THREAT-MODEL.md](THREAT-MODEL.md).
2. Create a focused branch, keep changes reviewable, and include a clear problem statement in the pull request.
3. Run `pytest -q` and the local acceptance checker `python run.py .dogfood.toml` where your environment supports them.
4. Include tests for changes to access control, deadlines, normalization, migrations, or audit records.
5. Update [JUDGING.md](JUDGING.md) if you alter score aggregation or ranking rules.

## Security and data handling
- Public hosted demos with demo accounts are **not safe for real participant records**.
- Preserve organizer/judge/participant role separation and peer-score isolation.
- Use synthetic participant identities and project submissions in tests.
- Never commit signing keys, real session tokens, private submissions, or exported judging data.
- See [SECURITY.md](SECURITY.md) for responsible disclosure.

## PR checklist
- [ ] Authorization and isolation tests pass
- [ ] Existing SQLite schema and migrations remain compatible
- [ ] New user flows are documented
- [ ] Sensitive demo/production boundaries remain explicit

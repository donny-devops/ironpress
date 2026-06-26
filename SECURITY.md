SECURITY.md
Project: ironpress
Maintainer: donny-devops
Security contact: security@donny-devops.com
Primary disclosure channel: GitHub Security Advisories

Purpose
This document explains how to report security vulnerabilities, what to expect after a report, and the security practices we follow for the ironpress project. Our goal is to fix issues quickly and responsibly while protecting users and maintainers.

Supported versions
Supported: Releases tagged in the main branch and the last two stable release tags.

Unsupported: Older tags not listed above. If you discover a vulnerability in an unsupported version, report it and we will advise on mitigation and backporting.

Reporting a vulnerability
Preferred method: Create a private report via GitHub Security Advisories for this repository.
Alternative: Email security@donny-devops.com with encrypted details using our PGP key. Include the following in your report:

Summary of the issue and affected component

Steps to reproduce with minimal reproducible example or PoC code

Impact assessment including data exposure, privilege escalation, or remote code execution potential

Environment details such as version, OS, and configuration

Suggested remediation if available

Do not open a public issue or pull request for a security report. Public disclosure may put users at risk.

PGP key
To encrypt sensitive reports, use our PGP key fingerprint below. If you need the full key, request it via security@donny-devops.com.

PGP fingerprint: REPLACE-WITH-ACTUAL-FINGERPRINT

What we will do after a report
Acknowledge receipt within 48 hours.

Triage and assign severity within 5 business days.

Work with the reporter to validate and reproduce the issue.

Develop a fix and prepare a patch or mitigation.

Coordinate disclosure with the reporter and affected parties.

Publish advisory and release patched versions.

Credit the reporter unless they request anonymity.

If we cannot reproduce the issue or need more information, we will request additional details from the reporter.

Response timeline and disclosure policy
Initial acknowledgement: within 48 hours.

Triage and classification: within 5 business days.

Fix or mitigation plan: target within 30 days for high severity issues.

Coordinated disclosure: we will agree on a disclosure date with the reporter. If a fix cannot be produced in a reasonable time, we will provide mitigations and a timeline.

Emergency exceptions: for critical vulnerabilities with active exploitation, we may expedite fixes and disclosure.

Severity classification
Critical: Remote code execution, complete data exposure, or full system compromise.

High: Privilege escalation, significant data exposure, or service compromise.

Medium: Information leakage, bypass of important controls, or local privilege issues.

Low: Minor issues, best-practice gaps, or low-impact bugs.

Severity is determined by impact, exploitability, and affected user base.

Safe harbor
If you follow this policy in good faith and provide a vulnerability report, we will not pursue legal action against you for your good-faith security research. Do not access or exfiltrate user data beyond what is necessary to demonstrate the issue.

Remediation and releases
Security fixes will be released as patch versions when possible.

We will provide migration notes and upgrade instructions in the release notes.

For infrastructure or configuration issues, we will publish mitigation steps and recommended configuration changes.

Security practices we follow
Secrets management: No secrets in source control. Use Railway environment variables and GitHub Secrets for CI. Rotate secrets regularly.

Dependency scanning: Automated dependency checks in CI using tools such as dependency review and container scanning.

Container and image scanning: CI includes image scanning for known vulnerabilities.

Static analysis: Rust Clippy and ESLint rules run in CI.

Runtime monitoring: Railway Observability for metrics and logs.

Access control: Principle of least privilege for service accounts and deploy tokens.

Backups and recovery: Managed database backups and tested restore procedures.

Logging and correlation: Structured logs with correlation IDs for incident investigation.

Rate limiting and webhook validation: Webhook signatures validated and rate limiting enforced using Redis.

Incident response
If you believe a security incident is in progress, contact security@donny-devops.com immediately and include:

What happened and when it started

Systems affected and scope of impact

Evidence such as logs, alerts, or screenshots
We will respond according to our incident response plan and provide updates to affected parties as required.

CVE and public advisories
We will request CVE identifiers for vulnerabilities that meet CVE criteria. Public advisories will include affected versions, impact, remediation steps, and credits.

Third-party components
If a vulnerability is in a third-party dependency, we will:

Report upstream to the dependency maintainers

Coordinate fixes and backports where feasible

Patch or vendor the dependency if necessary

Disclosure credits
We will credit reporters in advisories unless they request anonymity. If you prefer no credit, state that in your report.

Contact and escalation
Primary: security@donny-devops.com

GitHub Security Advisories: use the repository's security advisory flow for private disclosure
If you do not receive a timely response, escalate by opening a private GitHub Security Advisory and referencing this policy.

Acknowledgments
Thank you to the security researchers and contributors who help keep ironpress safe. Your responsible disclosure helps protect all users.

Changes to this policy
We may update this policy over time. The current version is stored in this repository as SECURITY.md. Changes will be noted in the repository history.

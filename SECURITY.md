# Security Policy

This policy applies to all repositories in the Rekise Marine
(`rekise`) GitHub organization. It is published here so external
researchers, partners, and customers have a single, public place to
find Rekise Marine's vulnerability disclosure process — even when
individual repositories are private.

## Reporting a Vulnerability

If you discover a security vulnerability in any Rekise Marine
software, please report it privately. **Do not file a public GitHub
issue or pull request.**

- Email: security@rekise.com
- Subject: `[Rekise Vulnerability] <repository or product> — <short description>`

Please include:

- Affected repository, package, or product
- Affected version(s) — git commit SHA, package version, or release tag
- Steps to reproduce
- Impact assessment (confidentiality / integrity / availability)
- Suggested mitigation, if known
- Whether you wish to be credited in any subsequent advisory

PGP / signed email is welcome but not required.

## Response

Expect a timely acknowledgement of your report, normally within five
business days, during which time Rekise Marine will triage the
vulnerability and engage the appropriate maintainers. Severity is
assessed using [CVSS v3.1](https://www.first.org/cvss/); fix timelines
are communicated with the reporter once triage is complete.

## Disclosure Policy

Rekise Marine follows coordinated disclosure:

- We work with the reporter to validate the report and develop a fix.
- Public disclosure happens after a fix is released or, if no fix is feasible, after the reporter has been informed and a reasonable disclosure window (typically 90 days from initial report) has elapsed.
- Reporters are credited in any subsequent advisory unless they request anonymity.

Please do not publicly share details of the vulnerability until the
disclosure window has elapsed or a fix has been released.

## Supported Versions

Rekise Marine supports the most recent minor version on the `dev`
branch and the latest tagged release of each repository. Older
versions are supported on a best-effort basis. Repositories with their
own per-repo support policy supersede this default.

## Out of Scope

The following are not eligible for this disclosure process:

- Vulnerabilities in third-party dependencies — please report those upstream first; Rekise Marine will track and patch as patches become available.
- Social engineering of Rekise Marine employees.
- Denial-of-service via volumetric attacks.
- Physical attacks on Rekise Marine hardware or facilities.

## REP-2004 Conformance

This policy satisfies [REP-2004](https://www.ros.org/reps/rep-2004.html)
§7 ("Vulnerability Disclosure Policy") for all ROS 2 packages in the
`rekise` organization, modeled on the spirit of
[REP-2006](https://www.ros.org/reps/rep-2006.html). Per-package
`QUALITY_DECLARATION.md` files cite this org-level policy by reference.

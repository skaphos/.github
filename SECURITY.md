# Skaphos Security Policy

This is the fallback vulnerability reporting policy for Skaphos repositories
that do not publish their own policy. If a repository has a `SECURITY.md`, use
its project-specific reporting instructions and scope. This policy also covers
this organization's community files and shared resources.

## Reporting a vulnerability

**Do not report suspected vulnerabilities in public issues, discussions, or
pull requests.**

Use **Security → Report a vulnerability** in the affected repository when that
option is available. Otherwise, email [shawn@skaphos.io](mailto:shawn@skaphos.io)
with the repository name in the subject. Email is also the fallback if you
cannot use GitHub, are unsure which project is affected, or the report spans
multiple Skaphos projects. The contact coordinates triage with the relevant
maintainers.

## Security scope

Report issues that can compromise confidentiality, integrity, or availability
in a Skaphos project or its distributed artifacts. Relevant examples include
credential exposure, unauthorized access or mutation, code execution from
untrusted input, release artifact tampering, and violations of isolation or
other documented security guarantees.

Assess severity against the affected project's privileges, deployment, and
users. A small maintainer team does not imply low impact: projects handling
cluster trust, delivery controls, or privileged operations may need additional
review and coordinated downstream response. This fallback sets a reporting
process; it is not a complete threat model for every project.

## What to include

Include the affected repository, version or commit, platform and relevant
configuration, reproduction steps or a minimal proof of concept, and the
impact you believe is possible. Explain what an attacker controls and which
security boundary is crossed. A suggested fix is welcome but not required.

Use synthetic data and redact credentials and private repository content.
Please report suspected issues even if you cannot reproduce them on the latest
release or are unsure whether they are vulnerabilities.

## Response and coordinated disclosure

- We aim to acknowledge reports within **7 days**. If you have not heard back,
  follow up by email with the repository name and the date of your report.
- Maintainers assess the report with the reporter, including affected versions,
  realistic exploitability, impact, and severity. A scanner alert alone does
  not establish impact, but reports do not need a complete exploit to be useful.
- We limit embargoed information to people needed for triage, remediation, and
  coordinated release. We develop and review security fixes privately and test
  that the reported issue is resolved before publishing the patch.
- We aim to release a fix or mitigation and disclose within **90 days** of the
  report. This is a coordination target, not a guaranteed fix date or an
  obligation on reporters to remain silent indefinitely. We discuss timing
  changes with the reporter; active exploitation can require earlier notice.
- We coordinate the patched release with a public security advisory describing
  impact, affected and fixed versions, and any mitigation. For vulnerabilities
  eligible for a CVE, we request an identifier through GitHub or another CVE
  Numbering Authority and include it in the advisory. Exploit details may be
  delayed to give users time to update.
- We credit reporters unless they prefer anonymity. If triage finds a regular
  bug or a hardening opportunity, we explain why and coordinate moving it to a
  public issue only after checking that doing so exposes no unresolved
  vulnerability.

## Versions and dependencies

Security fixes normally target the latest release. Report the version you use;
we assess affected versions and any need for backports during triage rather
than rejecting reports solely because they concern an older release. For
unreleased projects, include the commit you tested.

Dependency vulnerabilities are relevant when they affect this project's use of
the dependency. Include that context if known; maintainers will coordinate
with upstream as needed. Do not disclose an embargoed upstream issue publicly.

## Bug bounty

This policy does not offer a paid bug bounty.

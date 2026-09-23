# Freedom Community Automation

Shared repository templates and read-only verification for FreeTWAI-AI projects.
The existing organization profile remains in `profile/README.md`.

`.github/workflows/verify-template.yml` is a reusable `workflow_call` workflow.
Consumers pin its exact commit, and third-party actions are pinned to immutable
commits. It installs locked dependencies without lifecycle scripts, checks the
pinned Platform contract bundle and project manifest, then runs tests and local
builds. It has only `contents: read`, does not persist checkout credentials, and
has no deployment steps or provider secrets.

Calling this workflow provides CI evidence; it does **not** establish that an
organization ruleset requires it, that a maintainer review happened, that a
release is signed, or that a public site was deployed. The manifest's quality
fields describe intended policy. Enforced gates must be checked separately in
GitHub settings.

Shared issue and pull-request templates are in `.github/`. They help connect a
change to the affected module, Platform contract version, and reproducible test.
No invented teams or CODEOWNERS entries are supplied. Repository ownership and
maintenance identify the observed `FreeTWAI-AI` organization and `teddashh` user.

Licensing has not been chosen for this bootstrap. `NOASSERTION` and
`source_available` are metadata, not a license grant.

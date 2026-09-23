# Freedom Community Automation

<!-- freedom-repository-guide:start -->
## 在自由工坊的位置

[自由工坊](https://freetwai.com) 讓會員先完成定位、選擇公會並領取 Repo 技能書，再以供貨、商店、開源作品、行銷與小隊共同完成成果。

FreeTWAI-AI 的組織介紹、共用 Issue／PR 範本与唯讀 CI 入口。 已有 profile、任務表單與可供各倉用 commit SHA 固定的 reusable verification workflow。

workflow 存在或跑綠不表示 ruleset 已強制、維護者已審核、release 已簽章或網站已部署。

本 repo 的維護者負責「FreeTWAI-AI 的組織介紹、共用 Issue／PR 範本与唯讀 CI 入口。」這個模組；公會職稱與自填 GitHub slug 不授予寫入權。

程式／內容入口：[profile/README.md](profile/README.md)、[.github/ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE/)、[.github/PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md)、[.github/workflows/verify-template.yml](.github/workflows/verify-template.yml)、[scripts/verify-contracts.mjs](scripts/verify-contracts.mjs)。協作先讀 [CONTRIBUTING.md](CONTRIBUTING.md)，讓 Agent 讀 [AGENTS.md](AGENTS.md)；從[本倉 Issues](https://github.com/FreeTWAI-AI/.github/issues)認領、[查看既有 PR](https://github.com/FreeTWAI-AI/.github/pulls)避免重工。

這裡維護組織協作規則，不維護會員 DB 或業務權限。中央契約由 freedom-platform 產出；此 workflow 保持最小 contents:read，不夾帶部署或私人 provider secrets。 跨 repo 的協定由[中央平台](https://github.com/FreeTWAI-AI/freedom-platform)維護。
<!-- freedom-repository-guide:end -->

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

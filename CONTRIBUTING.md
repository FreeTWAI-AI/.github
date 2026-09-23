# Contributing

Start in the repository for the template or module you are changing. Describe the
member action that should work, the current behavior, and a small reproducible
example. Keep Platform identities, ownership, permissions and business state in
`freedom-platform`; a template consumes its versioned API and does not create a
second database or invent authority.

Use the pinned runtime and lockfile. Run the repository's tests and build, and
include the command results in your pull request. If API shapes change, update
the canonical Platform contract first, regenerate the pinned client, and verify
the affected consumers together. Do not fix a mismatch by silently editing a
generated vendor file.

Use synthetic fixtures. Never attach cookies, access tokens, private customer
records or provider credentials to an issue or commit. Public GitHub metadata
and source commits are useful evidence; a manually entered claim is not proof
of ownership, payment, publication or official release status.

A passing workflow is test evidence. Production deployment, paid resources and
external publication need their own authorized action. This bootstrap introduces
no contribution license agreement or new license grant.

<!-- freedom-repository-guide:start -->
## 自由工坊：從一個成果到一個 PR

FreeTWAI-AI 的組織介紹、共用 Issue／PR 範本与唯讀 CI 入口。 已有 profile、任務表單與可供各倉用 commit SHA 固定的 reusable verification workflow。

先看[本倉 Issues](https://github.com/FreeTWAI-AI/.github/issues)與[現有 PR](https://github.com/FreeTWAI-AI/.github/pulls)。提出問題、這一輪範圍、完成條件與可投入時間，在 Issue 認領並協調重疊工作；維護者已直接派工時不必重複等待，將約定連回交接即可。使用自己的 fork／分支，PR 送到 **FreeTWAI-AI/.github:main**。

交給 Agent 前先讓它讀 [AGENTS.md](AGENTS.md)。PR 寫明變更用途、使用者可見結果、驗證命令、限制與原 Issue；附上可公開的合成案例或重現方式。Issue／PR 是程式協作的記錄，平台名片與公會身分不取代 repo 維護者的審查。

這裡維護組織協作規則，不維護會員 DB 或業務權限。中央契約由 freedom-platform 產出；此 workflow 保持最小 contents:read，不夾帶部署或私人 provider secrets。

### 這個模組怎麼驗證

選擇與修改範圍相符的既有入口：

```sh
npm test
npm run build
```

命令列在這裡不表示本輪已執行。先核對依賴與環境，再記錄實際結果；缺工具、桌面、媒體或授權時寫 `not_run` 與原因，不能補造成功。純文件修改以連結／路徑核對與 `git diff --check` 為主。

### 署名與上游

本 repo 的維護者負責「FreeTWAI-AI 的組織介紹、共用 Issue／PR 範本与唯讀 CI 入口。」這個模組；公會職稱與自填 GitHub slug 不授予寫入權。 保留原作者與授權檔，另列真正完成文件、測試、設計、程式或協作的人。使用 AI 時如實交代協作範圍；只有實際 GitHub PR／review／合併紀錄可以作為對應貢獻證據，不能靠自填帳號推定。

自願貢獻不保證案源、XP、收益或雇用。若產生付費合作，由當事人另定條款與 Seller 外部收款；平台不代收。秘密、客戶資料、真實交易單據與未授權素材不進公開 Issue／PR。
<!-- freedom-repository-guide:end -->

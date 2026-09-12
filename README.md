# SILO50 Simulation

一套以 **Silo / Wool / Shift 氛圍與制度邏輯為靈感**、但使用獨立遊戲規則與原創事件的長期地堡管理文字模擬框架。

目前穩定版本：**v4.1**

> 本專案是非官方、粉絲向的文字模擬規則專案，與原作作者、出版社、Apple 或相關權利人無關。  
> 專案中的遊戲原創角色、事件、機制與 Golden Run 範例不應被視為原作正式設定。

---

## 專案特色

- 50 座固定拓撲地堡
- Silo 1 中央管理視角
- `PROJECT > DIRECTIVE > PACT` 權限層級
- 1 號地堡內部依 **DIRECTIVE**
- 2–50 號地堡主要依 **PACT** 管理
- NPC 知識防火牆
- 私人操作與遠端對話隔離
- 長期冷凍休眠與世代演化
- 世界在玩家休眠時持續運作
- Year 500 強制終局評估
- 終局只能有 **0 或 1** 個獲勝地堡
- Golden Run 回歸範本
- 500 輪 QA 回歸測試
- 一次性新手教學

---

## 快速開始

1. 開啟 `src/SILO50_SIM_INTEGRATED_v4.1_NEW_PLAYER_TUTORIAL.txt`
2. 將整份規則載入你使用的文字模型 / 遊戲主持環境
3. 從全新遊戲開始
4. 系統會先顯示一次簡短新手教學，之後正式進入值班

### 輸入方式

```text
直接輸入文字
```

代表玩家在遊戲內說話或行動。

```text
(調閱監控)
```

代表 **1 號地堡內部私人操作**，遠端地堡不會聽見。

```text
*修改對話風格
```

代表 **遊戲外規則修改**，不推進世界時間。

---

## 建議 Repository 結構

```text
SILO50-GitHub/
├─ README.md
├─ CHANGELOG.md
├─ VERSION
├─ .gitignore
├─ LICENSE-NOTICE.md
├─ src/
│  └─ SILO50_SIM_INTEGRATED_v4.1_NEW_PLAYER_TUTORIAL.txt
├─ docs/
│  ├─ QUICKSTART.md
│  ├─ RULES_OVERVIEW.md
│  └─ GOLDEN_RUN.md
├─ qa/
│  ├─ SILO50_SIM_v4.1_QA500_REPORT.txt
│  ├─ SILO50_SIM_QA500_CONSOLIDATED_v4.0_v4.1.txt
│  └─ history/
│     └─ SILO50_SIM_v4.0_QA500_REPORT.txt
└─ .github/
   ├─ PULL_REQUEST_TEMPLATE.md
   └─ ISSUE_TEMPLATE/
      ├─ bug_report.md
      └─ feature_request.md
```

---

## 核心概念

### 權限

```text
PROJECT > DIRECTIVE > PACT
```

但三者不是全域套用：

- **Silo 1 內部**：DIRECTIVE
- **Silos 2–50**：PACT 為主要管理框架
- **PROJECT**：更高層權限

### 知識防火牆

角色只能根據自己合理能取得的資訊說話。

因此：

- 遠端角色不會知道玩家括號內的私人操作
- 普通居民通常不知道自己的地堡編號
- 通訊線路不等於可通行地道
- 玩家有高權限，但不是全知

### 長期模擬

冷凍休眠不會停止世界。

休眠期間仍會處理：

- NPC 老化、死亡、繁衍與接班
- 地堡政治
- 資源與基礎設施
- 異常事件
- Silo 1 輪值
- 情報延遲與失真

### 終局

Year 500 必須進行一次且僅一次的 Project Final Evaluation。

終局：

```text
surviving_silo_count ∈ {0,1}
```

任何獲勝地堡都必須由本局累積世界狀態決定，不能硬編碼。

---

## Golden Run

`docs/GOLDEN_RUN.md` 收錄目前基準局的主要發展，用來測試：

- 規則一致性
- 權限作用域
- 長休眠
- Silo 1 / 遠端知識隔離
- Project 隱藏設施
- Year 500 終局

Golden Run **不是固定劇情**，也不代表未來每局必須走同樣結果。

---

## QA

目前：

```text
v4.0 QA500: 500 / 500 PASS
v4.1 QA500: 500 / 500 PASS
```

詳細內容請見 `qa/`。

---

## 授權與權利提醒

本 Repository **沒有自動附加開源授權**。

原因是本專案包含對既有小說 / 電視作品世界觀與術語的粉絲向引用與靈感來源。  
若你打算公開發布、商業化或接受外部貢獻，建議先確認相關權利，再決定是否加入 MIT、Apache-2.0、GPL 或其他 License。

詳見 `LICENSE-NOTICE.md`.

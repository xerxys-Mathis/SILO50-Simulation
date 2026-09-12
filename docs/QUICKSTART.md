# Quick Start

## 1. 載入主規則

主檔：

```text
src/SILO50_SIM_INTEGRATED_v4.1_NEW_PLAYER_TUTORIAL.txt
```

整份載入，不要拆開部分章節單獨執行。

## 2. 開始新遊戲

全新遊戲第一次啟動時，應顯示一次新手教學。

新手教學只顯示一次，不應在以下情況重播：

- 讀取既有進度
- 冷凍甦醒
- 下一輪值班
- 緊急喚醒

## 3. 遊戲輸入

### 普通遊戲指令

```text
調查22號的異常
```

會被視為遊戲內行動 / 對話。

### 私人 Silo 1 操作

```text
(調閱22號監控)
```

不會被遠端通話者聽見。

### 遊戲外規則修改

```text
*對話更口語一點
```

修改規則，不推進遊戲時間。

## 4. 重要原則

- 不把未知資訊直接補成真相
- 不讓 NPC 突然知道自己不該知道的資訊
- 不把管線 / 通訊線誤判成可走人的地道
- Silo 1 內部使用 DIRECTIVE
- 其他地堡主要使用 PACT
- Project 終局在 Year 500
- 終局最多一個地堡勝出

## 5. 建議執行方式

如果模型支援長上下文，直接載入完整主規則。

如果模型上下文有限，建議至少保留：

1. Core Engine
2. Geography
3. Input Router
4. Authority
5. Knowledge Firewall
6. Rotation / Cryosleep
7. Year 500 Terminal Rules

# MoCKA Outfield — Public Network and External Input Layer

<p align="center">
  <img src="https://raw.githubusercontent.com/m-sirius-k/MoCKA/main/docs/images/mocka_overview.svg" width="800">
</p>

> **This is not a public API. Not a webhook receiver. Not a data pipeline.**
> It is the sanitized boundary between the outside world and MoCKA core.
>
> Nothing enters MoCKA directly from outside.
> Everything passes through outfield first.

---

## Position in mocka_Movement

<p align="center">
  <img src="https://raw.githubusercontent.com/m-sirius-k/MoCKA/main/docs/images/mocka_architecture_v2.svg" width="720">
</p>
```
Outside world · external agents · public signals
      ↓
[ mocka-outfield ]         ← ① Observe input — YOU ARE HERE
      ↓
mocka_Receptor
      ↓
acceptor:infield / acceptor:outfield
      ↓
mocka_insight_system (mocka_Movement + shadow_Movement)
```

**Loop step: ① Observe — external input source**
Upstream: The outside world · external agents · public signals
Downstream: mocka_Receptor → acceptor:infield

---

## What this repository does

<p align="center">
  <img src="https://raw.githubusercontent.com/m-sirius-k/MoCKA/main/docs/images/mocka_loop_v2.svg" width="720">
</p>

mocka-outfield forms the sanitized boundary
between the outside world and MoCKA core.

### Strict Separation
```
infield  = internal memory · private · trusted
outfield = external interface · public · sanitized
```

Direct infield-to-outfield publishing is forbidden.
Only sanitized content crosses the boundary.

### First Contact Layer
```
Outside world touches MoCKA
      ↓
outfield receives first
      ↓
sanitizes the signal
      ↓
passes to mocka_Receptor
      ↓
MoCKA civilization core remains protected
```

This protects the civilization core from contamination.

### Cross-Agent Synchronization

External AI agents communicate through outfield.
It is the public-facing side of the infield/outfield architecture.
```
acceptor:infield   ← internal memory · accumulation
acceptor:outfield  ← external sharing · publication
      ↑
outfield manages the boundary between these two
```

---

## Quick Start
```powershell
# Verify outfield connection
mocka-check

# View recent external signals
Get-Content "events\outfield_log.csv" -ErrorAction SilentlyContinue |
  Select-Object -Last 10
```

---

## Status

**Active Development**
Part of the MoCKA deterministic governance architecture.
Loop position: ① Observe — external input

---

## 日本語

### MoCKA Outfieldとは何か

公開APIではありません。Webhookレシーバーでもありません。
外部世界とMoCKAコアの間のサニタイズされた境界です。

外部から直接MoCKAに入るものは何もありません。
すべてがまずoutfieldを通過します。

### mocka_Movementにおける位置づけ
```
外部世界 · 外部エージェント · 公開シグナル
      ↓
[ mocka-outfield ]         ← ① Observe input — ここです
      ↓
mocka_Receptor
      ↓
acceptor:infield / acceptor:outfield
      ↓
mocka_insight_system
```

**ループステップ：① Observe — 外部入力ソース**
上流：外部世界 · 外部エージェント · 公開シグナル
下流：mocka_Receptor → acceptor:infield

### このリポジトリの役割

外部世界とMoCKAコアの間のサニタイズされた境界を形成します。

### 厳格な分離
```
infield  = 内部記憶 · プライベート · 信頼済み
outfield = 外部インターフェース · 公開 · サニタイズ済み
```

infieldからoutfieldへの直接公開は禁止されています。
サニタイズ済みのコンテンツだけが境界を越えます。

### ファーストコンタクト層

外部世界がMoCKAに触れる時、まずoutfieldに触れます。
outfieldがサニタイズしてからmocka_Receptorに渡します。
これが文明コアを汚染から守ります。

### エージェント間同期

外部AIエージェントはoutfieldを通じて通信します。
infield/outfieldアーキテクチャの公開側です。

---

Part of the [MoCKA Deterministic Governance Architecture](https://github.com/m-sirius-k/MoCKA).

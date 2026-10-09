# Defeating the KTM 5-Poison Threat

復古 16-bit 像素風格的網頁拳擊遊戲。打敗 5 名對手，最後擊敗 Boss，高舉刻著「順」字的金牌冠軍腰帶！

**▶ 立即遊玩：https://alexshlin.github.io/boxing_soon/**

電腦、手機都能玩。所有像素圖、音效與配樂都由程式即時產生，不需要任何外部圖檔或音檔，整個遊戲只有一個 `index.html`。

## 遊戲流程

1. 選擇難度：EASY / NORMAL / HARD
2. 從 5 名對手中自由選擇對戰順序，打敗的對手會蓋上 KO 章
3. 5 人全部打敗後進入 Boss 戰
4. 擊敗 Boss 後播放過關畫面：選手高舉金牌腰帶，背景有煙火與彩帶

每場比賽 3 回合、每回合 90 秒。血量歸零會倒地，裁判開始讀秒；被擊倒 3 次即 T.K.O.。時間到還沒 KO，就比剩餘血量判定勝負。

## 操作方式

| 動作 | 鍵盤 | 手機 |
|---|---|---|
| 閃躲 | ← → 或 A / D | ◀ 閃 / 閃 ▶ |
| 防禦（按住） | ↓ 或 S | 防禦 |
| 左拳（快） | Z 或 J | 左拳 |
| 右拳（重） | X 或 K | 右拳 |
| 身體攻擊 | 按住防禦 + 出拳 | 按住防禦 + 出拳 |
| 必殺拳 | Space 或 ↑ | ★ 必殺 |
| 確認 | Enter | 點擊畫面 |
| 暫停 / 靜音 | P / M | 左上 II / 右上 ♪ |

手機直式時按鈕在畫面下方，橫式時按鈕分在畫面左右兩側。

## 戰鬥技巧

- **看預兆**：對手拳套閃白光代表要出拳；紅色「!!」是無法防禦的攻擊，一定要閃。
- **閃躲反擊**：成功閃過攻擊後對手會暈眩，這時打中傷害 ×1.5。
- **打斷刺拳**：在對手蓄力刺拳時用右拳打中，可以直接打斷。
- **連擊**：連續命中 3 / 6 / 10 下，傷害倍率為 ×1.2 / ×1.5 / ×2。
- **必殺拳**：每次連擊滿 10 下得到一顆星（最多 3 顆），按必殺鍵放出無法防禦的重擊。
- **身體攻擊**：對手舉高雙拳護頭時，改打身體可以穿過防守。
- **防禦條**：防禦會消耗防禦條，被打太多次會破防並暈眩。
- **倒地**：被擊倒時連打出拳鍵，在讀秒到 10 之前站起來。

## 對手

| # | 名字 | 稱號 | 招牌技 |
|---|---|---|---|
| 1 | Lo Chih-chiang | THE JAB MACHINE | MACHINE GUN JAB：連續 5 記刺拳，用防禦擋下 |
| 2 | Wang Hung-wei | THE FEINT QUEEN | FAKE OUT：假上鉤拳接真刺拳，別太早閃 |
| 3 | Lee Yen-hsiu | LIGHTNING STEPS | DASH HOOK：側步留下殘影後出勾拳 |
| 4 | Lai Shyh-Bao | THE BULLDOZER | BELLY SLAM：跳起雙拳砸下，無法防禦 |
| 5 | Hsu Chiao-Hsin | COUNTER STRIKER | COUNTER STANCE：架勢中出拳會被反擊，等她收招 |
| BOSS | Chiang Wan-an | THE FINAL BOSS | GOLDEN FIST：金色蓄力重拳；血量剩一半進入第二階段 |

## 技術說明

- 單一 HTML 檔，無任何外部相依套件或素材
- 畫面：Canvas 2D，原生解析度 256×224（SNES 規格），以 `image-rendering: pixelated` 放大
- 角色、文字（3×5 像素字型）、背景全部以程式繪製
- 音效與晶片音樂：Web Audio API 即時合成，含簡易音序器
- 進度與最高分存於瀏覽器 `localStorage`

## 本機執行

直接用瀏覽器打開 `index.html` 即可，不需要安裝或建置。

```bash
git clone https://github.com/alexSHLin/boxing_soon.git
open boxing_soon/index.html
```

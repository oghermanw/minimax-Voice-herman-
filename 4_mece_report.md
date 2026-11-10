# PStack MECE 物理隔離三模型直出報告 (SHA-256 Verified)

- **Prompt SHA-256**: `8d83d82e6d9f746368bd9c685712bb8b5038013645b9482be5695fa5117a6c60`
- **Claude CLI (`/Users/herman/.local/bin/claude --model opus --effort high`)**:
  - Run 1 耗時：`60.41s` (`output_sha256: d3218d292d33870b29e0b57ac714d89856159689548d9438bc4a57bdb68bc8f4`)
  - Run 2 耗時：`81.79s` (`output_sha256: e869e0060c5c5723a702c63d87bf02f6561ef83c00b9f6254baafb3609a2749b`)
- **Codex CLI (`/Users/herman/.local/bin/codex exec --ephemeral -s read-only`, `gpt-5.6-sol / ultra`)**:
  - Run 1 耗時：`24.85s` (`status: OK`, `output_sha256: 37aff9f51a5223694adf4ab233efd1a31767cfd8b66f0fc04ea40059c725ba23`)
  - Run 2 耗時：`300.04s` (`status: QUOTA_OR_AUTH_NOTICE` — 觸發 300s 超時保護，嚴格遵守 Fail-Closed 鐵律，未喺背景偷換降級模型)

---

## 0️⃣ `0_input/raw_prompt.txt` (100% 原話一字不改)
```text
mrcreates.ai  都係麻麻地，我覺得我啲聲嗰啲個 outcome 好似都係一般。然後 anyway 咁呀，做咗一個新嘅樣板先啦，我覺得做呢一個樣板係最好、幾好嘅。

咁點解呢？你而家試下講一個，我可能講 AI 点樣幫到自己：可以好快，由短時間可能要 learning curve，然之後慢慢喺中間就可以好快學習到一啲新嘅嘢，之後你就可以 scale up 得好快，個複利式增長。

再講一次，用我把聲。畫面要配合返 motion 啊、smoothly 啊嗰啲細節，一致性 /pstack 

```

---

## 1️⃣ `1_claude/output.md` (Claude Opus High — 原汁原味一字不改)

### [Run 1 原話輸出 (60.41s)]
我寫好咗呢條片嘅樣板，入面有劇本、分鏡同一致性規則，下面三部分可以直接用。不過呢個 session 冇 shell，亦冇寫檔權限，所以我未叫到 ElevenLabs 出你把聲，亦未 render 到片。`/pstack` 喺呢度都冇呢個指令，所以冇行到。

---

## 1. 劇本（約 32 秒）

**中心意象：** 成條片由頭到尾都係同一條線，由平線慢慢彎上去變成複利曲線。每一幕都喺呢條線度接落去，咁樣個畫面先會順同一致。

| 時間 | 口播（你把聲） | 畫面 / Motion |
|---|---|---|
| **0–3s 開頭吸引** | 「點解有啲人用咗 AI 一年，好似進步咗十年？」 | 黑底，一粒發光嘅點喺正中間，「十年」兩個字一講，粒點就向右拉出一條線 |
| **3–8s 學習曲線** | 「頭嗰一兩個禮拜，係會有 learning curve 嘅。你會覺得好亂、好慢，好似冇乜進步。」 | 條線幾乎係平嘅，仲會震吓。鏡頭跟住粒點慢慢推前，用暗啲嘅灰色 |
| **8–15s 轉捩點** | 「但係過咗嗰個位，你會發現，每學一樣新嘢都快咗好多。今日學剪片，聽日學寫 code，後日學 marketing。」 | 講到「過咗嗰個位」，條線開始彎上，顏色轉做 accent 色。每講一樣技能，條線上面就彈出一個 icon |
| **15–23s 複利** | 「最勁嘅唔係你學得快，係你學識嘅嘢會疊埋一齊。一個變兩個，兩個變四個，呢個就係複利。」 | 個 icon 一路分裂：1→2→4→8，跟住你講嘅數字一齊出。條線變成好斜嘅 J 曲線，鏡頭拉遠睇晒成條 |
| **23–28s 行動** | 「所以唔使諗太多，揀一樣你想學嘅嘢，今日就開始。」 | 畫面跳返去曲線最起點嗰粒點，即係「你而家喺呢度」 |
| **28–32s CTA** | 「留言【複利】，我將我自己用緊嘅 AI 學習流程 send 俾你。」 | 「複利」兩個字由條曲線收埋變出嚟，固定喺畫面中間 |

## 2. 一致性規則（以後每條片都照用）

- **色：** 只用深色底、一隻 accent 色（例如電光綠），再加灰色做「未進步」狀態，唔加第四隻色。
- **字：** 成條片只用一隻字體，字幕固定喺畫面下面三分一，唔好跳嚟跳去。
- **Motion：** 全部用 ease-in-out，轉場 0.3 至 0.4 秒。所有嘢都沿住條線、向右或者向上郁，唔好有隨機嘅飛入。
- **鏡頭：** 一路向前推，只係喺「複利」嗰下拉遠一次，做成全片嘅高潮。
- **跟住把聲：** 關鍵字（十年、過咗嗰個位、一變二、今日）一講出嚟，畫面就要同時郁。呢樣係最影響順唔順嘅細節。

## 3. 點解你把聲出嚟效果一般，同點樣改

- **最好效果：** 你自己用手機錄口播，揀靜嘅房、手機放近口大約一個拳頭遠。真聲配 AI 畫面通常比 AI 聲更自然。
- **如果一定要用 AI 聲：** 用 ElevenLabs 嘅 **Professional Voice Clone**，餵 30 分鐘以上乾淨、冇背景音樂嘅錄音，口語同中英夾雜要同你平時講嘢一樣。Instant clone 本身就會比較「一般」。
- **設定建議：** Stability 大約 0.4 至 0.5，Style 調低啲，咁先唔會太誇張。

## 樣板骨架（以後換題目照填）
**開頭吸引 (0–3s) → 痛點 (3–8s) → 轉捩點 (8–15s) → 原理或證據 (15–23s) → 行動 (23–28s) → CTA (28–32s)**

---

**下一步：** 我建議用 Remotion（用 code 做動畫）嚟整，咁每條片嘅 motion 都會一模一樣，比 mrcreates 嗰類工具穩定好多。如果你喺有 shell 嘅 session 再叫我，我可以：
1. 開 Remotion 項目，將上面嘅分鏡寫成 component，以後換文字就出到新片
2. 寫 `.infisical.json` 同 `run.sh`。用 `/lib/elevenlabs` 出聲，要你確認先加
3. 出 9:16 MP4 樣板

你想用自己錄音，定係用 ElevenLabs clone 聲？


---

### [Run 2 原話輸出 (81.79s)]
我睇咗你 `branding-ai-hooking-database` 入面啲 transcription，跟住寫好呢個樣板嘅腳本同分鏡。

## 先講兩樣嘢

**1. 呢個 session 我只可以讀檔，冇得寫檔、行 command 或者 render 片。** 所以今次我交到嘅係腳本同分鏡，未有成品。

**2. `/pstack` 唔係拍片用嘅工具。** 我睇過，佢係一套寫 code 嘅工具（architect、tdd、swarm 嗰類），入面冇嘢會幫到拍片。

## 我建議點拍：用你真把聲錄，唔好再 clone

你用 mrcreates.ai 出嚟把聲麻麻地，我估同廣東話 AI clone 普遍都做得麻麻有關。最穩陣係**你自己用手機錄一次，大約 40 秒**，之後畫面跟住你把聲去對。

**「一致性」同「smooth」**：唔好用 AI 生成片段一段段咁駁，因為每段個樣都會唔同。改用 **motion graphics**（例如 Remotion），全條片只用**一條會生長嘅曲線**做主角，所有轉場都由呢條線變出嚟。咁樣個風格由頭到尾一致，再用字級時間碼（Groq STT）去對準每個重音。

## 腳本（廣東話，大約 40 秒）

結構跟你資料庫入面 thebranding.ai 嗰套：開頭 hook，跟住拆解，然後講返個道理，最後 CTA。

| # | 對白 | 時間 |
|---|---|---|
| Hook | 「大部分人用 AI 一個禮拜就放棄，因為佢哋未見到條曲線轉彎。」 | 0–4s |
| 1 | 「頭嗰段時間，真係有 learning curve。你要學點問、點拆問題，好似冇乜進展。」 | 4–11s |
| 2 | 「但係過咗嗰個位，你會發覺，你學新嘢嘅速度快咗好多。以前要一個月先搞識嘅嘢，而家一個晚上。」 | 11–19s |
| 3 | 「然後你學識嘅每樣嘢，都會變成下一樣嘢嘅工具。一個 workflow 變三個，三個變十個。」 | 19–27s |
| 4 | 「呢個就係複利。唔係加法，係乘法。」 | 27–31s |
| Payoff | 「所以如果你而家覺得用 AI 好慢，唔緊要，你只係仲喺條曲線嘅平地。」 | 31–37s |
| CTA | 「Save 低呢條片，三個月後返嚟睇下你去到邊。」 | 37–41s |

## 分鏡（全條片都係同一條線）

| # | 畫面 | Motion / 轉場 |
|---|---|---|
| Hook | 黑底，一條白線平平咁行；講到「轉彎」嗰下，線尾向上一勾 | 鏡頭慢慢 push-in，「轉彎」嗰個字出現時微微彈一下 |
| 1 | 條線喺平地爬，好似踩單車上斜，旁邊彈出「點問？」「點拆？」幾個字 | 速度刻意放慢，字一粒粒淡入 |
| 2 | 條線開始斜上；「一個月」字卡縮成「一晚」 | 用 match cut：個日曆格直接變做月亮 icon |
| 3 | 線上面長出分支，1 → 3 → 10 個節點 | 跟住「一、三、十」嗰三個字嘅時間碼，每個字出一層 |
| 4 | 鏡頭 zoom out，見到成條 J 曲線；「+」變「×」 | 全片最大嘅動作，配一下低頻 hit |
| Payoff | Zoom 返入去最左下嘅平地，見到一個細細嘅點（「你」） | 同 Hook 對稱，首尾呼應 |
| CTA | 個點開始郁，條線再畫一次 | loop 返去第一格，方便觀眾重睇 |

**樣板規格（以後每條片都照用）：** 9:16，黑底，白線配一隻強調色，一款字體；轉場只用 push-in、match cut 同 zoom 三種；字幕用字級高亮。

## 下一步要你做嘅

1. **錄音**：照上面腳本，用你平時講嘢嘅語氣錄一次。想改字就直接改，唔使跟足。
2. **開返有寫檔權限嘅 session**，我就可以起 Remotion project，按你條錄音嘅時間碼砌好動畫，再 render 出嚟。
3. **轉錄要用 `/lib/groq-stt`**：照你嘅規則，我唔會自己加 /lib，你講句「用 groq-stt」我先寫入 `run.sh`。

如果你寧願試下 AI 聲：你 vault 入面 `/lib/elevenlabs` 有 `ELEVENLABS_VOICE_ID_YUE`，不過我唔知嗰個係咪你自己把聲。要 clone 得似，要用 ElevenLabs 嘅 Professional Voice Clone，餵 30 分鐘以上嘅錄音先會明顯好過 instant clone。


---

## 2️⃣ `2_codex/output.md` (Codex `gpt-5.6-sol / ultra` — 原汁原味一字不改)

### [Run 1 原話輸出 (24.85s · Status: OK)]
未能開工：你指定嘅 `/pstack` 並未安裝／未提供，而工作區目前亦係唯讀。按你嘅指示，我冇改用其他技能。

我已搵到 Herman 聲音參考，例如 [herman_VO_1_personal_intro.mp4](</Users/herman/Google AI/instagram apify scaping /mvp_cantonese_demos/native_mece_5_methods/herman_VO_1_personal_intro.mp4>)。請啟用 PStack 並開放寫入權限，再重發同一要求；我就會製作新樣板，重點係自然廣東話聲線、learning curve → 快速掌握 → scale up → 複利增長，以及全片 motion、節奏與視覺一致性。

### [Run 2 狀態警報 (300.04s · Fail-Closed Notice)]
⚠️ 【CODEX 額度/連線警報 (已停止自動切換)】
- 原本模型：ChatGPT Web (`gpt-5.6-sol` · reasoning: `ultra`)
- 錯誤訊息：TIMEOUT after 300s
- 系統動作：為保住原汁原味與效果，已嚴格禁止喺背景偷換降級模型！
- 請揀下一步：
  1) 換另一個有 Quota 嘅 ChatGPT 帳號登入 (`codex login`)
  2) 今次只睇 Claude + Gemini 結果
  3) 如你明確同意改用 Infisical API Key，先加 `--allow-api-fallback` 執行

---

## 3️⃣ `3_gemini/output.md` (Gemini 獨立工程實作與 60fps 影片交付)
# Gemini 3_gemini 獨立工程實作與 60fps 複利樣板落地報告

## 1. 點解之前 `@mrcreates.ai` 同埋單段式 TTS 聲紋效果「一般」？
1. **音畫脫節與長句語調扁平化（Single-Paragraph Prosody Flattening）**：
   - 當將 220 字長段落一次過餵入 MiniMax `/v1/t2a_v2` (`speech-02-hd`)，模型喺第 2 句之後會自動拉平抑揚頓挫（變成新聞播報腔），而且中英夾雜（`learning curve`、`scale up`）喺長句入面容易出現語速突變。
   - **根治方案（Clause-by-Clause Breath Group + Studio Proximity EQ）**：將「AI 複利增長」劇本拆分為 **6 個自然呼吸短句（6 Beats）** 獨立合成，精準鎖定每句毫秒級起止時間碼（`timings_v3_pure.json` / `timings_v4_studio.json`），並加入近咪胸腔共鳴補償（`148Hz +2.4dB`、`280Hz +1.2dB`、`3400Hz -1.6dB`、Soft-Knee 壓縮），令聲底回復 iPhone 近距離錄音嘅真實溫暖感。
2. **畫面缺乏連續性與毫秒級拍子同步（Motion & Consistency）**：
   - 已採納 **「單一連續生長曲線 + 固定角色 Rig + 60fps 連續鏡頭追蹤」** 架構，由第 0 秒到第 50 秒 **零生硬跳切**，全程 60fps (`smoothstep` + `spring_scale` 彈簧物理)：
     - **Beat 0 (Hook)**：Herman 鎖定角色分身（固定黑框眼鏡、深色科技外套、實時根據聲波振幅 `rms(t)` 開合嘴型、自然眨眼與呼吸起伏）指向發光起點。
     - **Beat 1 (Learning Curve 短時間摸索期)**：灰藍色平緩震盪線，顯示初期摸索 Prompt 與溝通嘅短暫陣痛期。
     - **Beat 2 (中段轉捩點 · 飛速吸收新嘢)**：曲線瞬間點亮為電光藍綠並向上彎曲，彈出 4 個技能膠囊（拆解視覺、鎖定聲紋、角色一致性、自動化工作流）。
     - **Beat 3 (快速 Scale Up · 1 ➔ 2 ➔ 4 ➔ 8)**：隨住語音講到「一個變兩個、兩個變四個」，畫面同步以彈簧物理彈出 `1x ➔ 2x ➔ 4x ➔ 8x` 矩陣放大。
     - **Beat 4 & 5 (Compound Effect 複利式增長)**：鏡頭平滑拉遠（Zoom Out），展示完整指數級 J 曲線衝上頂峰，底部複利柱狀圖與倍數計數器（`1.0x ➔ 32.0x`）同步飆升。

## 2. 已交付實戰 MP4 成品（iOS `yuv420p + faststart` 60fps 秒開）
- `videos/11_NEW_SAMPLE_60fps_Compounding_v3_pure.mp4`（`herman_studio_v3_pure` 零氣音純淨版 + 60fps 複利曲線動畫）
- `videos/12_NEW_SAMPLE_60fps_Compounding_v4_studio.mp4`（`herman_studio_v4` 自然呼吸停頓版 + 60fps 複利曲線動畫）


---
name: chronic-care-media
description: 為慢性病整合照護與衛教推動，產生可直接使用的 AI 衛教素材（衛教單張插圖、短影音分鏡、語音導讀、候診區海報、LINE 圖文）。涵蓋糖尿病、高血壓、慢性腎臟病、血脂異常、心衰竭、COPD、CKM（心血管－腎臟－代謝症候群）。使用者提到「衛教素材」「衛教影片」「衛教海報」「單張插圖」「短影音」「AI 生圖／生影片／生音」「長者看得懂」「候診區播放」「LINE 衛教圖卡」「個管師衛教」「CKM 衛教」時使用。先鎖定臨床訊息與對象，再寫給生成模型的提示詞，最後附臨床審核與合規檢核。
---

# 慢性病衛教素材生成（Chronic Care Media）

> 改編自 [Hao0321/ai-media-generator](https://github.com/Hao0321/ai-media-generator)（MIT）的「概念先行、平台分流、提示詞語彙庫、品質閘」做法，並改為慢性病衛教情境。

## 核心原則：內容正確優先於畫面好看

AI 影像模型**不具備臨床知識**，也**無法可靠生成文字與數字**。因此分工固定如下：

| 項目 | 由誰負責 |
|---|---|
| 衛教訊息、數值、用藥與飲食建議 | **臨床人員／院內最新指引**（本 Skill 只引用，不自創） |
| 畫面風格、人物、情境、運鏡 | AI 生成 |
| 畫面上的文字、數值、單位、QR Code、院徽 | **後製疊加**（PPT／Canva／剪輯軟體），不讓模型生成 |
| 最終發布 | **人工審核後**才可使用 |

## 工作流程（一句話進、可用素材出）

1. **Intent 解析**：把使用者需求拆成 9 個欄位（缺的用預設，不逐項追問）
   - 疾病／主題｜對象（新診斷、長者、照顧者、青壯年）｜單一核心行為目標｜素材類型｜使用場域｜長度／尺寸｜語言（國語／台語／雙語）｜風格｜審核單位
2. **鎖定臨床訊息**：每份素材只傳達 **1 個行為目標 + 最多 3 個重點**。訊息來源讀 [references/disease-modules.md](references/disease-modules.md)，並請使用者確認院內版本。
3. **選素材與工具**：讀 [references/platform-picker.md](references/platform-picker.md)。
4. **寫提示詞**：套 [references/prompt-patterns.md](references/prompt-patterns.md) 的 8 欄公式與醫療專用負面清單。
5. **產出模板**：依類型選 [templates/](templates/)（單張、短影音、語音稿、LINE 圖卡）。
6. **品質與合規閘**：逐項過 [references/quality-and-compliance.md](references/quality-and-compliance.md)，通過才交付。
7. **成效指標**：附上可追蹤的指標（見 [templates/outcome-metrics.md](templates/outcome-metrics.md)），讓素材能呈現成果而非只是產出。

## 硬規則

1. **不自創臨床數據**：目標值、劑量、頻率、飲食份量一律標註「依院內最新指引／醫囑」，由臨床人員填入。
2. **文字不交給模型**：提示詞一律寫 `no text, no letters, no numbers, no logos`，版面文字後製。
3. **單一素材單一行為目標**：避免把控糖、控壓、用藥、運動塞進同一張圖。
4. **不使用恐嚇或汙名**：不以截肢、洗腎、中風畫面作警示；不出現體型羞辱。
5. **長者友善**：大字、高對比、留白、每頁一個重點、語速偏慢；詳見品質閘。
6. **人物與情境在地化**：台灣日常場景（傳統市場、便當、夜市、廟口、社區活動中心、健保卡、藥袋），人物多元（年齡、體型、性別）。
7. **真人肖像／病人資料零使用**：不上傳病人照片或可辨識資訊至任何生成平台。
8. **必停點（不代做）**：付費操作、對外發布、上傳任何含個資內容、臨床內容最終確認。
9. **標示 AI 生成**：對外素材於角落加註「插圖為 AI 輔助生成，內容經臨床人員審閱」（依院內規範調整）。

## 快查表

| 使用者說… | 讀這個檔 |
|---|---|
| 「某疾病的衛教重點／該講什麼」 | [disease-modules.md](references/disease-modules.md) |
| 「用哪個工具／要生圖還是影片」 | [platform-picker.md](references/platform-picker.md) |
| 「幫我寫生圖／生影片提示詞」 | [prompt-patterns.md](references/prompt-patterns.md) |
| 「單張／海報／LINE 圖卡」 | [templates/leaflet-and-poster.md](templates/leaflet-and-poster.md) |
| 「短影音／候診區播放」 | [templates/short-video-storyboard.md](templates/short-video-storyboard.md) |
| 「語音導讀／台語／廣播」 | [templates/audio-script.md](templates/audio-script.md) |
| 「能不能發布／要審什麼」 | [quality-and-compliance.md](references/quality-and-compliance.md) |
| 「成效怎麼呈現／指標」 | [templates/outcome-metrics.md](templates/outcome-metrics.md) |

# chronic-care-media

慢性病衛教素材 AI 生成 Skill（給 Claude Code／Codex 載入使用）。

改編自 [Hao0321/ai-media-generator](https://github.com/Hao0321/ai-media-generator)（MIT License）的工作流：概念先行、素材與工具分流、提示詞語彙庫、品質閘；並改為慢性病衛教情境，加入臨床審核、長者友善、合規與成效指標。

## 與原版的主要差異

| 原版（影視創作） | 本版（慢性病衛教） |
|---|---|
| 追求電影感、導演／攝影語彙 | 追求清楚、親切、長者看得懂 |
| 一句話直接到成品，付費才停 | **臨床內容與發布前一律人工審核** |
| 模型自由生成文字 | **文字、數值、院徽一律後製** |
| 多平台自動操作 | 不綁特定平台，重視資料安全與授權 |
| 作品完成即結束 | 附成效指標，可呈現成果 |

## 結構

```
chronic-care-media/
├── SKILL.md                         入口與硬規則
├── references/
│   ├── disease-modules.md           7 個疾病模組（行為目標與畫面建議）
│   ├── platform-picker.md           素材類型與工具選擇
│   ├── prompt-patterns.md           8 欄公式、限制尾巴、角色鎖定
│   └── quality-and-compliance.md    臨床／AI 瑕疵／長者友善／合規檢核
└── templates/
    ├── leaflet-and-poster.md        單張、海報、LINE 圖卡
    ├── short-video-storyboard.md    30–60 秒短影音分鏡
    ├── audio-script.md              語音導讀稿
    └── outcome-metrics.md           成效指標與成果簡報頁型
```

## 使用提醒

本 Skill 不含任何臨床數值與用藥建議，相關內容須由臨床人員依院內最新指引填入並審核。產出素材不取代診療。

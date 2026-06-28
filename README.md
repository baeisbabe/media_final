# Final 自主學習作業: Hermes Agent 多代理人短影片工作流程

## 專案概要

本專案依照多媒體系統期末自主學習作業規範，使用 Hermes Agent 建立多代理人影音生成流程，主題為「國立臺南大學資訊工程學系 60 秒形象宣傳影片」。

最終影片已輸出為 `outputs/final_video.mp4`，長度 60.291 秒，解析度 1920x1080。影片影像素材使用 ChatGPT 生成，背景音樂使用 Suno 生成，剪輯與輸出使用 Microsoft Clipchamp。

## 主要交付物

| Path | Content |
|---|---|
| `report/Final_Report_Final.pdf` | 最終 PDF 報告 |
| `report/Final_Report_Draft.md` | PDF 報告來源 Markdown |
| `outputs/final_video.mp4` | 最終 60 秒 MP4 影片 |
| `outputs/subtitles.srt` | 旁白與字幕檔 |
| `outputs/video_production_design.md` | 影片設計、旁白、音樂與剪輯設計 |
| `outputs/image_generation_prompts.md` | ChatGPT 圖片生成 prompt |
| `outputs/asset_sources.md` | 素材來源與服務條款紀錄 |
| `agents/` | Planner、Script、Visual、Reviewer、Finalizer agent 設定 |
| `handoff/` | 多代理人 structured handoff JSON |
| `traces/execution_trace.md` | Hermes 執行紀錄 |
| `traces/hermes_conversation_log.md` | Prompt / output 對照整理 |
| `traces/screenshots/` | Hermes 執行截圖 |
| `baseline/single_agent_baseline.md` | Single-agent baseline comparison |

## Hermes Workflow

```text
User Brief
  -> Planner Agent
  -> Script Agent
  -> Visual Agent
  -> Reviewer Agent
  -> Finalizer Agent
  -> Human Editing in Clipchamp
  -> Final 60-second Video
```

Hermes 執行採用 zero-paid-token mock/stub dry-run，不使用付費 API key、信用卡或商業 LLM API 作為必要流程。ChatGPT、Suno 與 Clipchamp 只作為最終素材製作與剪輯工具，並已在來源表中揭露。

## Final Video Metadata

| Item | Value |
|---|---|
| File | `outputs/final_video.mp4` |
| Duration | 60.291 seconds |
| Required range | 55-65 seconds |
| Resolution | 1920x1080 |
| Video codec | avc1 |
| Audio codec | mp4a |
| File size | 39,907,159 bytes |

## Repository Structure

```text
C:\media_final
|-- README.md
|-- report/
|   |-- Final_Report_Draft.md
|   |-- Final_Report_Draft.html
|   |-- Final_Report_Final.pdf
|   `-- assignment_requirements_extracted.txt
|-- agents/
|-- handoff/
|-- traces/
|   |-- execution_trace.md
|   |-- hermes_conversation_log.md
|   `-- screenshots/
|-- outputs/
|   |-- final_video.mp4
|   |-- subtitles.srt
|   |-- video_production_design.md
|   |-- image_generation_prompts.md
|   `-- asset_sources.md
|-- asset/
|   |-- s1.png
|   |-- s2.png
|   |-- s3.png
|   |-- s4.png
|   |-- s5.png
|   |-- s6.png
|   `-- 清爽學習節拍.mp3
|-- baseline/
`-- setup/
```

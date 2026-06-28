# Single-Agent Baseline

## Purpose

本檔案作為作業要求的 baseline 比較。Baseline 假設只用一個 prompt 請單一 agent 直接產生 60 秒影片企劃、腳本與分鏡，不再拆成 Planner、Script、Visual、Reviewer 與 Finalizer。

## Baseline Prompt

```text
請幫我製作一支 60 秒的國立臺南大學資訊工程學系形象宣傳影片企劃，內容包含目標觀眾、核心訊息、分鏡、旁白、字幕、素材需求與剪輯方式。影片需適合高中生、新生與一般觀眾觀看。
```

## Baseline Expected Output

單一 agent 通常會一次產生完整企劃，例如：

- 影片主題：國立臺南大學資訊工程學系形象宣傳影片。
- 觀眾：高中生、新生、家長與一般觀眾。
- 結構：開場、系所介紹、學習特色、專題實作、學習氛圍、結尾 CTA。
- 內容：程式設計、AI、資料、系統、網路、團隊合作與專題展示。
- 素材：校園畫面、教室、筆電、白板討論、學生互動、片尾標題。

## Baseline Weaknesses

| 評估項目 | Single-Agent Baseline 問題 |
|---|---|
| 結構完整度 | 可一次產生企劃，但企劃、腳本、分鏡、審查與統整沒有清楚責任分工。 |
| 可追蹤性 | 不容易知道每個決策來自哪個階段，也缺少 agent-to-agent handoff。 |
| 風險檢查 | 容易混入未驗證的官方資訊、成果敘述、Logo 使用或人物肖像風險。 |
| 修正流程 | 若內容有問題，通常只能重新要求單一 agent 改寫，缺少獨立 reviewer feedback。 |
| 低資源完成性 | 可以用一個 prompt 產生初稿，但較難證明受控式 multi-agent workflow。 |

## Multi-Agent Workflow Improvement

本專案將任務拆成 5 個 agents：

1. Planner Agent：定義主題、受眾、scene outline 與素材政策。
2. Script Agent：撰寫旁白與字幕。
3. Visual Agent：規劃分鏡、shot list 與素材需求。
4. Reviewer Agent：檢查長度、真實性、版權、肖像權與安全風險。
5. Finalizer Agent：整合最終腳本、字幕、素材來源與繳交檢核。

因此 multi-agent workflow 在結構、追蹤性、審查能力與符合 PDF 規定方面都比 single-agent baseline 更完整。


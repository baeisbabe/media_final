prompt1
你是本專案的 Coordinator Agent。

請使用繁體中文，為「國立臺南大學資訊工程學系 60 秒形象宣傳影片」建立 zero-paid-token multi-agent workflow。

本專案使用 Hermes Agent 作為 agentic workflow platform，但採用 mock/stub dry-run，不使用 paid API、不使用信用卡、不使用付費 AI 影音生成服務。

請只輸出以下內容：
1. 專案目的
2. 目標觀眾
3. 核心訊息
4. 五個 agents 的名稱
5. 每個 agent 的 role、input、output、constraints

五個 agents 為：
Planner Agent、Script Agent、Visual Agent、Reviewer Agent、Finalizer Agent。

不要建立檔案，不要使用工具，只輸出文字。

prompt2
請繼續 mock/stub dry-run。

現在只模擬 Planner Agent。

請根據以下專案：
「國立臺南大學資訊工程學系 60 秒形象宣傳影片」

輸出有效 JSON，內容包含：
project_title、target_audience、core_message、video_length_seconds、scenes、asset_policy、review_items。

scenes 請規劃 6 個場景，總長 60 秒。
請只輸出 JSON，不要加解釋文字。

prompt3
請模擬 Script Agent。

根據 Planner Agent 的 6 個 scene，產生 60 秒影片的旁白與字幕。

請輸出有效 JSON，包含：
agent_name、input_source、script_style、scenes。

每個 scene 需包含：
scene_id、time_range、narration、subtitle、estimated_seconds。

請使用繁體中文，只輸出 JSON。

prompt4

請模擬 Visual Agent。

根據 Planner 與 Script 的結果，設計每個 scene 的畫面、拍攝素材與 B-roll。

請輸出有效 JSON，包含：
agent_name、input_source、storyboard、asset_folder_plan、shooting_notes。

每個 scene 需包含：
scene_id、time_range、visual_plan、shot_list、needed_assets、risk_notes。

限制：
避免可辨識人物正臉，不拍學生證、帳號密碼、成績、私人聊天，不使用未授權 Logo。

請使用繁體中文，只輸出 JSON。

prompt 5

請繼續剛才的 mock/stub multi-agent dry-run。

現在請重新模擬 Reviewer Agent 與 Finalizer Agent，但這次必須逐一評論每個 scene。

任務一：Reviewer Agent
請根據前面 Planner、Script、Visual Agent 的 6 個 scenes，逐一檢查每個 scene。

每個 scene 都要評論以下項目：
1. scene_id
2. time_range
3. scene purpose 是否清楚
4. narration / subtitle 是否適合
5. visual plan 是否可執行
6. 是否符合 55 至 65 秒影片長度控制
7. 是否符合國立臺南大學資訊工程學系形象宣傳主題
8. 是否有虛構或誇大資訊風險
9. 是否有版權風險
10. 是否有肖像權或隱私風險
11. 修改建議
12. scene_status：pass / revise

最後再給整體審查總結：
- overall_score，1 到 5 分
- main_strengths
- main_issues
- required_revisions
- whether_passed

任務二：Finalizer Agent
請根據 Reviewer Agent 的逐 scene 審查結果，輸出最終修正版影片製作資料。

Finalizer Agent 必須包含：
1. per_scene_revision_plan：逐 scene 修改計畫
2. final_scene_table：最終 6 個 scenes 的時間、畫面、旁白、字幕、素材
3. final_editing_checklist
4. final_asset_source_checklist
5. GitHub submission checklist
6. 明確聲明 Hermes 沒有自動生成 final_video.mp4，final_video.mp4 會由學生依照 shooting plan 使用自製素材與免費剪輯工具手動完成。

請輸出兩個有效 JSON：

第一個 JSON：
檔名建議為 handoff/04_reviewer_feedback.json
根物件名稱為 reviewer_feedback

第二個 JSON：
檔名建議為 handoff/05_finalizer_output.json
根物件名稱為 finalizer_output

請使用繁體中文。
請不要輸出 Markdown 表格。
請不要宣稱影片已經完成。
請不要使用付費 API、信用卡、cloud billing 或付費 AI 影音生成服務。


完整對話內容過程放在hermeslog.txt，該檔案主要為提示對話，handoff裡有輸出內容
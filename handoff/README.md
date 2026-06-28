# Handoff Files

This folder contains the structured handoff evidence for the Hermes Agent multi-agent workflow.

## Clean Submission Handoff

| File | Agent | Purpose |
|---|---|---|
| `01_planner_output.json` | Planner Agent | Project brief, target audience, scene plan and asset policy. |
| `02_script_output.json` | Script Agent | Narration and subtitle plan. |
| `03_visual_output.json` | Visual Agent | Storyboard, shot list, asset folder plan and risk notes. |
| `04_reviewer_feedback.json` | Reviewer Agent | Length, theme, truthfulness, copyright, portrait/privacy and completion review. |
| `05_finalizer_output.json` | Finalizer Agent | Final scene table, editing checklist, asset checklist and submission checklist. |
| `06_final_safe_plan.json` | Finalizer Agent / human cleanup | Safe final plan after filtering raw Hermes output. |

## Raw Evidence

`04_reviewer_feedback.json.txt` and the root PowerShell transcript preserve raw Hermes/mock output. Some raw fragments are not strict JSON because they include transcript text, ellipses or malformed snippets. The clean JSON files above are the normalized submission version.


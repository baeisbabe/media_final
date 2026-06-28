# Image Generation Prompts

These prompts are designed for ChatGPT image generation. Generate images as visual backgrounds or B-roll replacements, then add Chinese titles/subtitles later in Clipchamp. Avoid asking the image model to render Chinese text directly.

## Global Style

Use this style direction for all scenes:

```text
clean modern university promotional video still, bright campus atmosphere, realistic photography style, natural daylight, professional but warm tone, technology learning environment, no official logos, no readable private information, no brand names, no student ID, no passwords, no sensitive screen content, 16:9 aspect ratio, high resolution
```

## Negative Prompt

Use this negative prompt for all scenes:

```text
official logo, school emblem, brand logo, readable personal data, password, API key, student ID, grades, private chat, copyrighted character, celebrity, distorted hands, distorted face, extra fingers, unreadable messy text, watermark, low resolution, blurry, overexposed, dark cyberpunk mood, exaggerated sci-fi, fake ranking, award certificate
```

## Scene 01: Opening Hook

Purpose: 用資訊科技感抓住注意力，但不要過度科幻。

```text
realistic university promotional video still, close-up of a laptop keyboard and code editor on screen with generic non-readable code, soft morning light, subtle campus background blur, a student hand typing but no visible face, clean modern technology learning mood, bright and trustworthy, shallow depth of field, 16:9 aspect ratio, no logos, no readable private information
```

Suggested use: 0-5 秒開場 B-roll。

## Scene 02: Department Positioning

Purpose: 呈現系所定位，可在剪輯時自行加上「國立臺南大學資訊工程學系」文字。

```text
realistic bright university classroom exterior and hallway, open classroom door, students silhouettes in the distance but no recognizable faces, laptops on desks, clean academic atmosphere, warm daylight, space on the upper third for title overlay, professional promotional video still, 16:9 aspect ratio, no logos, no readable text
```

Suggested use: 5-15 秒系所介紹背景。

## Scene 03: Learning Features

Purpose: 呈現程式設計、AI、資料、系統、網路與動手實作。

```text
realistic computer science lab learning scene, laptop screens showing abstract data visualization and generic code blocks without readable text, small electronics board and network cables on desk, students working hands-only or from behind, clean organized workspace, modern university lab, natural light, professional educational promotional style, 16:9 aspect ratio, no logos, no private information
```

Suggested use: 15-30 秒學習特色畫面。

## Scene 04: Project and Teamwork

Purpose: 呈現專題、白板討論、小組協作與 demo。

```text
realistic university student project teamwork scene, group of students seen from side or back discussing around a whiteboard and laptops, whiteboard contains abstract diagrams only, prototype device on table, collaborative and focused atmosphere, bright classroom, no recognizable faces, professional campus promotional still, 16:9 aspect ratio, no logos, no readable personal text
```

Suggested use: 30-45 秒專題與團隊合作。

## Scene 05: Learning Atmosphere

Purpose: 呈現提問、討論、同儕互助與學習氛圍。

```text
realistic warm university learning atmosphere, two or three students discussing a laptop in a classroom or campus corridor, faces turned away or softly obscured, friendly peer support mood, notebooks and laptop on desk, natural daylight, calm and professional educational style, 16:9 aspect ratio, no logos, no readable private information
```

Suggested use: 45-55 秒學習氛圍。

## Scene 06: Closing CTA Background

Purpose: 片尾文字卡背景，文字請在剪輯軟體後製，不要讓 AI 生成中文字。

```text
clean realistic university campus background for ending title card, bright sky, modern campus walkway, soft focus, minimal composition, large empty space in the center for text overlay, warm professional promotional tone, 16:9 aspect ratio, no logos, no readable text, no people close-up
```

Suggested use: 55-60 秒結尾 CTA。

## Optional Cover Image

Purpose: GitHub README 或報告封面用。

```text
realistic modern computer science education promotional cover, university campus blended with laptop, abstract data visualization, whiteboard sketches and teamwork atmosphere, bright clean composition, professional academic tone, no logos, no readable text, no recognizable faces, 16:9 aspect ratio, high resolution
```

## Asset Source Note

After generating images, record each image in `outputs/asset_sources.md`:

- tool name: ChatGPT
- prompt or prompt file reference
- generation date
- license or terms URL
- output filename
- whether it is AI-generated

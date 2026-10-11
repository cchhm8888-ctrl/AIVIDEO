---
name: video-breakdown-to-brief
description: "Use when a creator develops an AIGC video from a reference or brief: story, four-beat script, shots, spatial blocking, assets, Style DNA, timecoded prompts, animatic, or shot-generation planning and review."
metadata:
  short-description: 从拉片或选题生成故事、分镜、资产、动态镜头与制作记录
---

# Video Breakdown to AIGC Production

Help a creator move from **reference evidence or a new brief** to an original, executable AIGC video package. Build the story before prompts: story premise → story script → four-beat production script → shots → assets → prompts → animatic → dynamic-shot production → continuity.

Default to Chinese when the user writes in Chinese. Match another language when requested.

## Choose one working mode

Choose from the request; ask only when the mode materially changes the result.

1. **只做拉片** — analyze a supplied video and stop after evidence and transferable methods.
2. **拉片后做项目** — use verified methods from a supplied video to develop the creator's own project.
3. **生成新脚本** — start from the creator's topic, audience, material, and constraints; no reference video is required.
4. **W03 内容输出辅助 / Style Skill** — start from confirmed project materials (prefer an approved W02 snapshot) and turn useful visual methods into compact rules and a reusable Skill.
5. **动态镜头制作 / W05** — use approved shot, camera, asset, and keyframe materials to plan generation modes, motion prompts, candidate comparison, failure repair, and an editable shot package.

For modes 2 and 3, read [story development](references/story-development.md) and [the production worksheet](references/worksheet-schema.md) before drafting a package. For mode 4, read [the W03 Style Skill flow](references/w03-style-skill-flow.md) and the worksheet sections it points to. For mode 5, read [dynamic-shot production](references/w05-dynamic-shot-production.md) and the corresponding worksheet sections; if approved inputs are missing, identify the missing shot, camera, or keyframe material. For mode 1, read the worksheet when a detailed evidence or production report is requested.

## Protect evidence and authorship

When a reference video is used, mark non-trivial conclusions as:

- **画面可见** — directly visible or audible; include a timecode or clear scene cue.
- **分析判断** — an interpretation supported by visible or audible evidence.
- **资料缺失** — not available in the supplied video or sources.

Do not infer prompts, seeds, model versions, generation parameters, lenses, author intent, budget, rights, or backstage workflow from a finished video. Do not turn a reference video's characters, plot, world, brand assets, shot order, or recognisable visual signature into the creator's project. Transfer a method, not the surface.

If a required external fact is unknown, write **缺少资料**. In a new original project, a proposed character, setting, prop, or visual choice may be labelled **创作设定待确认**; it becomes a **固定锚点** only after the creator accepts it.

## Break down a reference in three passes

### First viewing: attention and feeling

Record three changes in attention or feeling and one moment worth revisiting. Describe the experience before explaining it.

### Second viewing: image and sound evidence

Build a selected evidence table. Every row needs a timecode or scene cue, what is seen or heard, the image/space/sound relationship, narrative function, and a relevant continuity or production question. Use tentative language for uncertain technical labels.

### Third viewing: transferable decisions

Separate method from surface. Write each useful finding as:

`source evidence → transferable method → creator's own material → intended story effect`

When developing a story from a reference, transfer only rhythm, information delay, conflict design, contrast, hook placement, or sound/image relationships. Do not transfer the reference's plot or characters.

## Build the AIGC video package in order

Do not jump from a theme to polished prompts. Complete each stage with a visible result, then use it as input to the next.

### 1. Confirm the project brief

Capture audience and viewing situation, observable problem, protagonist's immediate goal, obstacle, accessible people/places/objects/sounds, visible ending change, duration and format, and practical or rights limits.

### 2. Develop the story before the screenplay

Use the step-by-step method in [story development](references/story-development.md):

1. choose the source route — transferable method from a breakdown or a creator's own topic;
2. identify a person, immediate want, obstacle, cost, and visible choice;
3. write and check one story sentence;
4. design empathy, contrast, conflict points, and emotional hooks;
5. draw the two curves — **龙骨曲线** for story pressure and **砖瓦曲线** for emotional movement;
6. draft the story script as a causal sequence;
7. map the approved story script into four beats.

The one-sentence story must make a viewer care through a concrete want, a cost or loss, and a meaningful choice. It must include at least one contrast between expectation and reality, or between an outer action and inner feeling. Do not use abstract labels such as “healing” or “growth” as the event itself.

### 3. Write the four-beat production script

Use four linked beats:

1. **建立** — establish person, space, routine, and what is normal.
2. **触发** — introduce an event that makes the goal harder or forces attention.
3. **转变** — show a choice or action that changes the relationship or situation.
4. **余韵** — leave a visible or audible result after the action.

For every beat, state scene, goal, conflict, visible action, information given to the viewer, sound task, and visible/audible change. The trigger must cause the turn; the ending must prove a real change rather than announce a theme.

### 4. Turn the four beats into 6–10 shots

Unless the creator specifies another structure, make 6–10 shots for a 30–60 second video. Every shot must belong to one beat and give the viewer one clear piece of information. Record shot ID, start–end timecode and duration, beat, framing and camera relationship, screen action, information function, movement, sound, required assets, continuity anchor, and risk/check. The shot count is a production budget, not a target to fill with decorative images.

### 5. Plan space and camera blocking

Before writing keyframe or video prompts, make a platform-neutral spatial plan for every important scene. First lock the scene landmarks, entrances and exits, subject / prop positions, facing directions, action paths and light direction; then place cameras according to the information function of each shot. A camera position is not the same thing as a shot size: the position explains where the viewer is, while the shot size explains the relationship to the subject.

For each scene, include a compact text layout when spatial relations matter:

```text
场景 SPACE_01 俯视排布（文字示意）
北 / 入口：
地标：墙面、窗、展台、桌面……
CHAR_01 起点 → 行动路径 → 终点：
PROD_01 / PROP_01 初始位置与状态：
CAM_K1（建立）：位置 / 朝向 / 看到的地标
CAM_K2（触发）：位置 / 朝向 / 视线关系
CAM_K3（转变）：位置 / 朝向 / 运动方向
CAM_K4（余韵）：位置 / 朝向 / 结尾构图
光线方向：
```

For every camera, state its camera ID, position or side of the space, height / angle when relevant, subject eyeline, screen direction, framing, movement, and the landmark that keeps the next shot orientated. Keep this plan separate from the final prompt text so it can be revised without changing the story.

### 6. Build assets and write prompts

Extract only assets needed by the approved story and shots. Give every recurring asset a stable ID and a concrete type, such as `CHAR_01`, `PROD_01`, `PROP_01`, `TOOL_01`, `SPACE_01`, `ENV_01`, `MAT_01`, or `REF_01`. Do not hide a required asset inside a generic “scene” prompt.

For each required asset, first write a compact asset specification, then write its asset-image prompt. For scene assets, select only the views required by the shots; possible views include a base establishing view, subject reverse eyeline / level view, 45° high-angle oblique wide view, and 90° vertical top-down view. Do not generate all four by default. The specification must state:

- **人物角色** — role in the story, age range or appearance only when observable/needed, body/face/hair/clothing, expression baseline, permitted action range, and continuity locks;
- **产品/主体** — exact product identity, shape, parts, material, scale, orientation, use state, and which supplied reference image is authoritative; preserve geometry and do not invent specifications;
- **道具与刀具** — object type, function in the action, size/hand relationship, material, wear/state, safe handling, and whether it is merely a visual prop or a cutting tool; never add a knife/tool unless the story or shot requires it;
- **场景/空间** — location type, layout, surfaces, entrances/exits, background density, spatial relation to the subject, and what must not appear;
- **环境条件** — time, weather, air/particles, ambient color, practical light sources, sound-relevant conditions, and continuity across shots;
- **材质/工艺/参考板** — only when the story needs evidence of texture, craft, or a visual-system reference.

Every asset-image prompt must include the asset ID, subject and function, composition, camera distance or view, material/appearance, light and color, background/space, continuity requirements, and a concise negative prompt. For product assets, explicitly say `结构以参考图为准` when a reference image is supplied. For character assets, specify a repeatable identity sheet rather than a one-off pose. For tools or knives, describe only the required tool and its safe, non-graphic use context.

Produce three prompt levels when the requested package includes them:

- **asset-image prompts** — one prompt per required character, product, prop/tool, scene/space, environment condition, material, or reference sheet;
- **four-beat visual prompts** — one prompt for 建立、触发、转变、余韵, defining what must be readable across that section and referencing the relevant asset IDs;
- **keyframe prompts** — one prompt for each generated or selected timeline state, with a project timecode, Shot ID, camera / spatial relation, asset IDs, visible change, and handoff;

- **per-shot video prompts** - one prompt for every approved shot, referencing stable asset IDs and specifying that shot's start-end timecode, duration, action, space, framing, movement, light, sound intention, and continuity handoff.

Do not add model-specific syntax unless the creator names a platform and requests it. Do not generate asset categories that the story does not use. If a required identity, product detail, location, or environment condition is unknown, mark it `创作设定待确认` or `资料缺失` instead of guessing.

### 7. Timecoded keyframes and animatic specifications

Use one project timeline for the new video. Every shot has a start–end timecode and duration; every keyframe prompt has a project timecode and a `Shot ID`. Do not mix these with timecodes from a reference video: reference timecodes belong only in the evidence table.

For each shot that needs a generated or selected keyframe, record:

| Keyframe ID | Project timecode | Shot ID / beat | State to hold | Camera / spatial relation | Asset IDs | Visible change | Continuity handoff | Negative |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| KF-K1-A | 00:00–00:05 | K1 / B1 |  |  |  |  |  |  |

The keyframe prompt must name the stable asset IDs, timecode, state, camera position or view, scene landmarks, light direction, and the one change that the frame needs to make readable. A keyframe is a state on the timeline, not a second story beat.

Default dynamic previsualization is a specification, not a rendered video file. Describe the keyframe order, seconds per frame, simulated pan / tilt / push / pull or hold, temporary sound intention, transition, and the silent-viewing check. Create an actual animatic only when the creator explicitly asks for a video file.

| Time range | Shot / keyframe | Hold / simulated movement | Temporary sound layer | Transition / handoff | Silent read check |
| --- | --- | --- | --- | --- | --- |
| 00:00–00:05 | K1 / KF-K1-A |  |  |  |  |

### 8. Produce dynamic shots when requested

When the creator asks to move beyond the animatic, apply [dynamic-shot production](references/w05-dynamic-shot-production.md). For each selected shot, choose text-to-video, image-to-video, or start/end-frame generation from the available inputs and the required change. Carry the approved Shot ID, project timecode, camera position, asset IDs, and identity/space/light anchors into the motion prompt. Separate subject action, camera movement, and environment response; specify the starting and ending states and one primary movement.

Plan a comparable baseline only when generation or testing is requested. If actual candidate clips are supplied or generated, inspect the middle as well as the first and last frames, record the visible failure and the smallest useful correction, and select a usable segment or simpler replacement. Keep version, prompt, input frames, settings actually used, result, and a backup candidate where available. Do not claim a candidate passed inspection without seeing it, invent platform settings or costs, or generate paid/external clips merely because the planning section is present.

## W03 content-output extension

When the user asks for W03, visual consistency, Style DNA, Style Grammar, Style Skill, or help applying a visual method to video content, read [the lightweight W03 flow](references/w03-style-skill-flow.md). This is a visual-rule layer on top of the confirmed story and production materials, not a second independent production workflow.

Use four short passes:

1. **提取** — select only 3–5 useful Style DNA dimensions from a reference, product image, or existing result;
2. **转译** — turn evidence into `Must Keep / Can Change / Negative` rules and stable subject, space, and light anchors;
3. **调用** — add the same rules to the content the user actually requested: story, four-beat script, shot table, spatial plan, asset prompts, four-beat visual prompts, keyframe prompts, animatic specification, or per-shot video prompts;
4. **检查** — report only relevant continuity problems as `问题 → 证据 → 最小修改 → 需要重写的行`.

Do not automatically generate a full Visual Bible or four-shot test. Add those only when the user asks for them or when a high-risk consistency problem requires a small test. Keep W02 story, characters, products, content variables, and spatial geometry intact; W03 controls visual language, while asset and space plans control identity, positions, and geometry. Never use an artist's name as a replacement for a rule, copy a reference film's surface, or invent timecodes, prompts, model settings, rights, or production facts.

For the required asset inventory and asset-image prompt fields, read [asset prompt schema](references/asset-prompt-schema.md) when the current request needs concrete character, product, prop/tool, scene, environment, material, or reference-sheet assets.

For a W03 Skill export, the minimum useful result is: one-line visual direction, 3–5 Must Keep rules, Can Change variables, 3–5 Negative rules, subject / product, space, and light anchors, plus a reusable prompt template. Keep final prompts in the requested prompt sections rather than duplicating them inside the rule summary.
### 9. Audit and revise

Check story causality, contrast, empathy, curve logic, hooks, screen direction, eyelines, entrances/exits, prop state, character identity and costume, location geometry, light/weather/time, action handoff, and sound bridges. Report:

`状态（可用 / 需修改 / 缺资料） → 依据 → 最高优先级问题 → 可选修改方案 → 需要更新的故事表、脚本表或提示词`

Fix deterministic internal inconsistencies before first delivery. Do not overwrite creative choices such as conflict, ending, or visual direction without the creator's confirmation. Preserve the original row and log the accepted change.

## Required outputs

For a complete AIGC project, return these linked sections in order:

1. 项目命题卡
2. 故事来源与方法迁移卡（拉片路径时）或选题拆解卡（自主选题路径时）
3. 一句故事法、共情点与反差设计
4. 双曲线、情绪钩子与冲突点表
5. 故事剧本表
6. 四拍脚本表
7. 6–10 镜头分镜表
8. 空间调度与机位文字排布
9. 资产清单
10. 资产图提示词表
11. 四拍视觉提示词表
12. 关键帧提示词表（含项目时间码）
13. 逐镜视频提示词表（含项目时间码）
14. 动态预演规格
15. 连续性检查与修订日志

When the creator also requests dynamic-shot production, append the relevant generation-mode decisions, motion prompts, candidate comparison or actual-result review, repair decisions, and shot-package manifest. A preproduction request stops at the requested stage; do not append speculative generation results.

Do not substitute a prose summary for the tables. Story nodes, beat IDs, shot IDs, and asset IDs must match across them.

For W03 content-output mode, return only the requested content plus the compact visual-rule layer described in the W03 reference.

## Shot-table output format

After the four-beat script is approved, include a separate shot table before prompt generation. Output one row per shot, keeping the same shot IDs and beat IDs used by the storyboard and prompts. Use this column order:

| Shot ID | Duration | Visual description | Shot size | Lighting / mood | Dialogue / voiceover | Sound effects | Camera movement |
| --- | --- | --- | --- | --- | --- | --- | --- |
| K1 |  |  |  |  | no dialogue / voiceover |  |  |

For no-dialogue projects, write `无台词` in the dialogue / voiceover column and still describe the sound task. Keep final prompts in the per-shot video prompt table; do not repeat them in the shot table and do not add an operation column. The table may be Markdown or a scrollable structured table when it is long.
End with one concrete next production action based on the current package, such as confirming the story sentence, locking the spatial plan, approving the asset sheet, checking the first keyframe timecode, or resolving the highest-risk continuity handoff.

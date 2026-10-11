# AIGC video development worksheet

Use the sections that match the chosen mode. Keep beat, shot, and asset IDs stable across every table.

## Information status

Use these statuses consistently:

- **已确认** — supplied or explicitly accepted by the creator.
- **创作设定待确认** — an original design proposal created for a new script; it is not an external fact.
- **固定锚点** — a creative setting the creator has accepted and that must remain continuous.
- **缺少资料** — an unknown external fact, rights condition, production condition, platform requirement, or requested input.

In `生成新脚本` mode, character appearance, costume, prop design, palette, and location layout may be proposed as **创作设定待确认**. Never present these as facts about a real person, place, brand, production, or reference video. After acceptance, promote them to **固定锚点**.

## 1. Project intake

| Field | Confirmed input | Status / source |
| --- | --- | --- |
| Working title |  | 已确认 / 创作设定待确认 / 缺少资料 |
| Mode | 只做拉片 / 拉片后做项目 / 生成新脚本 |  |
| Audience and viewing situation |  |  |
| Observable problem |  |  |
| Protagonist's immediate goal |  |  |
| Obstacle or pressure |  |  |
| Accessible people, places, objects, sounds |  |  |
| Desired visible ending change |  |  |
| Duration, ratio, sound, deliverables |  |  |
| Dialogue policy | dialogue / voiceover / no dialogue / non-verbal voice only |  |
| Practical and rights limits |  |  |

## 2. First viewing card

Use only when a reference video is supplied.

```markdown
### First viewing
- Source / version:
- Running time:
- Three changes in my attention or feeling:
  1.
  2.
  3.
- One moment I want to revisit:
- Why I want to revisit it:
```

## 3. Evidence table

Every row needs a timecode or clear scene cue. `Evidence level` is `画面可见`, `分析判断`, or `资料缺失`.

| Time / cue | Evidence level | What is seen or heard | Image, space, or sound relation | Story function | Continuity or production question |
| --- | --- | --- | --- | --- | --- |
|  | 画面可见 |  |  |  |  |

## 4. Transfer cards

| Source evidence | Transferable method | Do not copy | Creator's own material | Intended story effect |
| --- | --- | --- | --- | --- |
|  |  | characters, plot, setting, brand assets, signature image |  |  |

## 5. Project brief

```markdown
### 项目命题卡
- 受众与观看情境：
- 观众要看懂的问题：
- 主角此刻想完成什么：
- 什么正在阻碍他 / 她：
- 现有真实材料：
- 结尾能看见或听见的变化：
- 一句话概念：用【人物 / 材料】在【场景】中完成【动作与选择】，让【受众】看见【变化】。
- 形式与时长：
- 对白规则：
- 限制：
- 创作设定待确认：
- 缺少资料：
```

## 6. Four-beat script table

The four rows form one causal chain. Do not use four unrelated attractive scenes.

| Beat ID | Beat | Time range | Scene | Immediate goal | Conflict / pressure | Visible action | Information for viewer | Sound task | Visible or audible change |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| B1 | 建立 |  |  |  |  |  |  |  |  |
| B2 | 触发 |  |  |  |  |  |  |  |  |
| B3 | 转变 |  |  |  |  |  |  |  |  |
| B4 | 余韵 |  |  |  |  |  |  |  |  |

### Four-beat check

- B2 directly disrupts the state established in B1: 可用 / 需修改 / 缺资料
- B3 is an observable decision or action caused by B2: 可用 / 需修改 / 缺资料
- B4 preserves a visible or audible result of B3: 可用 / 需修改 / 缺资料
- The full change fits the confirmed duration: 可用 / 需修改 / 缺资料
- Each beat has at least one assigned shot: 可用 / 需修改 / 缺资料

## 7. 6–10-shot storyboard table

Use 6–10 rows unless the creator confirms another count. Every shot provides one primary piece of information.

| Shot ID | Time range / duration | Beat ID | Shot size and camera relation | Visible action | Information function | Movement | Sound | Asset IDs | Continuity anchor | Risk / check |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| K1 |  | B1 |  |  |  |  |  |  |  |  |
| K2 |  |  |  |  |  |  |  |  |  |  |
| K3 |  |  |  |  |  |  |  |  |  |  |
| K4 |  |  |  |  |  |  |  |  |  |  |
| K5 |  |  |  |  |  |  |  |  |  |  |
| K6 |  |  |  |  |  |  |  |  |  |  |

Add K7–K10 only when they have distinct information functions.

### Timeline check

- Sum of shot durations equals the confirmed total duration: 可用 / 需修改 / 缺资料
- Shot time ranges have no overlap and no unexplained gap: 可用 / 需修改 / 缺资料
- Every B1–B4 beat owns at least one shot: 可用 / 需修改 / 缺资料
- Spatial plan, camera IDs, and selected scene views cover every shot that needs them: 可用 / 需修改 / 缺资料
- Keyframe project timecodes match the shot table and have no overlap: 可用 / 需修改 / 缺资料
- Animatic specification covers the full confirmed duration: 可用 / 需修改 / 缺资料

When the creator specifies 45 seconds, the shot durations must total exactly 45 seconds.

### 7a. Compact production shot table

When the shot list is shown in a review interface, also render this eight-column table before the prompt sections:

| 镜号 | 时长 | 画面描述 | 景别 | 光影氛围 | 对白·旁白 | 音效 | 运镜 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| K1 |  |  |  |  | 无台词 / 待确认 |  |  |

Use one row per approved shot. Keep final prompts in section 11, not in this table, and do not add an operation column. Keep shot IDs and durations identical to the 6–10-shot storyboard table.
## 7b. Spatial staging and camera plan

Use a platform-neutral text plan before prompt generation whenever a scene has more than one subject, a meaningful entrance / exit, or a camera move. Keep geometry and identity in the plan; keep style rules in W03.

```text
场景 SPACE_01 俯视排布（文字示意）
入口 / 出口：
地标：
CHAR_01 起点 → 路径 → 终点：
PROD_01 / PROP_01 位置与状态：
CAM_K1：位置 / 朝向 / 高度 / 看到的地标
CAM_K2：位置 / 朝向 / 高度 / 看到的地标
光线方向：
```

| Camera ID | Shot ID | Position / height | Facing / eyeline | Shot function | Framing / movement | Landmark kept in view |
| --- | --- | --- | --- | --- | --- | --- |
| CAM_K1 | K1 |  |  | 建立 |  |  |

## 8. Asset manifest

Use stable IDs. `Fixed anchors` must remain identical unless the script explicitly changes them.

| Asset ID | Type | Name / function | Fixed continuity anchors | State changes by beat or shot | Needed views / files | Status / source / rights |
| --- | --- | --- | --- | --- | --- | --- |
| CHAR_01 | character |  | face, hair, costume, age range |  | front / side / full body | fixed / pending / missing |
| SPACE_01 | location |  | layout, entrances, windows, key light |  | exterior / interior / plan | fixed / pending / missing |
| PROP_01 | prop |  | shape, material, color |  | clean / changed state | fixed / pending / missing |
| LOOK_01 | visual system |  | palette, contrast, texture, weather |  | reference board | fixed / pending / missing |

### Scene view selection (adaptive)

Choose only the views that a scene actually needs. Available view types are: `基准场景全景`, `对象反向回视平望`, `45°俯视斜角全景`, and `90°垂直正俯上帝视角`. The selected view set must cover the approved shots and preserve the same entrances, landmarks, subject positions, screen direction, and light direction. Do not generate all four views by default.

| Scene ID | Governing shots | Selected views | Shared spatial anchors | Missing view / input |
| --- | --- | --- | --- | --- |
| SPACE_01 | K1–K4 |  |  |  |

## 9. Asset-image prompt table

One row generates an asset or neutral reference sheet, not a whole story beat.

| Prompt ID | Asset ID | Intended image | Platform-neutral prompt | Negative / exclusions | Confirmed ratio / use | Missing input |
| --- | --- | --- | --- | --- | --- | --- |
| A-CHAR-01 | CHAR_01 | character reference sheet |  | no brand, no text, no extra person | confirmed ratio / reference |  |
| A-SPACE-01 | SPACE_01 | location reference |  | no readable logo, preserve entrances | confirmed ratio / reference |  |
| A-PROP-01 | PROP_01 | prop state sheet |  | no unrelated decoration | confirmed ratio / reference |  |

If the ratio is not supplied, write `缺少资料`; do not copy an example ratio into the project.

### Platform-neutral asset prompt pattern

```text
[asset ID and intended use], [confirmed fixed anchors or creative settings pending confirmation],
[required neutral view or state], [environment and light when relevant],
[readable material details], [confirmed composition / aspect ratio],
exclude: [brand marks, copyrighted characters, text artifacts, continuity violations, unconfirmed external facts].
```

## 10. Four-beat visual prompts

Each prompt states what the viewer must read across that beat and names the shots it governs.

| Beat ID | Governing shots | What must be readable | Platform-neutral visual prompt | Continuity anchors | Do not add |
| --- | --- | --- | --- | --- | --- |
| B1 建立 |  |  |  |  |  |
| B2 触发 |  |  |  |  |  |
| B3 转变 |  |  |  |  |  |
| B4 余韵 |  |  |  |  |  |

## 10a. Timecoded keyframe prompt table

Every generated or selected keyframe gets a project timeline timecode and a Shot ID. A reference video timecode must never be substituted for a new-project timecode.

| Keyframe ID | Project timecode | Shot ID / beat | State to hold | Camera / spatial relation | Asset IDs | Visible change | Continuity handoff | Negative / exclusions |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| KF-K1-A | 00:00–00:05 | K1 / B1 |  |  |  |  |  |  |

### Platform-neutral keyframe prompt pattern

```text
[keyframe ID, project timecode, shot ID / beat]. Use [asset IDs and fixed anchors].
State: [the single readable state at this timecode].
Camera / space: [camera position, eyeline, framing, landmark and direction].
Light / material: [confirmed light, weather and material rules].
Change: [one visible change this frame must establish or hold].
Handoff: [last pose, prop state and screen direction for the next shot].
Exclude: [identity drift, geometry changes, extra people, text artifacts, unconfirmed facts].
```

## 11. Per-shot video prompt table

Every approved shot receives its own prompt. Reuse the exact IDs and fixed anchors from the asset manifest.

| Prompt ID | Shot ID / beat | Asset references | Starting state | Action and visible change | Framing / camera / space | Light, weather, material | Sound intention | Duration / handoff | Negative / exclusions |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| V-K1 | K1 / B1 |  |  |  |  |  |  |  |  |

### Platform-neutral shot prompt pattern

```text
[shot ID, beat ID, start-end timecode, duration]. Use [asset IDs and fixed anchors].
Start: [confirmed starting state and spatial relationship].
Action: [one concrete action] causes [one visible change].
Camera: [framing, camera-to-subject relation, movement only if meaningful].
Environment: [confirmed space, light, weather, materials].
Sound intention: [human / environment / music function; write none when absent].
End handoff: [last pose, prop state, screen direction, sound bridge into next shot].
Exclude: [identity drift, costume drift, prop-state errors, geometry changes, extra people,
unreadable text, brand marks, unconfirmed external facts].
```

Do not add model-specific commands, seeds, lenses, or settings unless the creator confirms the target platform and asks for them. Unless explicitly requested, output no prompt variants, direction alternatives, or variable-test matrix.

## 11a. Dynamic previsualization specification

Default output is a specification for a 30–60 second animatic, not a rendered video file. Record the keyframe order, hold duration, simulated pan / tilt / push / pull, temporary sound intention, transition, and silent-viewing result.

| Time range | Shot / keyframe | Hold / simulated movement | Temporary sound layer | Transition / handoff | Silent read check |
| --- | --- | --- | --- | --- | --- |
| 00:00–00:05 | K1 / KF-K1-A |  |  |  |  |

Only create an actual animatic file when the creator explicitly requests it and the required keyframes are available.

## 11b. Dynamic-shot generation plan (when requested)

Use [dynamic-shot production](w05-dynamic-shot-production.md). Fill one row per shot selected for generation. `Project timecode` must match the approved storyboard; an input frame is identified by its real file or keyframe ID. Leave platform and settings as `待选` until chosen by the creator or recorded from an actual run.

| Shot ID / beat | Project timecode / duration | Camera ID / space | Input frame IDs | Mode and reason | Subject start → end | Dominant motion / environment response | Motion prompt | Fixed anchors / exclusions | Platform / settings status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| K1 / B1 |  |  |  | 文生 / 图生 / 首尾帧 |  |  |  |  | 待选 / 已确认 |

### Candidate review (only after clips or sampled frames exist)

`Clip-local range` describes the usable portion of the generated file. It is distinct from the project's placement timecode. Do not mark an unseen result as inspected.

| Shot ID | Candidate / file | Input / prompt version | Actual platform / model / settings | Clip-local usable range | Start / middle / end evidence | Identity / action / background / camera | Defect and affected time | Selection / reason |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| K1 |  |  |  |  | 待检查 / 已检查 |  |  |  |

### Repair and comparison log

Use this only for an observed defect or a requested comparison. Hold the other relevant conditions steady when changing one factor. Record actual costs and generation time only when known.

| Shot / candidate | Observed problem / time | Changed factor | New candidate / evidence | Result | Decision: use segment / revise / replace / edit |
| --- | --- | --- | --- | --- | --- |
|  |  |  |  | 待检查 / 可用 / 仍有问题 |  |

### Shot-package manifest

| Shot ID / project placement | Selected clip / clip-local range | Backup clip | Input frames | Prompt and recorded settings | Review / repair record | Source / rights status | Remaining gap |
| --- | --- | --- | --- | --- | --- | --- | --- |
| K1 /  | 未生成 / 文件路径 | 无 / 文件路径 |  |  |  | 已确认 / 缺少资料 |  |

If the creator asks only for planning, return the generation plan and a planned manifest. Candidate review, repair outcomes, and final clip selection require real results.

## 12. Continuity audit

| Check | Status | Evidence / affected IDs | Highest-priority problem | Optional fixes | Update target |
| --- | --- | --- | --- | --- | --- |
| Story causality across B1–B4 | 可用 / 需修改 / 缺资料 |  |  |  | beat table |
| Total duration and timeline coverage |  |  |  |  | storyboard / prompts |
| Character identity and costume |  |  |  |  | asset / shot prompts |
| Location geometry and entrances |  |  |  |  | asset / storyboard / spatial plan |
| Screen direction, eyeline, entrance / exit |  |  |  |  | storyboard / shot prompts |
| Prop state and action handoff |  |  |  |  | asset / shot prompts |
| Light, weather, and time |  |  |  |  | asset / beat / shot / keyframe prompts |
| Sound task and bridge |  |  |  |  | four-beat / storyboard |
| Dialogue policy |  |  |  |  | storyboard / prompts |
| Keyframe timecodes and animatic timing |  |  |  |  | keyframe / animatic specification |
| Rights and platform constraints |  |  |  |  | prompt exclusions |

If the project is `无台词`, every shot must contain no dialogue, narration, or intelligible language. Record whether non-verbal breath, effort sounds, crowd murmur, and background announcements are allowed.

Fix deterministic internal inconsistencies before the first delivery when doing so does not change the story choice. Ask the creator before changing a character decision, conflict, ending, visual direction, or other creative choice.

## 13. Revision log

Keep the original when a creative choice requires creator confirmation.

| Version | Problem | Evidence / affected IDs | Options offered | Creator decision | Revised row or prompt | Reason |
| --- | --- | --- | --- | --- | --- | --- |
| v01 |  |  |  | 采纳 / 不采纳 / 待确认 |  |  |

## 14. Delivery check

```markdown
- 项目命题卡、四拍、镜头、资产和提示词属于同一个项目：可用 / 需修改
- 每一拍都有可见或可听见的变化，并至少对应一个镜头：可用 / 需修改
- 每个镜头都有唯一的信息功能：可用 / 需修改
- 镜头时长总和等于确认总时长，时间轴无重叠、无无故空档：可用 / 需修改
- 每个重复出现的人物、场景和道具都有稳定资产 ID：可用 / 需修改
- 四拍提示词与逐镜提示词覆盖全部 B1–B4 和 K1–K6（及已确认的 K7–K8）：可用 / 需修改
- 对白、人声和字幕符合项目规则：可用 / 需修改
- 未知外部事实已标为“缺少资料”，原创设计已标为“创作设定待确认”或“固定锚点”：可用 / 需修改
- 没有未经请求的提示词变体、方向方案或变量测试矩阵：可用 / 需修改
- 连续性问题已经定位到具体表格行或提示词：可用 / 需修改
- 下一项制作动作：
```

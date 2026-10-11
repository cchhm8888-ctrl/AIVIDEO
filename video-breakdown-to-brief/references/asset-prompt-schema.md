# Asset Prompt Schema

Use this reference when a requested video package includes asset-image prompts. The goal is to make every visible dependency explicit and reusable across shots.

## 1. Asset inventory fields

| Field | Required content |
|---|---|
| Asset ID | Stable ID such as `CHAR_01`, `PROD_01`, `PROP_01`, `TOOL_01`, `SPACE_01`, `ENV_01`, `MAT_01`, `REF_01` |
| Type | 人物角色 / 产品 / 道具 / 刀具 / 场景空间 / 环境条件 / 材质工艺 / 参考板 |
| Story function | What this asset does in the story or shot; do not write only a visual label |
| Identity locks | Shape, parts, face/hair/clothes, size, material, color, state, or geometry that must stay unchanged |
| Allowed changes | Framing, pose, angle, background density, time, weather, or other variables that may change |
| Source | Supplied image, approved project detail, or `创作设定待确认` / `资料缺失` |
| Prompt | Complete asset-image prompt using the fields below |
| Negative | Short exclusions specific to this asset |
| Spatial anchors / view set | For scene assets, selected views and landmarks that must remain aligned across shots |

## 2. Asset-image prompt order

Write prompts in this order so they can be reused by image and video models. For a scene asset, add only the view(s) required by the shot plan:

`[Asset ID + type] → [story function] → [subject identity and geometry] → [pose/state/use] → [composition and selected view] → [material/appearance] → [space/background] → [light/color] → [continuity locks] → [negative prompt]`

## 3. Type-specific requirements

### 人物角色

State role, approximate age range only when needed, face/hair/body/clothing, expression baseline, allowed actions, camera-facing limits, and the identity details that must be repeated in every shot. Avoid defining a one-off pose as the character identity.

### 产品/主体

State exact name, silhouette, parts, material, scale, orientation, use state, and authoritative reference. Add `结构以参考图为准` when an image is supplied. Never invent specifications, logos, stones, mechanisms, or colorways.

### 道具与刀具

State object/tool type, action function, size relative to the hand/body, material, wear/state, safe non-graphic handling, and whether a blade is actually required. Do not introduce a knife, weapon, or cutting action because it looks cinematic; it must come from the story or shot.

### 场景/空间

State location type, layout, surfaces, entrances/exits, subject-to-space relationship, background density, and forbidden elements. For continuity, define which walls, windows, counters, pedestals, or horizon lines repeat.

### 环境条件

State time, weather, air/particles, ambient color, practical light sources, visibility, and sound-relevant conditions. Keep these compatible with the approved story and with adjacent shots.

### 材质/工艺/参考板

Use only when texture, craft, or visual method is part of the story. State the evidence to show (for example, raw stone grain, polished metal edge, hand-setting motion) and what should not be inferred from it.

## 4. Scene view selection (adaptive)

Select views from the shot and spatial plan rather than generating a fixed bundle. Available choices are `基准场景全景`, `对象反向回视平望`, `45°俯视斜角全景`, and `90°垂直正俯上帝视角`. Use the minimum set that covers the approved camera positions. Every selected view must repeat the same entrances, landmarks, subject positions, screen direction, and light direction.

## 5. Timecoded keyframe prompt fields

| Field | Required content |
|---|---|
| Keyframe ID | Stable ID such as `KF-K1-A` |
| Project timecode | Start–end time or exact point on the new video's timeline |
| Shot / beat | Exact `Shot ID` and `Beat ID` from the approved tables |
| State | One readable pose, prop state, or product state at this timecode |
| Camera / space | Camera position, eyeline, framing, landmark, and screen direction |
| Handoff | Last state that must match the next keyframe or shot |
| Negative | Identity, geometry, extra-person, text, or unconfirmed-fact exclusions |

Do not use a reference video's timecode as the new project's timecode. Keep keyframe prompts separate from asset-image prompts: the former describes a timeline state, while the latter describes a reusable asset or neutral reference sheet.

## 6. Minimal example

**Asset ID**: `PROD_01`  
**Type**: 产品  
**Function**: 片尾独立进入光池，完成产品与人物观看关系的反转。  
**Source**: supplied product image.  
**Prompt**: `PROD_01 AURORA 极光项链，黑色高级珠宝展示空间，产品结构以参考图为准，白金叶片链节与中央垂坠保持原比例和连接方式，完整可见，三分之四正面产品视图，石墨灰台面，冷白窄束侧光切出金属边缘，背景近黑并保留负空间，真实钻石反射，作为片尾独立产品证据，连续性锁定链节、垂坠、材质、尺寸关系；不要重新设计。`  
**Negative**: `不要改变结构，不要增加宝石或 Logo，不要变形、漂浮、穿模、文字、价格、UI。`


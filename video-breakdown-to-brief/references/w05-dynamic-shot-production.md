# Dynamic-shot production from an approved animatic

Use this reference when the creator asks to turn approved shots or keyframes into moving video, to compare generated candidates, or to organize usable clips. It extends the existing story, shot, spatial, asset, Style DNA, and timecoded prompt tables. Keep their IDs and approved creative decisions.

## 1. Select the generation input per shot

Start with the shot's information function and the frames already available. Record the choice and reason; do not prescribe one mode for an entire project.

| Mode | Use when | Check before generation |
| --- | --- | --- |
| 文生视频 | Exploring a shot without a locked image or visual identity | Describe the space and identity anchors explicitly; expect more variation. |
| 图生视频 | An approved frame should retain its subject, composition, product geometry, and spatial relationships | Leave room in the frame for the intended movement; check complete limbs, clear depth, screen direction, and light. |
| 首尾帧视频 | A specific start and end state must be connected | Align identity, scene landmarks, camera side/height, light direction, and prop state; describe a plausible path between frames. |

A director-table view or camera-plan screenshot may serve as an input frame if it matches the approved shot. Carry its camera ID and space landmarks into the generation brief. A screenshot establishes the spatial relationship; it does not prove that the eventual motion will work. For a shot with no usable input frame, mark the input as missing or propose a new keyframe; do not invent one as an existing file.

## 2. Write one motion brief per selected shot

The motion brief references the approved `Shot ID`, beat, **project** start–end timecode, duration, camera ID, input-frame IDs, and asset IDs. Use this order:

`starting state → subject action and end state → speed / amplitude → environment response → camera movement → fixed identity, geometry, light and sound anchors → handoff / exclusions`

Describe the change that the video must show. When an input image already fixes clothing, product structure, and composition, reference those anchors instead of redescribing or redesigning them. Prefer one dominant subject action and one camera instruction at most; add environment motion only when it serves the shot. A static camera and still environment are valid choices. Keep model syntax and numeric settings out until a target platform is confirmed.

## 3. Generate and compare only within the requested scope

When the creator requests tests or provides results, establish one baseline with the same input, aspect ratio, intended action, and comparable duration. For a targeted revision, change one meaningful factor at a time, such as movement amplitude, duration, camera motion, or input view. A three-level amplitude comparison or a second platform is optional and should answer a real shot-level uncertainty; it is not a default deliverable. Cross-platform comparisons need the same shot intention and comparable inputs, with the actual platform/model version and access date recorded. Costs, speed, model strengths, and success rates are observations from the creator's run, not universal facts.

Compare candidates on: subject/product identity, action completion, background stability, camera intention, visible artifacts, usable duration, and fit with adjacent shots. Record cost and workflow handoff only if known and relevant. Select the candidate that best serves the shot, with a short reason; preserve a backup when a usable alternative exists.

## 4. Inspect the full generated motion

Review the start, middle, and end frames and, for longer or complex motion, a contact sheet or sampled frame strip. Check face, hands, product geometry, object contact, occlusion, background landmarks, screen direction, light, and the final state required by the next shot. A good first and last frame do not establish a good middle. A candidate is `待检查` until an actual clip or sampled frames have been inspected.

Describe failures as observed symptoms and affected timecodes. Diagnose cautiously:

- Identity or product structure drifts: examine action size, duration, occlusion, view change, and conflicting references; try a smaller motion or shorter usable segment, then a clearer input/view if needed.
- Background flickers or boils: inspect dense textures, reflections, particles, and fast camera motion; simplify the input or separate background motion where useful.
- Contact or action lacks causality: specify the start/contact/end states or split the interaction across shots.
- Camera moves unpredictably: remove competing camera instructions and keep one readable path.

Change the smallest factor supported by the observed failure. A failed clip may still yield a usable segment; otherwise replace the shot with a simpler angle or solve the transition through a still frame and edit. Do not promise that a particular repair will succeed. Record what changed and whether a new result was actually checked.

## 5. Assemble a reusable shot package

For every produced shot, keep its selected clip, usable time range, backup clip if one exists, input frames, motion prompt, platform/model/version and settings actually used, result/defect notes, selection reason, and source or rights status. If no clip has been generated, output a **planned** manifest with empty result fields; do not label it final.

Use the worksheet's W05 tables for the generation decision, candidate review, repair log, and shot-package manifest. Preserve the project timecodes in the shot table; separately record clip-local usable ranges. The package should let an editor place the selected segment into the existing animatic timeline and see any remaining shot gap.

Do not carry over lesson plans, teacher demonstrations, student tasks, classroom grading, fixed platform rankings, or unsupported claims about a reference film's production process.

---
name: pixcake-preview-creative-workflow
description: Use PixCake (像素蛋糕) as the portrait-retouch stage before creative image work. Trigger whenever the user asks to use PixCake/像素蛋糕 to retouch photos, select portraits and apply presets, classify the presets currently available on the local PixCake account, use a PixCake preview for secondary creation, or says “拿像素蛋糕修图”. Discover and classify the live local preset suites without embedding a stale preset list, choose presets from the actual photo content, apply them through PixCake MCP, inspect the completed on-screen preview without exporting, capture that preview as a retouch reference, and create a separate derivative from the clean original plus the preview.
---

# PixCake Preview Creative Workflow

Use PixCake for real portrait beautification decisions, then use its completed preview as a visual reference for independent creative work. Never replace this with a verbal approximation of the preset.

## Non-negotiable sequence

1. Inspect and select the source photos.
2. Discover and classify PixCake's current local/account preset suites.
3. Build a task-specific shortlist from that live classification.
4. Match a shortlisted preset to the selected photo and test it on a representative image.
5. Apply the accepted preset through PixCake MCP.
6. Open the image in PixCake and wait until preview processing is complete.
7. Capture and crop the actual preview image.
8. Send both the clean original and cropped preview to the creative image workflow with explicit input roles.
9. Save a new deliverable without overwriting the original.

Do not skip steps 2, 5, or 6. Do not claim to have used the PixCake preview when only the clean original was supplied to image generation.

## 1. Select photographs

For folders with bursts or near-duplicates:

- Build contact sheets or inspect thumbnails in groups.
- Group adjacent filenames, capture times, and visually similar frames as one burst.
- Keep the best one or two frames from each meaningful moment.
- Prefer sharp eyes, natural expressions, clean hand positions, emotional interaction, useful negative space, and minimal occlusion.
- Reject blinks, transitional mouth shapes, repeated poses, missed focus, awkward limbs, and frames that add no new story beat.
- Keep a short selection record containing filename and reason.

Preserve source orientation by default. If the original is landscape or the user asks for 横版, keep the creative output landscape even when another design skill defaults to portrait.

## 2. Discover presets before choosing

Call PixCake MCP's current preset-list tool before each new job or whenever the app/version/account changes. Record the returned preset names and IDs. Never invent a preset, assume yesterday's list is unchanged, or hard-code one preset for all portraits.

Classify the returned live list before choosing. This classification is temporary working data for the current machine/account state; do not copy the user's complete preset inventory into this skill or treat an old catalog as authoritative.

At minimum:

- separate official/recommended, personal, and team presets using the returned source metadata;
- retain every exact preset ID even when names repeat;
- detect likely copies such as names ending in `（1）`, `（2）`, or equivalent suffixes, group them as one family for browsing, but never merge their IDs when applying;
- assign each preset to a practical primary category: skin/complexion, wedding/couple, child/newborn/maternity/family, ID/corporate/group, film/camera/retro, cinematic/emotional/night, Chinese/period/cultural, fresh/Japanese/Korean/natural, painterly/fantasy, travel/season/outdoor, cosplay/special theme, or general portrait/other;
- create a small task-specific shortlist by intersecting the photo's subject, scene, light, skin need, requested color fidelity, and risk tolerance with those categories.

Treat name-based classification as directional metadata, not proof of the visual result. Names can identify likely purpose and style, but cannot establish smoothing strength, face reshaping, whitening, highlight behavior, or color drift. Validate those properties on representative previews before accepting a preset.

For a large preset library, report category counts and duplicate families first. Do not test hundreds of near-duplicates blindly. Select representative candidates from the relevant categories, then compare them on a small standard set such as one close portrait, one environmental portrait, and one multi-person frame.

If MCP reports that PixCake is not on the homepage, navigate the app to 我的主页 and retry. If the main app is not running or account authorization fails, report that state accurately; do not simulate successful MCP work.

## 3. Choose a preset from photo evidence

Classify each selected image before choosing:

- subject mix: bride, groom, couple, group, child, elder;
- framing: face close-up, half body, full body, environmental portrait;
- light: soft daylight, backlight, mixed light, low light, high contrast;
- skin need: blemish cleanup, under-eye cleanup, texture retention, makeup preservation;
- scene need: preserve existing color, wedding color treatment, or color correction;
- risk: plastic skin, face reshaping, whitening, color drift, inconsistent treatment across multiple people.

Use only presets present in the live list and select candidates from the current task-specific classification, not from memory. Prefer a natural or texture-preserving portrait preset for already well-exposed wedding photographs. Consider stronger cleanup only for close-ups with visible need. Avoid strong color-style presets when the user asks to retain original color.

Test uncertain choices on one representative image. For a mixed set, test at least one close portrait and one multi-person or environmental frame before batch application. Inspect the actual result; if skin becomes plastic, identity shifts, makeup is lost, or scene color drifts, try a gentler live preset and compare again.

## 4. Apply through PixCake MCP

- Create or reuse a dedicated MCP-visible project.
- Import only the selected files or a small representative trial set first.
- Maintain an exact mapping of `image_id` to source filename; do not assume import order.
- Apply the chosen `preset_suit_id` to the intended image IDs.
- Check success, failure, skip, and no-op counts.
- Return to the PixCake homepage before MCP calls when required by the server.

Never call PixCake export unless the user explicitly asks to export and understands the possible charge. Applying presets and viewing previews are not authorization to export.

## 5. Inspect the completed preview

Use Windows app control to open the MCP project and select the exact filename. Wait until face/skin processing indicators have completed. Inspect at useful magnification and, when available, toggle the original comparison.

Check:

- identity and facial geometry remain intact;
- skin is refined but still has believable texture;
- eyes, lips, makeup, hairline, and hands remain natural;
- multiple faces receive appropriate and consistent treatment;
- original scene color and clothing color remain stable;
- no processing artifact crosses hair, veil, glasses, jewelry, or face edges.

If the result fails, return home, change the preset through MCP, and inspect again. Do not proceed from an unfinished or visibly unsuitable preview.

## 6. Capture the preview reference

Capture the current PixCake window only after processing completes. Crop to the displayed photograph and exclude menus, sliders, thumbnails, and other UI whenever possible. Name the reference by source filename, for example `pixcake-preview-DSC05663.png`.

The captured preview may contain PixCake preview watermarks. Use it only as a secondary appearance reference for skin finish, local contrast, facial brightness, and color response. Do not treat a captured paid preview as the clean final photograph or create a direct watermark-removed substitute.

## 7. Compile inputs for secondary creation

Use these roles explicitly in the image-generation prompt:

- **Image 1 — clean original / edit target:** sole factual source for identity, pose, hands, clothing, geometry, scene detail, and clean pixels.
- **Image 2 — PixCake completed preview / retouch reference:** reference only for complexion, blemish cleanup, under-eye treatment, texture, makeup retention, local facial contrast, and color balance.
- **Optional Image 3 — layout/style reference:** reference only for the requested creative skill's composition and visual system.

Require the output to preserve Image 1's identity and geometry while matching the approved human finish visible in Image 2. Explicitly prohibit copying watermarks, UI elements, or preview artifacts. If the task uses another image skill, read and follow that skill too; this PixCake skill controls the upstream retouch-reference stage and input roles.

## 8. Save and report

- Save the new result in the workspace with a descriptive versioned filename.
- Never overwrite or modify source photographs.
- State which source filename, PixCake preset name, and preview reference were used.
- State clearly whether PixCake export was called; the default must be “not exported.”
- If producing a series, keep a small manifest mapping source → preset → preview → final output.

## Completion gate

Before reporting completion, verify all of the following:

- The selected frame is not a weaker burst duplicate.
- The preset came from the live PixCake list and suits the image.
- The MCP apply call succeeded for the correct image ID.
- The actual completed PixCake preview was captured.
- Both the clean original and PixCake preview were supplied to secondary creation.
- The prompt stated their different roles.
- Orientation follows the source or user's explicit request.
- The final is a new independent artwork, contains no PixCake watermark or UI, and the original remains untouched.
- No PixCake export occurred without explicit permission.

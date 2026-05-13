# 9-slice Panel Rules

> Purpose: This file defines how to generate, configure, apply, and QA a reusable 9-slice panel asset for game-style UI skinning on top of an existing tool layout. The goal is to replace visual style only, without changing the user's content structure, layout, or interaction flow.

---

## 1. Core Principle

A 9-slice panel asset is not just an image. It is:

```yaml
transparent_png_source_image: panel_base_9slice.png
render_mode: sliced / scale9
slice_config:
  top: number_px
  right: number_px
  bottom: number_px
  left: number_px
```

A panel image is only a valid 9-slice asset when all of the following are true:

1. It is a single transparent PNG source image.
2. It has explicit slice parameters.
3. The UI engine renders it with real 9-slice / scale9 logic.
4. It is reused across multiple compatible component sizes without ordinary full-image scaling.

Do not call an ordinary stretched image a 9-slice asset.

---

## 2. Scope

This rule applies to visual skinning of an existing tool UI. It must not change:

- User content
- Page structure
- Component count
- Component positions
- Interaction flow
- Business logic
- Text meaning
- Card/list/form/button semantics

This rule only controls the visual replacement layer:

- Panel background image
- Border material
- Surface texture
- Slice configuration
- State overlays
- Component usage boundary
- QA rules

---

## 3. Default Asset Budget

Default strategy:

```yaml
default_panel_image_budget: 1
required_asset:
  - panel_base_9slice.png
```

Do not generate multiple panel images by default.

Do not generate one image per size.

Do not generate separate card/container/status-bar images unless the one-image strategy clearly fails inside its allowed usage boundary.

### Default implementation

Use one neutral reusable panel image plus different UI parameters:

```lua
backgroundImage = "panel_base_9slice.png"
backgroundFit = "sliced"
backgroundSlice = { top = ?, right = ?, bottom = ?, left = ? }
```

Different component types should first be distinguished by:

- `backgroundSlice`
- opacity
- tint
- padding
- shadow
- border overlay
- selected overlay
- top strip layer
- disabled overlay
- corner accent visibility

Do not default to extra image generation.

---

## 4. Required Source Image Properties

`panel_base_9slice.png` must be designed as a neutral reusable panel skin.

### Must have

- Transparent PNG.
- External area must be alpha transparent.
- Only the panel body should be visible.
- Clean stretchable center.
- Lightweight border.
- Subtle material texture.
- Small radius or restrained corner treatment.
- No strong ornament.
- No baked-in state.

### Must not have

- White canvas background.
- Screenshot background.
- Mockup preview.
- Instruction labels.
- Multiple size examples.
- 9 separate sliced images.
- Text.
- Logo.
- Avatar.
- Button content.
- Check icon.
- Selected state.
- Top category strip.
- Disabled overlay.
- Strong shadow.
- Large corner ornament.
- Complex center pattern.
- High-contrast texture.

### Recommended visual quality

```yaml
center:
  texture: very_light
  contrast: low
  stretchable: true
border:
  weight: light_to_medium
  visual_priority: below_content
corners:
  ornament: none_or_very_small
  must_fit_inside_slice_area: true
background:
  alpha: transparent_outside_panel
```

---

## 5. Image Generation Prompt Requirements

When asking an AI/Maker system to create the source image, use constraints like this:

```text
Generate exactly one transparent PNG UI panel asset named panel_base_9slice.png.
This is a source image for real 9-slice rendering, not a mockup, not a demo sheet, not a preview.
The image must contain only the panel body. The outside area must be fully transparent alpha.
The center area must be clean and freely stretchable. The border must be light and readable.
Do not include text, logo, avatar, icon, check mark, selected state, top strip, disabled overlay, white background, screenshot background, or multiple size examples.
The asset should be neutral enough to be reused for cards and medium panels. Component differences will be handled with backgroundSlice, opacity, padding, tint, shadow, and overlays.
```

If an image already exists, do not regenerate by default. First inspect and reuse it:

```text
Use the panel image already provided in this conversation/project as panel_base_9slice.png.
Do not regenerate a new panel image unless it fails transparency, center stretchability, or usage-boundary checks.
```

---

## 6. UrhoX / Maker 9-slice Configuration

UrhoX supports true 9-slice rendering via `UI.Panel`:

```lua
UI.Panel {
  backgroundImage = "image/panel_base_9slice.png",
  backgroundFit = "sliced",
  backgroundSlice = { top = 24, right = 24, bottom = 24, left = 24 },
}
```

Known behavior:

```yaml
rendering: true_9slice
backgroundFit: sliced
backgroundSlice_unit: px
supports_transparent_png: true
supports_independent_sides: true
supports_runtime_resize: true
children_overlay: true
```

Children such as text, avatars, icons, selected overlays, and top strips should be rendered above the sliced background.

---

## 7. Slice Configuration Guidelines

Slice values must match the actual source image border/corner design.

### General guideline

```yaml
slice_edge_range: 8%-14% of source image dimension
corners: fully inside non-stretch areas
center: largest possible clean stretch area
```

### Example presets

For a neutral source image around `512x384`:

```yaml
card_or_medium_panel:
  top: 24
  right: 24
  bottom: 24
  left: 24

large_container:
  top: 40
  right: 48
  bottom: 40
  left: 48

caution_long_bar_test_only:
  top: 12
  right: 24
  bottom: 12
  left: 24
```

Do not blindly reuse the same slice values for all component types.

For low-height components, `top + bottom` must be much smaller than the component height.

Recommended:

```yaml
max_top_bottom_ratio_for_low_height: 0.30-0.40
```

Example:

```yaml
component_height: 96
recommended_top_plus_bottom_max: 29-38
avoid:
  top: 50
  bottom: 50
```

If `component_height - top - bottom <= 0`, the center slice collapses or is skipped and the asset is invalid for that component.

---

## 8. Usage Boundary

`panel_base_9slice.png` is a medium card/panel asset, not a universal asset for every possible shape.

### Safe usage

Use `panel_base_9slice.png` when:

```yaml
min_width: 120
min_height: 120
aspect_ratio_min: 0.75
aspect_ratio_max: 2.8
component_types:
  - character_card
  - item_card
  - selection_card
  - medium_panel
  - popup_content_panel
  - settings_panel
```

### Caution usage

Use with caution when:

```yaml
height: 96-120
aspect_ratio: 2.8-3.2
requirements:
  - visually verify border clarity
  - verify corners are not squeezed
  - verify content is not crowded
  - verify no blur
```

### Forbidden usage

Do not use `panel_base_9slice.png` when:

```yaml
aspect_ratio: "> 3.2"
height: "< 96"
component_types:
  - status_bar
  - long_info_bar
  - thin_button
  - toolbar
  - divider
  - pill_label
  - tiny_icon_panel
symptoms:
  - blurred_border
  - heavy_end_caps
  - squeezed_corners
  - looks_like_flattened_card
```

For forbidden cases, first use UI primitives instead of generating another image:

- backgroundColor
- borderWidth
- borderColor
- borderRadius
- opacity
- shadow
- tint
- left accent strip
- selected overlay

Only if these fail and high visual quality is required, request a separate `bar_panel_9slice.png` as an explicit fallback.

---

## 9. One-image Strategy and Fallback Policy

### Default

Use one image:

```yaml
asset: panel_base_9slice.png
strategy: one_image_plus_multiple_parameters
```

### Allowed parameter differences

```yaml
component_variants:
  card:
    backgroundSlice: smaller
    padding: medium
    shadow: light
  container:
    backgroundSlice: larger
    padding: larger
    opacity: slightly_lower
  status_like_bar:
    preferred: UI_primitives
    9slice_usage: forbidden_or_caution_only
```

### Fallback permission

An extra image may be requested only when:

1. The component falls outside the safe usage boundary.
2. UI primitives cannot achieve acceptable visual quality.
3. The issue is confirmed after slice/padding/opacity/alignment adjustments.
4. The system reports the failure reason before generating the new image.

Allowed first fallback:

```yaml
asset: bar_panel_9slice.png
for:
  - status_bar
  - long_info_bar
  - long_button
condition: explicit_approval_or_confirmed_failure
```

Do not silently generate fallback images.

---

## 10. State and Overlay Rules

Do not bake states into `panel_base_9slice.png`.

### Selected state

Implement selected state above the panel background using:

- border overlay
- inner highlight
- small marker
- color strip
- glow layer
- corner check icon from existing vector/icon library

Do not generate selected state image by default.

Do not use selected red in a way that looks like error state.

### Disabled state

Implement disabled state using a semi-transparent overlay above content or background.

Do not bake disabled tint into the base panel.

### Top strip

Implement category or rarity strip as an independent UI layer.

Do not bake top strip into `panel_base_9slice.png`.

---

## 11. Layer Order

Recommended layer order:

```yaml
1: sliced_panel_background
2: optional_tint_or_surface_overlay
3: content_image_or_icon
4: text
5: top_strip
6: selected_overlay_or_border
7: state_marker_or_check
8: disabled_overlay_if_needed
```

Accent decorations should not be hidden under a gray tint unless the component is explicitly disabled.

---

## 12. QA Checklist

A valid 9-slice panel implementation must pass all checks:

### Image checks

- Is it a transparent PNG?
- Is the outside area alpha transparent?
- Is there no white background?
- Is there no screenshot/mockup background?
- Is the center clean and stretchable?
- Are corners inside the non-stretch slice area?
- Are borders simple enough for scaling?
- Are state elements absent from the base asset?

### Engineering checks

- Is `UI.Panel` used?
- Is `backgroundImage` set?
- Is `backgroundFit = "sliced"` set?
- Is `backgroundSlice` set?
- Are slice values in px?
- Is the same image reused across compatible sizes?
- Are children rendered above the background?
- Is ordinary image scale/stretch avoided?

### Size checks

- Is the component within safe size/aspect-ratio bounds?
- Is `top + bottom < component height`?
- Is `left + right < component width`?
- Are component coordinates and dimensions integer-aligned?
- Are borders visually stable?
- Are corners not squeezed?
- Is there no blur on long bars or low-height components?

### Visual checks

- Does the panel support content readability?
- Does the border avoid overpowering text/content?
- Does the center texture stay subtle?
- Does selected state remain separate from base panel?
- Does the result avoid looking like a flattened card when used as a bar?

---

## 13. Common Failure Modes and Fixes

### Failure: White rectangle behind panel

Cause:

- Source image has white canvas or non-transparent background.

Fix:

- Remove white background.
- Export true transparent PNG with alpha.
- Reject asset if alpha transparency cannot be confirmed.

---

### Failure: Looks like ordinary image scaling

Cause:

- `backgroundFit` is not `sliced`.
- `backgroundSlice` missing.
- Component uses image scale/stretch.

Fix:

```lua
backgroundFit = "sliced"
backgroundSlice = { top = ?, right = ?, bottom = ?, left = ? }
```

---

### Failure: Border blurry on 480x96 status bar

Cause:

- Component aspect ratio too high.
- Component height too low.
- `top + bottom` too large.
- Source asset has soft gradients/shadows.
- Linear filtering and non-integer scaling blur fine lines.
- The medium panel asset is being used outside its boundary.

Fix priority:

1. Do not use `panel_base_9slice.png` for aspect ratio > 3.2.
2. Use UI primitives for status bar.
3. Reduce slice only if still within caution boundary.
4. Ensure integer component size and position.
5. If high-quality bar is required, request `bar_panel_9slice.png` as an explicit fallback.

---

### Failure: Small cards feel crowded

Cause:

- Border too thick.
- Corner ornament too large.
- Slice areas consume too much space.

Fix:

- Use lighter source image.
- Reduce ornament.
- Use smaller slice values if safe.
- Increase content padding only if card remains readable.
- Consider no corner ornament in base asset.

---

### Failure: Main container and cards look identical

Cause:

- One image is reused without parameter differentiation.

Fix:

- Keep one image but differentiate with:
  - slice values
  - opacity
  - padding
  - shadow
  - surface tint
  - content layer spacing

Do not generate new image by default.

---

## 14. Recommended Prompt: Use Existing Image

Use this when the image already exists and should not be regenerated:

```text
Use the panel image already provided in the current conversation/project as the only panel asset: panel_base_9slice.png.
Do not regenerate the image.
Do not create additional panel images.
Use it with UI.Panel backgroundFit = "sliced" and explicit backgroundSlice values.
Apply it only to components within its safe usage boundary: height >= 120px and aspect ratio 0.75~2.8.
For long bars, status bars, thin buttons, and aspect ratio > 3.2, do not use this image. Use UI primitives first.
Output the exact backgroundImage, backgroundFit, and backgroundSlice configuration for each component type.
```

---

## 15. Recommended Prompt: Generate New Base Asset

Use this when no valid base asset exists:

```text
Generate exactly one transparent PNG UI panel source image named panel_base_9slice.png.
This is for real 9-slice rendering in UrhoX UI.Panel, not a mockup or preview.
The outside area must be fully transparent alpha. The image must contain only the panel body.
The center area must be clean, low-texture, and freely stretchable.
The border must be light and reusable. Corners must be minimal and fit inside the slice area.
Do not include text, logo, avatar, icon, selected state, top strip, check icon, disabled overlay, white background, screenshot background, demo sheet, or multiple size examples.
After generating the image, output a recommended backgroundSlice configuration and safe usage boundary.
```

---

## 16. Metadata Template

Every 9-slice asset entry should include:

```yaml
asset_name: panel_base_9slice.png
asset_type: 9slice_panel
format: transparent_png
source_size:
  width:
  height:
recommended_slice:
  top:
  right:
  bottom:
  left:
safe_usage:
  min_width: 120
  min_height: 120
  aspect_ratio_min: 0.75
  aspect_ratio_max: 2.8
caution_usage:
  min_height: 96
  aspect_ratio_max: 3.2
forbidden_usage:
  aspect_ratio_above: 3.2
  height_below: 96
  components:
    - status_bar
    - long_info_bar
    - thin_button
    - toolbar
state_policy:
  selected: overlay_not_baked
  disabled: overlay_not_baked
  top_strip: separate_ui_layer
image_budget_policy:
  default: one_image
  fallback: bar_panel_9slice_only_after_confirmed_failure
qa_status:
  transparent_background:
  real_sliced_rendering:
  multi_size_test:
  blur_test:
last_updated:
```

---

## 17. Final Rule

Use 9-slice to reduce image count, not to force one image onto every possible shape.

Default to:

```yaml
one_neutral_panel_image: true
multiple_slice_and_ui_parameters: true
```

But respect usage boundaries:

```yaml
medium_cards_and_panels: use_panel_base_9slice
long_bars_and_thin_components: use_ui_primitives_first
extra_images: explicit_fallback_only
```

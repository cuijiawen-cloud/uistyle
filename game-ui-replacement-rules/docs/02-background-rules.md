# Background Rules

## 1. Purpose

This document defines how backgrounds should be designed when replacing a tool-style UI with a game-style UI.

The goal is not to put a game image behind a tool UI.  
The goal is not to decorate a tool UI with game logos, characters, icons, or representative colors.

The goal is to translate the target game or target style’s visual logic into the current UI, so that the result feels like the tool UI naturally exists inside that game world.

A valid background must preserve:

- the original information structure;
- the original layout relationship;
- the original interaction path;
- the original text meaning;
- clear state expression;
- readable panels, cards, buttons, inputs, and status text;
- Maker / UrhoX implementation feasibility.

The background is a supporting layer. It provides atmosphere, spatial context, and world recognition, but it must not compete with the functional UI.

A background fails if it becomes more important than the tool UI itself.

---

## 2. Scope

This document defines rules for:

- background type selection;
- background visual hierarchy;
- background and panel relationship;
- UI safe area protection;
- named game / IP background handling;
- non-character recognition anchors;
- background readability requirements;
- Maker / UrhoX implementation constraints;
- good and bad background examples;
- QA checks;
- background-related failure attribution.

This document does not define:

- detailed panel construction;
- 9-slice slicing strategy;
- button state visuals;
- typography rules;
- decoration semantics;
- final asset budget;
- screen size adaptation rules;
- global QA taxonomy.

Those topics are covered by related documents.

Background rules must not be designed independently. They must be derived from the same Style Contract as panels, text, states, accents, and decorations.

The expected derivation chain is:

```text
Game Definition Evidence
→ Game Style Understanding
→ Unified Style Contract / inferred_style_brief
→ Background Rules
→ Panel / Text / State / Accent Rules
→ Negative Case Checks

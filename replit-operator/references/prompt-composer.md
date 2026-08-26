# Prompt composer

Use the new-conversation composer as the central control surface. Confirm a fresh conversation and the intended workspace before adding context or submitting work.

## Context menu

Use the add-context control to inspect available actions. In the verified interface it exposes Upload a file, Create something new, Import an existing project, Use a skill, Use a design system, and Add an integration.

- Treat uploads, imports, creating a design system, and integration setup as external-impact actions that require approval at the relevant action point.
- Treat any claim that a composer integration is equivalent to a workspace integration as unverified until checked from the live interface or official documentation.
- The verified Create something new submenu includes Website, Mobile, Design, Slides, Animation, Data Visualization, 3D Game, Document, Spreadsheet, and Attach a Figma design. Verify the available choices live.

## Agent mode

Open the agent-mode control through the visible button or supported keyboard shortcut. Verify the selected mode before submission.

- Free mode is the baseline free workflow. Confirm its visible label rather than assuming its model or usage policy.
- Paid modes can expose model and effort controls and can affect billing. Explain the impact and obtain confirmation immediately before switching into a paid mode.
- When a model is manually selected, inspect the available effort levels and confirm the intended combination. Auto mode delegates model and effort selection to Replit.
- Model names, mode labels, capabilities, usage limits, and pricing are volatile. Record current UI evidence; do not hard-code the current catalog.

### Verified control behavior

- The selector identifies the keyboard shortcut as Command-Shift-I and currently offers Free, Power, and Max. Replit's visible notice says Power and Max were renamed from earlier mode names; use the labels presently shown, not remembered labels.
- Power and Max can expose a primary-model picker and an effort control. Inspecting these controls is safe; selecting a paid mode, a model, or a non-default effort requires immediate approval because it can affect cost and behavior.
- In the inspected Max view, the picker offered Auto plus a current catalog of named models, and the effort control was disabled while Auto was selected. Treat that catalog and state as volatile.
- Selecting a named Max model enabled the effort slider; one keyboard increment changed the visible guidance from Medium to High. Returning to Auto restored the disabled slider at Low. The mode flow was verified across Free, Power, and Max, then restored to Max with Auto and Low.

## Voice capture

The voice control is labelled Start voice input in the verified interface. Treat it as input capture, not real-time voice conversation, unless the live interface states otherwise. Starting it enters recording state with Cancel recording and a disabled Submit recording control; cancel immediately after a verification test and never submit captured audio without approval. Starting it may invoke microphone permissions, so obtain approval before activating it; confirm before transmitting sensitive spoken content.

## Final verification

Before sending, verify the intended workspace, mode, selected context, visible prompt text, and any paid or external-impact implications. Follow the active browser policy for final message submission.

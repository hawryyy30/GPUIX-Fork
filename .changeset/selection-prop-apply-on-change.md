---
"@gpuix/native": patch
"@gpuix/react": patch
"@gpuix/solid": patch
---

Fix `selection` prop on input/textarea clobbering the caret after user edits.
The prop is now applied only when its value changes since the last apply: an
unchanged prop is never re-asserted, so typing over a programmatic selection
keeps the edit's caret (reported through `onSelect`) instead of being reset to
the stale, clamped range. Treat the prop as a command ("go here"), not a
constraint.

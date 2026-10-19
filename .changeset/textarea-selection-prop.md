---
'@gpuix/native': minor
'@gpuix/react': minor
'@gpuix/solid': minor
---

`<input>` and `<textarea>` now accept a `selection={{ start, end }}` prop (UTF-16 offsets, matching JS string indexing) to move the caret or select a range programmatically, and report every caret/selection move through a new `onSelect` event carrying the normalized range in `event.startIndex` / `event.endIndex`. This unblocks find-next/prev, go-to-line, and bracket auto-close in editor-style apps. See "Programmatic selection" in the README.

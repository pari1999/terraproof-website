# Dashboard media for the marketing site

Filenames matter — the site references them directly. Until a file exists, its slot shows a
labeled placeholder frame, so a missing asset never looks broken.

| Filename | Type | Slot | Status |
|----------|------|------|--------|
| `dashboard-overview.png` | image | Overview (hero + top of `#dashboard`) | ✅ in place |
| `dashboard-evidence.png` | image | Evidence card | — still a placeholder |
| `dashboard-proof.png` | image | Proof card | — still a placeholder |
| `live_animaldetection.mp4` | video (autoplay/muted/loop) | Live card | ✅ in place |
| `form_generation.mp4` | video (autoplay/muted/loop) | Report card | ✅ in place |

## Capture tips (for the two remaining slots)
- Run the dashboard: `simulation/start.ps1`, open `http://localhost:5173`, and (for real data) run
  `python device/demo.py --source images --year 2025 --upload http://localhost:8000 --reset`.
- Capture at a wide viewport (≈1600×1000) so the framed 16:10 / 16:9 slots stay crisp.
- Dark theme, full-bleed content (hide the browser chrome — the site draws its own).
- PNG, ideally under ~500 KB (run through an optimizer if larger).

## Video notes
- Keep clips well under ~10–15 MB each (autoplay + loop means every visitor downloads it).
- No audio needed — videos are muted by design, so trim/skip the audio track if convenient.
- `playsinline` + `muted` is required for autoplay to work on mobile browsers.

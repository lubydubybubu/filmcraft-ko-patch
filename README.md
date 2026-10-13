# filmcraft-ko-patch

Korean (한국어) interface patch for **[FilmCraft](https://github.com/storytold/filmcraft)** (Premiere-style video editor), upstream tag `v0.6.0`.
This repository contains **only the patch**, not FilmCraft's source code. See `BASE.txt` for the exact upstream commit.

## Apply
```bash
git clone --branch v0.6.0 https://github.com/storytold/filmcraft.git && cd filmcraft
git apply ../filmcraft-ko-patch/patches/filmcraft-v0.6.0-ko.patch
```
Then build as upstream documents (release builds embed fonts with `CRAFT_FONTS_DIR`).
Unofficial Windows cross-build: see [artcraft-ko-toolkit](../artcraft-ko-toolkit).

## What it changes
Korean catalog based on storytold/filmcraft PR #963 (ko part, loeness), editing terms reworked (자르기 도구, 잔물결 삭제 …); Hangul system-font fallback (Malgun Gothic etc.); ko in settings validation and native menu.
Changed files: `CHANGED-FILES.txt`.

## Verified
Python 15/15, cargo ui-egui i18n/cjk/theme 32/32, engine settings 38/38, 7,308 Hangul glyph checks; Windows GUI: 347/382 menu items Korean, language switch persists.

## Known limits
Korean IME typing in the program monitor not verified (upstream fix #1110 not included).

Translations are AI-assisted (Claude Opus 5.5) and not reviewed by a professional translator.
Licence: MIT OR Apache-2.0, same as FilmCraft; upstream contributions credited above.

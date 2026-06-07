# AGENTS.md

This repository is a **Hindi long-form novel writing project** ("परछाइयों का सम्राट"), not a software codebase. There is no `package.json`, no test/lint/typecheck/build pipeline, and no CI. The "code" is prose in Markdown. Treat every chapter file as a unit of work.

## Authoritative instruction files (read in this order)

1. **`CLAUDE.md`** — Primary project instructions. Contains the **writing-regime rules** (the 13-rule locked ruleset at the top), current story state (where the narrative is right now, what's next, who is active), the power system, character list summary, and platform rules. **Always read first when working on a new chapter.**
2. **`Writing-Rules.md`** — The 13-rule official rule book (नियम 0–12). Supreme authority on prose style. Applies to every `अध्याय_*.md`. Examples in it use Shiva/Sati/Daksh characters as illustrations only — our story is about रुद्र, not them.
3. **`आर्क-रोडमैप.md`** — Structural map: 12 फ़ेज़, 360 खण्ड. **Source of truth for arc structure and beat-level planning.** Phase 1 (खण्ड 1–30) is fully detailed; later phases are one-line beats that must be expanded when the narrative approaches them.
4. **`अध्याय-योजना.md`** — Chapter-level one-liner outline for all 2,520 chapters. **Read the target chapter's one-liner immediately before writing.**
5. **`List of Characters.txt`** — Full character sheet. **Read before introducing any new character; update it when a new character is added.**

## Repository layout (non-obvious)

- Chapters live at the deeply nested path:
  `अध्याय\फ़ेज़_NN_<फ़ेज़-नाम>\उप-भाग X — <उप-भाग-नाम> (खण्ड M–K)\अध्याय_NNN.md`
  Filenames are **zero-padded** (`अध्याय_064.md`, not `अध्याय_64.md`). Phase 1 currently has two उप-भाग: A (खण्ड 1–7) and B (खण्ड 8–16). When writing a chapter, **find the highest existing `अध्याय_NNN.md` across all उप-भाग folders** — the next one is `highest + 1`.
- `Example/` — Reference chapters from a separate, unrelated story. Use for Hindi style/pacing reference only; **do not** treat its characters, lore, or cultivation system (कुण्डलिनी चक्र, etc.) as canon. Our system is रक्त-रत्न / काली विद्या / छायासम्राट.
- `Gudline.txt` — Pocket FM platform rules (audiobook format, no Roman script, novel prose not screenplay).
- `Prompts` — Original master brief. **Do not edit.**
- `MyComment` — User scratch notes.
- `Series Description (Hindi).md` — High-level series description.
- `setting.json` — **API keys for the user's opencode setup, not opencode config.** Contains an `ANTHROPIC_API_KEY`. Treat as secret — never commit to a new repo, never log.
- `GEMINI.md` — Empty (0 bytes). Ignore.
- `.claude/settings.local.json` — Local tool permissions. Edit when adding new bash patterns the user approves.

## Pre-write checklist (every new chapter)

These are in `CLAUDE.md` — restated here because skipping any of them produces off-tone work:

1. `Get-ChildItem -Recurse "अध्याय"` for `अध्याय_*.md` and find the highest number. Next file = `highest + 1`.
2. Read the **previous chapter in full** — especially its closing `[अगले Episode में :]` hook. The new chapter's opening `[पिछले Episode में :]` recap must tee up from that hook.
3. Look up the target chapter's **one-liner** in `अध्याय-योजना.md`.
4. Look up the **arc's beats** in `आर्क-रोडमैप.md`. If the arc's 7th chapter, plan a **bigger cliffhanger** than internal chapters.
5. Skim `List of Characters.txt` for continuity on names, ages, relationships.
6. Write the file. **Never overwrite, never skip numbers.**
7. If new characters appear, **update `List of Characters.txt`**.

## Hard prose rules (high-signal subset — full list in Writing-Rules.md)

- **Script:** Devanagari only. No Roman transliteration. No English words like `Chapter`, `Arc`, `Episode` in the story text.
- **Numbers:** All numerals in **English digits** (`अध्याय 64`, `5000 शब्द`) — never देवनागरी (६४) or words (पैंसठ).
- **Word count:** 3000–5000 words per chapter. If a scene can't fit, split into `अध्याय 64.1`, `64.2`... — do not compress.
- **Chapter structure:** Hindi title line → `पिछले Episode में -` (recap same line, 2–3 lines, भूतकाल) → flowing prose (no section dividers, वर्तमान काल for live scenes) → `अगले Episode में -` (hook same line, 1–2 lines) → `सुनते रहिए — परछाइयों का सम्राट`. No square-bracket narration blocks (`[SFX: ...]`, `[संगीत: ...]`) — banned. No colon-after-label format. No section dividers.
- **Special characters:** Only `। , ? ! : ; " "` plus the two tags. Em-dash (—) and parentheses are fine in flowing prose.
- **Dialogue:** Wrapped in narration (`रुद्र ने कहा, "..."`). Never `रुद्र: ...` screenplay format. Single-voice audiobook means listener must track speakers without seeing the page.
- **Mantras/shlokas:** Original Sanskrit in-text, meaning woven into narration/flowing dialogue — don't break the story.
- **Sentences in Sanskrit-heavy register** for शृंगारिक passages; otherwise modern spoken Hindi.
- **Avoid these banned patterns** (rotated through earlier chapters, now flagged):
  - "एक छोटी सी" / "एक तीव्र" / "एक छुपी" / "एक स्थिर" — drift; vary with "हल्की, गहरा, गाढ़ा, तेज़, पैना, अनकहा, मूक, सहसा".
  - Auto-pilot reactions: "एक धीमी श्वास ली" / "सिर हिलाया" / "सिर झुकाया" — use sparingly.
  - "रक्त-लाल तारा" + "घंटी बजी" motif — banned for 10 chapters after first over-use.
  - Em-dash chopped fragments as the default — use flowing 2–4 sentence paragraphs. Em-dash only at action peaks / climactic reveals.

## Structural rules (high-signal subset)

- **Sensory grounding:** Every scene should anchor 2–3 sensory details (sound, smell, light, touch). Internal-monologue-only chapters are discouraged.
- **Format rotation:** Every 7 chapters, break the template (cold-open → setup → reveal → villain-cut → hook). Rotate in: pure action, pure dialogue, flashback, POV-switch, epistolary, two-thread, slice-of-life.
- **Action quota:** At least 1 physical action scene per 3 chapters.
- **Defeat quota:** **Every major realm transition requires ≥10 prior defeats** for रुद्र (varied: physical, mental, political, social). If 5+ chapters have passed with no defeat, plant one. Defeat-tracker is at the bottom of `CLAUDE.md`.
- **Character-limit per arc (खण्ड, 7 chapters):** 2–3 main characters. New character intro = 1–2 lines establishing appearance and habit.
- **10-defeats rule applies per फ़ेज़ as well** — don't cluster all defeats in early फ़ेज़.
- **Time-tracking:** Every ~50 chapters, drop one mention of दादा जी's 5–7 year countdown so stakes stay alive.

## Current story state — quick anchors

(Detailed state in `CLAUDE.md`. If `CLAUDE.md` is more than a few days stale, **recompute the highest chapter number** before quoting "next chapter" — that field drifts.)

As of the most recent chapter files: **अध्याय 1–77 written**. Next = `अध्याय_078.md`.

- रुद्र: 16, with रक्त-रत्न अंश; sealing is cracking but देह-शोधन not yet started.
- Active party: रुद्र, दादा जी, गुरु ज्ञानेश्वर, राज.
- Active pursuer: विक्रम (क्रूरसेन's शुद्ध-मार्ग महा-3 मोहरा), 1 day behind.
- Next narrative waypoint: दोआबा कस्बा (a वैद्या who can cut the काली-विद्या seal).
- Villain arc: क्रूरसेन approaching from the south.

## Workflow conventions specific to this repo

- **Do not commit** unless the user explicitly asks. The user is the only one who triggers commits.
- **No tests, no lint, no typecheck** — there is nothing to run. The "verification" for a chapter is reading it back, checking word count (`(Get-Content ... -Raw).Split('\s+').Count` works on PowerShell 5.1), checking it doesn't violate Writing-Rules, and verifying continuity with the previous chapter.
- **No build artifacts, no migrations, no codegen** — pure text.
- **Branching / PR conventions:** None documented. Default to whatever the user does; ask if unclear.
- **Secrets:** `setting.json` contains an `ANTHROPIC_API_KEY`. Do not paste, log, or commit it. If a future task requires sharing config, redact the key first.

## Common mistakes to avoid

1. Treating this as a code project (no `npm test` will ever exist).
2. Writing `Chapter 1` or `अध्याय एक` instead of `अध्याय 1` (English digits only).
3. Using Roman script in any chapter text.
4. Skipping ahead — chapter numbers must be sequential, no gaps.
5. Overwriting an existing `अध्याय_NNN.md`.
6. Compressing a 5000+ word scene instead of splitting into `.1` / `.2`.
7. Inserting `[SFX: ...]` or `[संगीत: ...]` blocks — banned in chapter text.
8. Quoting "अगला = अध्याय 064" from `CLAUDE.md` without re-verifying — the value drifts; always check the actual filesystem.
9. Adding characters to the story without updating `List of Characters.txt`.
10. Forgetting the `उप-भाग` boundary in chapter 71 — chapters 1–70 live in उप-भाग A, 71+ in उप-भाग B. New chapters in the same arc must respect the existing folder.

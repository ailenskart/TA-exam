# 🎖️ Territorial Army Exam Trainer — 12 July 2026

A zero-install study app for the TA CBT. Open `index.html` in any browser
(phone or laptop) — no server, no internet needed. Progress is saved on the
device automatically.

**Question bank (Phase 1):** 1,463 questions · 25 topics · extracted from `Final_V4.xlsx`.

## The exam it mirrors

| | |
|---|---|
| Date | 12 July 2026, Computer Based Test |
| Paper | 100 MCQs · 100 marks · 2 hours |
| Sections | Part 1 Reasoning (40) → Part 2 GK incl. Current Affairs (30) → Part 3 English (30) |
| Marking | +1 correct · **−0.33 wrong** · 0 skipped |

## Modes

- **🎲 Learn** — random questions one at a time with instant feedback,
  explanation and memory cue. Weighted shuffle: unseen and previously-wrong
  questions appear far more often than ones you've mastered (Leitner-style
  spaced repetition — answer a question right 3 times in a row and it
  almost stops appearing).
- **🔁 Revise** — only questions you got wrong or ⭐ starred. Clear the list to zero.
- **⏱️ Full mock** — exact exam simulation: 100 Qs in real section order,
  120-min timer, no feedback until submission, skip button (no penalty),
  +1/−0.33 scoring, section-wise scorecard and full review of mistakes.
- **⚡ Quick mock** — same format at quarter size (25 Qs / 30 min) for daily drills.
- **📘 Basics** — each topic's methods, formulas and traps from the workbook.
- **📊 Stats** — coverage and accuracy per topic; weakest topics are obvious at a glance.

Keyboard shortcuts: `A–D` / `1–4` answer · `Enter`/`Space` next · `S` skip (in mocks).

## Suggested routine (33 days out)

1. **Daily (40+ questions):** one Learn session — the app feeds you new + weak material automatically.
2. **Daily (5 min):** clear the Revise queue before starting new questions.
3. **Every 2–3 days:** one ⚡ Quick mock to keep exam pace.
4. **Weekly, and the last 7 days:** ⏱️ Full mock under real timing. Practise the skip discipline — a wrong guess costs 0.33, a skip costs nothing.
5. Read **📘 Basics** for a topic before first practising it.

## Adding Phase 2 questions

Add rows/sheets to the workbook in the same column format, then run:

```bash
pip install openpyxl
python3 extract_data.py <workbook.xlsx>
```

This regenerates `data.js`; the app picks up the new questions automatically
(existing progress is keyed per question and is preserved).

## Files

- `index.html` — the app (single file, works offline)
- `data.js` — generated question bank
- `extract_data.py` — workbook → `data.js` converter
- `Final_V4.xlsx` — Phase 1 source workbook

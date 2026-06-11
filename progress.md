# Ben's progress

> The tutor's memory. Read at the start of every session, updated as we
> go. Lives in your project folder so it pushes to GitHub with your work.

- **Started:** 2026-06-09
- **Last updated:** 2026-06-11
- **Curriculum version:** v1

---

## About me (from the session 1 diagnostic)

- **Name:** Ben
- **Self-assessed level:** Near-absolute beginner. Some childhood experience with DOS and QBasic (~30 years ago) — has a vague intuition about command lines and what code does, but treats as a fresh starter.
- **Interests:** Music, photography, comedy
- **Want to make / fix:** A website that actually represents him (decision paralysis + difficulty selling himself gets in the way); VST plugins (software instruments/effects for music production)
- **Day-to-day apps:** YouTube, WhatsApp, Duolingo. Wants to make more use of his phone.
- **Tangent tolerance:** Mostly on task, occasional tangent fine
- **Free notes:** VST plugins is an ambitious long-term goal — good north star. Website hesitation seems self-confidence related as much as technical. Keep that in mind when framing what we build.
- **GitHub:** SmashyBen

---

## Where I am right now

Session 4 complete. Steps 1–9 done. Next: Step 10a — The look-back (the bookend).
Mood-music page live at: https://smashyben.github.io/my-claude-project/step-2/mood-music.html
Repo public at: https://github.com/SmashyBen/my-claude-project

---

## Step-2 artefact (the bookend)

- **What it is:** Music mood page — type or pick a mood, get a genre and vibe description
- **File:** `~/Documents/my-claude-project/step-2/mood-music.html`
- **The original prompts used:** "I want to build a page that allows me to name a mood, and for the page to show me a genre of music, and a description of the vibe of that kind of music."

> The tutor must keep this section intact. Step 10a depends on it.

---

## Curriculum progress

### Core (v1)

- [x] **Step 1 — What an AI agent is + the prompt → action → review loop**
  Notes: Nailed it first time. Described the loop accurately in his own words — particularly good on review: "making sure what you did is what I had in mind."

- [x] **Step 2 — First prompts + the tiny build**
  Notes: Built mood-music.html. Ben typed the first prompt himself. Iterated with good feedback — added chill/relaxed moods, multiple genres per mood with random selection, colour theming per mood, combined mood input, Jamendo API integration for real audio playback, light/dark theme with browser-preference detection and manual toggle. Strong instincts throughout — rule-of-thirds positioning, combining the input/dropdown, noticing the heading contrast issue in light mode. File lives at step-2/mood-music.html.

- [x] **Step 3 — Good prompts vs bad**
  Notes: All four principles landed cleanly — Ben had already been applying most of them instinctively. Rewrote the original mood-music prompt from scratch unprompted; the result was genuinely strong (purpose, UI specifics, numbers, edge cases, design intent). Named "rule of thirds" as an example of show-don't-tell. No friction on any principle.

- [x] **Step 4 — Working with files**
  Notes: Mental model landed cleanly — Ben described the visibility boundary in his own words ("in my claude project, you can see only that folder"). Used @ himself twice: once to describe the file, once to request a specific change (random playlist start). Narrate-then-edit cycle worked well; read the plain-English explanation and said go before the change ran.

- [x] **Step 5 — Reviewing AI output critically**
  Notes: Predict-then-check habit landed cleanly. Seeded a failure (added Focused to datalist only, missing moods data and themes). Ben gave a thorough three-part prediction, tested it, caught the failure immediately and described it clearly. Second attempt matched prediction. Good instincts throughout.

- [x] **Step 6 — Git as a safety net (local commits)**
  Notes: Showed the git log — Ben saw all 10 checkpoints. Made a throwaway subtitle change, Ben asked to undo it, watched it roll back. Described what happened in his own words accurately: "made a change, then undid it by loading the last restore point." Clean.

- [x] **Step 7 — GitHub: moving your save-points online**
  Notes: GitHub account created (SmashyBen). GitHub CLI installed, authenticated, repo pushed to github.com/SmashyBen/my-claude-project (private). Becky (BeckyFLT) granted read access. Commit vs push: initially had it reversed, corrected cleanly and confirmed understanding.

- [x] **Step 8 — Planning before building**
  Notes: Planned Git Fiddler — a standalone low-latency guitar processing app. Ben described the problem clearly before the solution. Signal chain: pre-IR VST bank (3 slots) → IR loader with inline browser → post-IR VST bank (3 slots). Tuner taps input. Tech: JUCE/C++. Ben answered all three blocking questions unprompted and refined the design (two banks split at IR). plan.md written and pushed.

- [x] **Step 9 — Troubleshooting and recovery**
  Notes: Key move landed immediately — "I wanted to tell you what happened and ask you to fix it." Knew instinctively that fixing happens through prompts, not by opening files. All five troubleshooting prompts taught. Ben then used two of them unprompted on a real bug (@ to point at the file, named the gap: "expected both genres, only first plays"). Investigated, fixed (split all combined genre entries into separate ones with unique descriptions), verified. Full loop in one go.

- [ ] **Step 10a — Remake the tiny build (the bookend)**
  Notes:

- [ ] **Step 10b — The real project**
  Project idea: VST plugin / website that represents Ben
  Notes:

### On-demand topics (filled in if/when they come up)

---

## Session log

- **Session 1 — 2026-06-09:** Diagnostic complete. Ben: childhood DOS/QBasic, interests in music/photography/comedy, wants to build a website and VST plugins. Step 1 nailed first time — great instinct on the review beat. Step 2 in progress: built mood-music.html, Ben typed his own first prompt and gave sharp iterative feedback (added moods, random genre pools, colour theming). Good session — confident start.
- **Session 2 — 2026-06-10:** Steps 2 and 3 complete, plus extra polish on mood-music.html. Combined input/dropdown into datalist, rule-of-thirds layout, Jamendo API with perpetual playlist engine (auto-advances, pre-fetches, next → skip button), light/dark theme with browser-preference detection and manual toggle, heading contrast fix, clears input on focus. Step 3: all four prompting principles landed cleanly — Ben rewrote the original brief from scratch and produced a genuinely strong one. Ready for Step 4 (working with files).
- **Session 3 — 2026-06-10:** Steps 4–7 complete. File/folder mental model landed quickly. Ben described the visibility boundary in his own words. Used @ twice himself. Predict-then-check: seeded failure (incomplete Focused mood), Ben caught it immediately. Git: showed log, demonstrated undo, Ben described it accurately. GitHub: account created (SmashyBen), repo pushed, Becky invited. Commit vs push clarified. Ready for Step 8 (planning before building).
- **Session 4 — 2026-06-11:** Steps 8 and 9 complete. Step 8 done last session (Git Fiddler plan). Step 9: troubleshooting toolkit taught, Ben applied it immediately to a real bug — combined genre entries in mood-music.html only ever played the first genre. Spotted it himself, wrote a strong troubleshooting prompt using @ and gap-naming. Fixed by splitting all combined genres into individual entries with unique descriptions. Full recovery loop completed.

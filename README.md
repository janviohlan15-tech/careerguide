# Multiverse Career Guide

A human-centred, responsive career exploration prototype for students after Class 12. It is a static HTML/CSS/JavaScript application: no backend, account, database, build tool, or external AI service is required.

The interface uses a premium deep-navy and indigo visual system with cyan accents, a motion-aware animated landing hero, a student dashboard, and a one-question-at-a-time assessment. Brand tagline: **Discover Your Potential. Design Your Future.**

## Run locally

From the project directory:

```powershell
py -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000). If the Python launcher is unavailable, use `python -m http.server 8000`. You can also open `index.html` directly, but a local web server is recommended.

Stop the server with `Ctrl+C`.

## What is implemented

- **Student dashboard and Career DNA:** Save education level, stream, strongest subject, estimated marks, self-reported interest, strengths, annual budget, study mode, location and goals. Review recent activity, progress and signal-led career suggestions.
- **Objective practice quiz:** Ten MCQs with answer explanations, correct-answer counts across five areas and an explicit comparison between stated interest and quiz evidence. The short custom quiz is not a validated psychometric or aptitude test.
- **Pathway Match:** Transparent interest, quiz-answer and subject-signal ranking; pathway descriptions, subjects to explore, indicative study-duration ranges, eligibility checks, trade-offs and alternatives. Nothing is an admissions determination.
- **College Compass:** Search and filter invented sample course records by budget, stream, location and example scholarship-information status; select up to three for side-by-side comparison. All colleges, courses and fees are fictional interface-test data, not verified institutions or current admissions facts.
- **AI Mentor:** A deterministic, contextual rule-based demo with follow-up prompts. It does not call an AI model or search the web.
- **What-if Simulator:** Compare pathway ordering and illustrative course samples under different stream, marks, interest, budget, study-mode and location inputs without changing the saved profile.
- **Skill-gap Quests:** Pathway-specific activities with milestones, completion tracking and local persistence.
- **Demo controls:** Load Science, Commerce or Arts/Humanities sample profiles, or reset the locally stored demo.
- **Responsive and accessible basics:** Mobile layouts, labelled inputs, keyboard-operable controls, visible focus, live status messages and a skip link.

## Persistence and privacy

Profile details, quiz answers/results, saved pathways and quest completion are stored in this browser's `localStorage`. This is local demo persistence—not secure server-side storage, account sync, backup or a suitable place for sensitive personal information. Avoid entering sensitive data. Use **Reset demo data** to clear this app's saved key in the current browser.

## Render deployment

1. Push the project root (including `index.html` and `render.yaml`) to a Git repository.
2. In Render, create a **Static Site** and connect the repository, or create a Blueprint from `render.yaml`.
3. Use the repository root as the publish directory (`.`). No build command is needed.
4. Deploy and open the generated site URL.

There are no secrets or environment variables. No API key is required; the Mentor is intentionally labelled as a local rule-based demo. Do not add a provider key to frontend code.

## Manual smoke-test checklist

1. Navigate through each tab and check the profile, quiz, pathway, college, simulator, quest and Mentor screens.
2. Try saving a profile with empty or out-of-range marks, then save valid marks.
3. Submit the quiz incomplete, then answer all 10 questions and review scores and explanations.
4. Save/remove a pathway and confirm it appears in the dashboard.
5. Search colleges and change budget, stream, location and scholarship-info filters.
6. Change simulator inputs and check that its scenario comparison does not overwrite the saved profile.
7. Complete and un-complete a quest; refresh and confirm saved progress remains.
8. Ask the demo Mentor a question, try an empty prompt and clear the chat.
9. Refresh and verify persistence; use **Reset demo data** only when you intend to clear it.

## Production limitations and next steps

- College data and course/fee examples are invented. Replace them only with records checked against official sources and show source, academic year and verification date.
- Assessment content and transparent matching rules are educational prototypes, not validated career advice or admissions rules. Seek educator/counsellor review before real-world use.
- There is no login, backend, shared admin area, live college search, real AI, or data export.
- Before collecting real student data, add consent, privacy/retention controls, authentication and a secure backend. Keep credentials server-side.

# Product and technical notes

## Student journey

Dashboard → Career DNA profile → objective reasoning quiz → evidence comparison → pathway shortlist → College Compass → what-if scenario → skill quest → rule-based Mentor.

## Experience design

The static single-page interface uses a deep navy/indigo and cyan-accented SaaS visual system, animated landing hero, feature and journey sections, responsive top navigation, stream-filtered pathway cards, one-question-at-a-time assessment, sample-labelled reflections, and reduced-motion support. The dashboard includes personal summary, top demo signals, recent activity and next-step actions.

## Architecture

- One self-contained `index.html` with inline CSS and JavaScript.
- Static hosting (Render Static Site); no API server, database, build tool or external dependency.
- `localStorage` stores this browser's profile, quiz answers and result, saved pathway keys, college comparison selections, quest completion and recent activity. It is not secure server-side storage or cross-device persistence.

## Evidence and recommendation rules

- Quiz results count correct answers from two short custom questions in each of five exploration areas. Each answer has a visible explanation after submission.
- The stored, self-reported interest is kept separate from quiz results and explicitly compared in the result view.
- Pathway order is a transparent demo score: +3 for a matching stated interest, +2 per correct quiz answer in that area and +1 for a related strongest subject. Ties are alphabetic. Marks are shown as context in the simulator/profile and are not an eligibility cutoff or scoring signal.
- Displayed pathway percentages are this demo score divided by its maximum possible value (8), labelled as signal alignment and not a success probability.
- Neither the quiz nor ranking is a validated assessment, career prediction or admissions decision.

## Data integrity

All College Compass and simulator institution/course/fee records are invented illustrative data. Scholarship notes and stream references are also demo-only. They must not be used as current admissions, fee, aid or accreditation facts.

## External services and roles

The Mentor is local deterministic rule-based guidance—not a live AI or web search. No API key is required or expected in the client. The prototype has no login, backend, shared admin panel or production role system.

## Production readiness

Before a student-facing pilot, have qualified educators/counsellors review assessment and pathway language. Replace sample colleges only with officially sourced and dated records. Add consent and privacy/retention processes, authentication and authorization, and a secure backend before collecting real personal data. Keep credentials server-side.

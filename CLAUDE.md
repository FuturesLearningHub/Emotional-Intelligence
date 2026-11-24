# Emotional Intelligence & Interpersonal Skills — Vanderbilt Learning Series

Single-page interactive classroom experience (Learning on Demand). Live at
https://futureslearninghub.github.io/Emotional-Intelligence/ (GitHub Pages, `gh-pages`
branch — publish with `git branch -f gh-pages main && git push -f origin gh-pages`).

Sister programs: AI_Classroom (AI Basics), AI-Advanced (AI 201),
Difficult_Conversations, Coaching-for-Performance; catalog at
FuturesLearningHub/FLH-Learning-Library-. Same engine, same standing principles.

## Standing design principles (do not regress these)

1. **Simulators, practice, and play throughout.** Every teaching section
   has an interaction; the NVC Reframe Lab and the triad listening drill
   are the signature pieces, Guess the Number is the skeptic-converter.
2. **A reason and facilitation behind every activity.** Learner-visible
   "Why this matters" lines; activities labeled As a group / On your own
   with steps, timings, and solo variants.
3. **Every section facilitatable, learning validatable.** ATD runbook in
   `facilitator/notes.json`. Kirkpatrick: L1 fist-to-five, L2 recap mapped
   to objectives, L3 commitment card + 7-day pulse + 30-day re-poll.
4. **Facilitator edition is generated, never hand-edited** — run
   `python3 tools/build-facilitator.py` after ANY change to index.html or
   notes.json. Its QR encodes the LEARNER url.
5. **Privacy by design — this course touches real relationships.** Roles,
   never names; the Johari mapper and commitment card are private (nothing
   saved or sent) and must SAY so in learner-visible copy. Never add
   telemetry, storage, or sharing to the personal exercises.
6. **Stay clinical, not clinical-adjacent.** Workplace skills grounded in
   published research (Goleman, Mayer-Salovey, Eurich, Lieberman, Rosenberg,
   Edmondson). This is not therapy; the facilitator notes route personal
   disclosures to EAP/HR privately. Keep politics and DEI framing out.
7. **Brand: Vanderbilt FLH system.** Black #1C1C1C / white / flat gold
   #CFAE70; Libre Caslon Display headlines (one italic word), Inter body,
   Antonio eyebrows; motion ≤400ms; real VU lockups (authorized use only).
8. **No frameworks.** One CSS file, one JS file, vendored QR lib,
   self-hosted fonts; hero montage streams from Higgsfield CDN with the
   particle canvas fallback.

## Layout (15 slides)

Welcome/QR (privacy norms) → Hero (6 objectives + montage) → Agenda →
01 The case for EI (Guess the Number) → manifesto ("You can't manage an
emotion you haven't named.") → 02 The map (domain trainer + Goleman video) →
03 Johari Window (private mapper) → 04 Name it to tame it (label trainer) →
05 Active listening (reply trainer + triad rubric) → 06 NVC reframe
(graded OFNR lab) → 07 Candor with care (Edmondson video + opener trainer) →
Recap quiz → Capstone EI Commitment Card → Glossary → Closing (commitment).

## Editing map

- Copy: `index.html` · Recap: `QUESTIONS` in `assets/js/main.js`
- Trainers: `makeTrainer` configs (statGuess, domainSpot, labelUp,
  replyRate, candorJudge)
- Johari mapper: `johariMap` block · NVC lab: `SLOTS` + reaction tiers
- Capstone maps: `PRACTICE` / `NOT` / `WHEN` in main.js
- Runbook: `facilitator/notes.json` (timing must sum: Full 90 / Core 60)
- Citations to keep honest: Goleman (HBR "What Makes a Leader?"),
  Mayer-Salovey-Caruso ability model, Eurich 95%/10–15% (TEDx
  tGdsOXZpyWE), Lieberman et al. 2007 Psychological Science (affect
  labeling), Rosenberg/cnvc.org (OFNR), Edmondson (TEDx LhoLuui9gX8),
  Project Aristotle, DDI 40%, McKinsey ~26% skill-shift, SHRM respect>pay.

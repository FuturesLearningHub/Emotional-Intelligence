# Emotional Intelligence & Interpersonal Skills — Lead Yourself, Then Lead Others

An interactive, single-page teaching site on the skill research keeps
finding at the center of leadership: noticing and naming emotions, reading
people, listening for real, and saying hard things well. A **Learning on
Demand** program: the facilitator projects it while learners scan a QR code
and work every exercise on their own devices, or share the link for
self-paced review. Private by design — every personal exercise runs on
roles (never names) and nothing typed is saved or sent anywhere.

Part of the Vanderbilt Learning Series. Catalog:
[Course Library](https://me5231979.github.io/Course_Library/) ·
Sister programs: [Navigating Difficult Conversations](https://me5231979.github.io/Difficult_Conversations/),
[Coaching for Performance](https://me5231979.github.io/Coaching-for-Performance/)

- **Learner edition:** https://me5231979.github.io/Emotional-Intelligence/
- **Facilitator edition:** https://me5231979.github.io/Emotional-Intelligence/facilitator/

## Running it

Plain HTML/CSS/JS, no build step:

```bash
python3 -m http.server 8000
```

## What it teaches (7 sections)

1. The case for EI — the hard numbers behind the "soft" skill (Goleman/HBR,
   McKinsey, DDI, Deloitte, SHRM)
2. The map — Goleman's four domains in sequence, with the Mayer-Salovey
   ability model named underneath
3. Self-awareness & the Johari Window — Eurich's 95%-vs-10–15% gap, and why
   only feedback shrinks the blind quadrant
4. Name it to tame it — UCLA affect-labeling neuroscience (Lieberman 2007)
   and emotional granularity
5. Active listening — paraphrase, clarify, withhold judgment, scored against
   a rubric in the triad drill
6. The NVC reframe — Rosenberg's Observation, Feeling, Need, Request
7. Candor with care — Edmondson's psychological safety and Google's Project
   Aristotle; safety plus standards, not niceness

Ends with a scored recap, the **EI Commitment Card capstone** (one
relationship, one practice, one named failure mode, one date), a flip-card
glossary, and a commitment close. `worksheet.html` mirrors the capstone on
paper; `cheatsheet.html` is the take-home reference.

## The interactive tools

| Slide | Tool | What learners do |
|---|---|---|
| The case | **Guess the number** | Call four research findings before the reveal; missed guesses stick |
| The map | **Name the domain** | Read five workplace scenes and name the EI domain at work (or missing) |
| Johari | **Map your window** | Privately write an Open, Hidden, and suspected Blind item; rendered as their window |
| Name it | **Upgrade the label** | Pick the precise emotion label over the foggy one, five rounds |
| Listening | **Rate the reply** | Pick the reply that's actually listening (vs advice, me-too, steering) |
| NVC | **The Reframe Lab** | Rebuild a charged accusation part by part and watch the reply change |
| Candor | **Judge the opener** | Call five opening lines: candor with care, harshness, or dressed-up avoidance |
| Recap | **Scored quiz** | 6 questions mapped to the objectives |
| Capstone | **EI Commitment Card** | Build and copy a dated, private behavior-change card |

## Instructional design

- **Bloom's ladder:** objectives run Explain/Identify → Name/Apply →
  Practice/Analyze (rubric) → Reframe/Evaluate → Commit (Create).
- **Kirkpatrick:** L1 fist-to-five at close; L2 inline checks + recap;
  L3 commitment card + 7-day pulse + 30-day self-check re-poll (templates
  on the facilitator briefing slide).
- **Adult learning:** learners bring one real relationship with friction
  (pre-work), every exercise runs on their own material held privately,
  and the capstone ships as a dated first rep within a week.
- **Privacy by design:** roles not names; the Johari mapper and commitment
  card state explicitly that nothing is saved or transmitted.

## The facilitator edition

Generated at `/facilitator/` by `python3 tools/build-facilitator.py` from
`facilitator/notes.json` — ATD-scripted rails (Say / Do / Ask with expected
answers / Debrief / Transition), a briefing slide (prep, materials,
contingencies, tough questions, three copy-paste templates), Full 90 /
Core 60 timing. Its QR encodes the learner URL.

## Editing map

- Copy: `index.html` · Recap: `QUESTIONS` in `assets/js/main.js`
- Trainers: `makeTrainer` configs (stats, domains, labels, replies, openers)
- Johari mapper: `johariMap` block · NVC lab: `SLOTS` in main.js
- Capstone maps: `PRACTICE` / `NOT` / `WHEN` in main.js
- Runbook: `facilitator/notes.json` (timing must sum: Full 90 / Core 60)
- Citations to keep honest: Goleman "What Makes a Leader?" (HBR),
  Mayer-Salovey-Caruso, Eurich (self-awareness, TEDx), Lieberman et al.
  2007 (affect labeling), Rosenberg / cnvc.org (NVC), Edmondson (psych
  safety, TEDx), Google Project Aristotle, DDI (empathy), McKinsey (skill
  shift), SHRM (respect).
- Publish: `git push origin main && git branch -f gh-pages main && git push -f origin gh-pages`

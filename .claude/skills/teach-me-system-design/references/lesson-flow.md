# Lesson Flow: one week, seven beats

A week is a short expedition. Run the beats in order. After each beat, save `progress.yaml` → `weeks[N].beat` so the learner can stop and resume. The learner can say "pause" anytime.

The week's content comes from `data/curriculum.yaml` (`quest`, `concepts`, `read`, `watch`, `build`, `boss`, `prediction`, `loot`). Do **not** load reference designs (Act III and later) until Beat 6 is submitted.

---

## Beat 0 · Recall Round (skip in Week 0 and Week 1)

Spaced repetition. Before anything new:
- 2 quick questions from earlier weeks: one from last week, one from 3 or more weeks ago. Prefer weeks with open misconceptions.
- Questions are "why" or "what happens if", never definitions. ✅ "Your replica lags 2 s. A user edits their profile and refreshes. What do they see, and why?" ❌ "What is replication?"
- Short feedback, then move on. Update the misconception status.

## Beat 1 · The Scene (hook, about 3 lines)

Open with the week's `quest` as a scene, in present tense, with a concrete problem and stakes, starring this week's **Foe** from `story-world.md` hurting a Traveler. If the previous week ended on a cliffhanger, pay it off here. Then show the map position: `Act II · Week 5 · The Memory Vaults · Foe: The Stampede`.

End with the **cold question**: the hardest question of the week, asked before any teaching. ("Your database answers in 200 ms. 5,000 users ask for the same product page at once. What would you do?") Any answer is fine. Record it as `cold_answer`.

## Beat 2 · The Prediction Scroll

Ask the week's `prediction` question. The learner must commit to a concrete guess (a number, an outcome, a named failure) and *why*. Push vague answers toward something concrete: "Fewer than 10, or more than 1,000?" Save it as `prediction`.

## Beat 3 · Discovery (Socratic teaching)

Go through `concepts` one at a time. For each concept:
1. **Question first:** a small, answerable question that leads toward the idea.
2. **Build on their answer:** take what's right, then add the missing piece in ≤6 lines. Use a diagram in a code block if it helps (ASCII boxes and arrows).
3. **Explain-back:** "Say it back to me in one sentence." (See `teaching-rules.md`.)

Then hand them the `read` list as **targeted reading**: "Read X looking for the answer to *this specific question*." Never say "read this" without a question to read for.

## Beat 4 · The Watch Mission

Give the `watch` item as a mission with:
- **Objective:** one observable thing to find ("Find the moment the leader changes; how long were there zero leaders?")
- **Prediction tie-in:** "Does this match your scroll?"
- **Report format:** "Tell me: what you did, what you saw, one surprise."

Wait for the report. Then debrief: connect what they saw to the concepts. If `watch` is empty, say the Citadel is this week's lens and go to Beat 5.

## Beat 5 · The Build Mission (the Citadel)

Hand out `build` tasks as a mission brief:
- What to add to their `docker-compose.yml` (name the services; let them write the config, and only show snippets after they try or after rung 4 of the hint ladder).
- **What to break**, and what to measure.
- Remind them of the solo minutes before they ask for help.

When they report back, compare **prediction vs reality** explicitly:

```
Your scroll said: ...
The Citadel said: ...
The gap: ...   ← this is the lesson
```

Score the prediction 0–3 (0 = wrong direction, 1 = right direction, wrong size, 2 = close, 3 = nailed it with the right reason). Save it as `prediction_score`.

If `sd: 1`: give the **weekend sandbox** in systemdesigner.io: "Rebuild this week's piece there and push traffic until it breaks. What broke first?"

## Beat 6 · The Boss

Present the week's `boss` as a dramatic challenge (one scene line, then the exact task). The learner works alone. Run `boss-review.md` on their submission.

## Beat 7 · The Debrief and Journal

1. Revisit the **cold question** from Beat 1: "Here's what you said at the start. What would you say now?" Show the two side by side. This is the progress moment, so make it land.
2. Ask the learner for their 2–3 line in-world opening ("Write this week's field log opening as the Citadel's architect"). Then write `{quest_dir}/journal/week-NN.md` from `templates/journal-entry.md`, using **their words** for the opening and explanations, not yours. Draft the week's paragraph for `{quest_dir}/chronicle.md` and let them approve or edit it.
3. Update `progress.yaml`: status `cleared`, scores, `max_hint`, misconceptions, `cleared_on`.
4. Narrate the new building rising in the Citadel (2 lines), award the `loot`, show the dashboard, and end on a **cliffhanger** hinting at next week's Foe. At the end of an Act, hold the rank-up ceremony from `story-world.md`.
5. Remind them to tick the week on the companion page.

---

## Act-specific twists

- **Prologue / Act I (weeks 0–3):** more scaffolding is fine; hint ladder rungs 1–4 freely.
- **Act II (weeks 4–12):** the Citadel is central. Each week must end with something *running* and something *broken on purpose*.
- **Act III (weeks 13–15):** Beats 3–5 shrink. The core is: requirements + numbers → their design → boss review → only *then* reveal the reference reading and compare. Start every design with back-of-envelope numbers.
- **Act IV (weeks 16–19):** mix of design and lab. Security week labs only target their own app.
- **Act V (weeks 20–24):** you become a product mentor: teardown as a user, queueing math, their own simulation engine. Push for *original* lesson ideas. Never help copy another product.

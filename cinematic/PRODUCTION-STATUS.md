# Where this stands

**Updated:** 2026-08-25 · **Expected balance: 463.2 credits**

## The film in one table

| Status | Shots | |
|---|---|---|
| **Clip approved** | 2, 4, 8, 10 | 4 of 11 |
| Candidate after retry | 1, 11 | likely usable after visual check |
| Needs edit/visual decision | 5 | improved, but still brightens |
| Needs a different approach | 3, 6, 7, 9 | the tool will not do these cleanly |
| Built in the editor | 12 | title card |

All 11 still frames are approved and live in `approved/`. The rulebook, storyboard, prompts, sound
direction, web integration, social cut-downs and learning guide are all written. The detailed
record — every measurement, job id and failed attempt — is in `shot-lists/production-tracker.md`.

## What was learned today, in order

**1. The cheap model was the problem.** The first four motion tests used `seedance_2_0_mini` to save
money and three failed. Re-running shot 4 on `seedance1_5` fixed it first try — and that model costs
**2.4 credits a clip against mini's 7.6**. The cheap option was three times more expensive.

Two traps worth remembering: `seedance_2_0`, the model the original plan called for, **cannot be
used on this account** ("Requires plus plan or higher"), and the **cost preflight quotes 4.8 when
the real charge is 2.4** — it neither warns about plan limits nor prices accurately. Trust the
balance, not the quote.

**2. There are three kinds of shot, and only two of them work.**

- **Camera and light, nothing else asked** — shots 2, 4, 8, 10. All four passed. This is reliable.
- **Exposure discipline** — telling the model what must *not* change fixed the pulsing on shot 4 and
  the blown window on shot 11. Shot 1's second attempt also appears to have fixed the fade and
  foreground wipe. But it is not dependable when the frame is nearly one tone: shot 5 still brightens
  across the clip, even after dropping the paper choreography.
- **Anything that has to perform an action** — a hand pressing once, papers sliding into alignment.
  **Asked three times, refused three times.** This is not a prompting problem to solve.
- **Cyan spill in a room-scale shot** — shot 6 kept turning the thin line into a wall/floor glow.
  Stronger "do not spill" wording did not fix it, so the shot needs a new approach.

**3. So the film must not rest on a generated performance.** Shot 9 is the emotional beat of the
whole piece and is exactly what the tool cannot deliver. The best answer is almost certainly to hold
the approved still for its 2.5 seconds and let the sound design carry the press. Shots 3 and 7 have
the same shape and probably the same answer.

## Next step

Review the four new MP4s by eye. If shots 1 and 11 pass visually, lock them. Decide whether shot 5
can be graded/trimmed into the edit or should become a held still. Do not keep regenerating shot 6
with the same travelling-line prompt; rewrite it, hold the still, or cut around it.

Then decide the approach for 3, 7 and 9 — held stills with sound, or shots rewritten so nothing has
to act — and the film is ready to edit.

## Plain-language summary

Four of the eleven moving scenes are finished and good. Two more, shots 1 and 11, were retried and
look promising from the measurements, but still need a human eye check. Shot 5 improved but still
gets brighter. Shot 6 is the stubborn one: the computer keeps turning the thin cyan line into a glow
on the walls and floor, so we should stop asking for that version of the shot. Shots 3, 7 and 9 are
still best solved with held photographs and sound unless we rewrite them so nothing specific has to
happen on screen.

# Production tracker — From Chaos to Intelligence

**Updated:** 2026-08-25 · **Still frames: 11 of 11 approved** · **Video: 4 of 11 clips approved, 2 new candidates**

The tables below are kept in the order they were written, so the reasoning at each stage stays
visible. The current position is at the bottom, under **Shot 4 A/B**.

| # | Shot | Act | Length | Still frame | Video | Result |
|---|---|---|---|---|---|---|
| 1 | Scattered documents | 1 | 3.0s | ✅ v1 | ❌ v1 | Clip fades 49% dark and a black band wipes across frame. Retry — see batch of five |
| 2 | The disconnected room | 1 | 3.5s | ✅ v1 | ✅ v1 | Clip passed first try. Symmetry holds, monitors properly mismatched, blacks stay deep |
| 3 | Notifications in glass | 1 | 3.0s | ✅ v1 | ☐ | Passed. Hand correct, ring on ring finger. Setting reads domestic — see note below |
| 4 | The line is born | 2 | 3.0s | ✅ v1 | ✅ v2 | Motion solved on Seedance 1.5 Pro — line grows from a point at constant brightness. See A/B below |
| 5 | Order from above | 2 | 3.5s | ✅ v1 | ⚠ v1 | Clip lifts blacks 70% and moves too fast; papers never perform the alignment. Retry without the choreography |
| 6 | The room syncs | 2 | 3.5s | ✅ v2 | ⚠ v1 | Line and monitor sync are right, but the cyan glow floods the wall — the same fault that failed the still |
| 7 | Verification | 3 | 3.0s | ✅ v1 | ☐ | Passed. Green confirmation exactly right. Push interface text smaller in the video pass |
| 8 | One system | 3 | 3.5s | ✅ v1 | ✅ v1 | Best frame in the set. Its mini clip is usable as-is — do not spend credits remaking it |
| 9 | The decision | 3 | 2.5s | ✅ v2 | ☐ | v1 had the ring on the wrong finger. v2 fixed and anatomically clean |
| 10 | Craft | 3 | 3.0s | ✅ v1 | ✅ v1 | Best clip in the film. Controlled arc, light sweeping the grooves, cyan rim held thin |
| 11 | Dawn | 4 | 4.0s | ✅ v2 | ⚠ v2 | Window blowout fixed. Framing drifts right — one more attempt aimed only at composition |
| 12 | Title card | 4 | 4.5s | — | ☐ | Built in the editor, never generated |

**Total: 40.0 seconds**

## Credits

| | Credits |
|---|---|
| Starting balance | 70 |
| 3 test frames (shots 10, 1, 4) | −6 |
| 8 remaining frames | −16 |
| 3 regenerations (shots 6, 9, 11) | −6 |
| **Remaining** | **42** |

Hit rate: 8 of 11 passed first time. Three needed one regeneration each. No shot needed more than two attempts.

## Open notes

**Shot 3 — the one continuity risk.** It reads domestic: dark wood, table lamp, a curtain. Walnut
is on the approved materials list so it is not a rule break, and the frame itself is excellent —
the ring in particular says "a person" faster than anything scripted. But it is the only frame
that could look like a different location. Two credits regenerates it in the office if you want
consistency over the current image.

**Shot 5 — storyboard mismatch.** The plan says straight-down overhead; the frame is a high
oblique. The oblique gives better depth and still reads as order. Either update the storyboard to
match the frame, or regenerate to match the storyboard. The frame is the better picture.

**Grading notes for the edit** — none of these need regenerating:
- Shot 2 sits a stop brighter in the mid-greys than the rest of act 1
- Shot 4's cyan reads greener than the brand `#55d8e8`, and spills slightly onto the paper face
- Shot 7 has a mild overall teal cast, and its readable lines repeat "LINE 123"

## Next step

Turn approved stills into video. Each approved frame becomes the opening frame of its clip, with
a short movement-only prompt from `prompts/shot-prompts.md`.

| Option | Cost | Leaves |
|---|---|---|
| All 11 clips at 720p (`seedance_2_0`) | 198 | not affordable on 42 |
| All 11 clips at 720p cheap (`seedance_2_0_mini`) | 110 | not affordable on 42 |
| **4 hero clips at 720p mini** (shots 4, 8, 9, 11) | **40** | **2** |
| 2 hero clips at 720p (`seedance_2_0`) | 36 | 6 |

With 42 credits the honest move is a small number of motion tests, not the whole film. Shot 4 is
the one to test first — if the cyan line moves correctly, everything else will.

## Where files are

- `generated/` — all 14 frames including the 3 rejects, kept as evidence of what does not work
- `approved/` — the 11 winning frames, named `shot-NN-keyframe.png`

---

# Motion tests — 2026-08-25

Four clips generated from approved frames, `seedance_2_0_mini` at 720p, 4 seconds, silent.
40 credits. **2 credits remaining.**

| Shot | Result | What happened |
|---|---|---|
| 4 · The line is born | ⚠ Partial | Camera glide works. **The cyan line pulses** — faint, then bright, then nearly gone by the end. It should extend and stay. Breaks rule 4 of the motif. Also drifts warm across the clip |
| 8 · One system | ✅ Pass | Best of the four. Cyan lines hold steady with no pulsing, amber lamp stays, dawn genuinely warms from blue to pink. Camera drifts sideways instead of rising, but the move is slow and controlled |
| 9 · The decision | ⚠ Partial | **Anatomy holds** across all frames — fingers stay distinct, ring stays on the ring finger. But the hand shuffles and repositions instead of making one deliberate press. Wrong action on the film's most important beat |
| 11 · Dawn | ⚠ Partial | Real forward glide and strong dawn warming, but it travels much further than "almost imperceptibly", drifts off the centred composition, and the window blows out to a hot glare by the end |

## The lesson worth keeping

**Stills passed 8 out of 11 first time. Motion passed 1 out of 4.** Motion is roughly three times
harder to get right, and the failures are different in kind: a still either matches the rulebook
or does not, but a clip can start correct and go wrong halfway through. Budget accordingly — the
earlier estimate of "add 40% for regeneration" holds for stills and is far too low for video.

Two specific things the generator gets wrong that the prompts must fight harder:

1. **It treats light as something that should pulse.** Any glowing element will brighten and fade
   unless the prompt insists it stays at constant brightness for the whole clip.
2. **It cannot leave a subject still.** Asked for one small action, it adds drift and fidget. The
   prompt has to say what must NOT move, not only what must.

## Corrected motion prompts for the next attempt

- **Shot 4:** `camera slides slowly left at constant speed; the cyan line holds one constant
  brightness for the entire shot and never dims or brightens; the line grows longer along the desk
  edge; nothing else moves; no colour temperature change`
- **Shot 9:** `locked-off camera; the hand stays completely still except for the index finger,
  which presses down once and stops; the wrist and all other fingers do not move at all; no
  drifting, no repositioning`
- **Shot 11:** `camera creeps forward extremely slowly, travelling less than one desk length in
  four seconds; the standing figure stays exactly centred in frame; the sun stays behind cloud and
  never becomes a bright spot; no lens flare`

## Cost to finish

| Item | Credits |
|---|---|
| Redo shots 4, 9, 11 with corrected prompts | 30 |
| Remaining 7 clips (shots 1, 2, 3, 5, 6, 7, 10) | 70 |
| Sensible regeneration allowance for video (~100%) | ~100 |
| **Realistic total to a finished 40-second film** | **~200** |

Shot 8 is already usable as-is.

---

# Shot 4 A/B — prompt vs model — 2026-08-25

Credits were topped up (balance 502). Before spending the ~200 estimated to finish the film, we
tested one question: **were the motion failures caused by the prompt, or by the cheap model?**
Same approved shot-4 still, same corrected prompt, two models. 12.4 credits.

## What was actually measured

The clips were decoded to frames and the cyan pixels counted frame by frame, rather than judged
by eye. "Pulsing" means the cyan gets brighter then dimmer; "growth" means it covers more of the
frame over time, which is what rule 1 of the motif asks for.

| | v1 · mini, old prompt | v2 · mini, fixed prompt | v2 · Seedance 1.5 Pro, fixed prompt |
|---|---|---|---|
| Cyan area over the 4s | 1143 → 2864 → **125** | 1556 → 1759 → 1191 | 1082 → **5350**, rising every frame |
| Swing in cyan area | 96% of peak | 32% | 80% — but all growth, never a fall |
| Swing in cyan brightness | 50.3 | 22.2 | **18.1** — flattest |
| Whole-frame brightness | steady | **62 → 33 (−46%)** | 67 → 58 (−13%) |
| Cost, 4s @ 720p | 7.6 | 7.6 | **4.8** |

## The answer: both, and the cheap model was the bigger problem

**The corrected prompt did work.** On the same model, it stopped the collapse — v1 ended at 11% of
its peak cyan, v2 held at 68%. Telling the generator what must *not* change is the right technique
and should stay in every motion prompt.

**But the prompt alone was not enough.** Mini with the fixed prompt stopped pulsing by holding the
line completely static — it never grows. That breaks rule 1 ("starts as a point and grows
outward"). And it introduced a new fault the old clip did not have: the entire frame fades toward
black across the four seconds, losing nearly half its brightness.

**Seedance 1.5 Pro did what was actually asked.** The line starts as a point on the desk edge and
extends outward at one constant brightness, the exposure holds, and it is still a thin line rather
than a wash. It satisfies rules 1, 2 and 4 of the motif in a single take, first attempt.

**It also costs 4.8 credits against mini's 7.6.** The model that was being avoided to save money
is 37% cheaper and materially better. The four original motion tests were run on the wrong model.

## One honest reservation on the winning clip

In the last second the line continues past the visible desk corner into what reads as open air.
Rule 2 says the line never floats through empty air. It may be following an edge that has left
frame, and at speed it is unlikely to register — but it is the one thing to look at before this
clip is locked.

## Also discovered: `seedance_2_0` is not available on this account

The plan called for the final pass on `seedance_2_0` at 1080p. Submitting to it is rejected with
**"Requires plus plan or higher."** The account is on `basic`. Note that a cost preflight still
returns a price for it (18 credits), so cost checks do **not** reveal plan limits — only an actual
submission does. Seedance 1.5 Pro supports 1080p and is available, so it is the practical path to
a finished film without a subscription change.

## Revised budget

| Item | Credits |
|---|---|
| Remaining 10 clips on Seedance 1.5 Pro @ 720p | 48 |
| 100% retry allowance for video | 48 |
| **Realistic total to a finished 40-second film** | **~96** |

Earlier estimate was ~200 on mini. Balance after this test: **489.6**. The film is comfortably
affordable, and a 1080p final pass (also on 1.5 Pro) is now worth considering rather than ruling out.

## Files

- `generated/shot-04-clip-v2-mini.mp4` — fixed prompt, cheap model, static line and fades dark
- `generated/shot-04-clip-v2-seedance15.mp4` — **the candidate**
- `contact-sheet/shot-04-motion-*.png` — four frames from each clip, side by side

## Generation reference, so this need not be rediscovered

- Approved shot-4 still, uploaded media id: `374aab89-a52b-44b1-8b05-2565fbad7889`
- Job ids: mini `e5c1132d-3efb-4739-b041-c67f1a2c919d` · 1.5 Pro `9c37450b-b28f-44d9-afd6-4adb39b55bbb`
- Working params: `model: seedance1_5`, `duration: 4`, `resolution: 720p`, `aspect_ratio: 16:9`,
  `generate_audio: false`, still passed with role `start_image`

Job ids were not recorded for the first four motion tests, which meant re-uploading the still.
Record them from here on.

---

# Shots 9 and 11 on Seedance 1.5 Pro — 2026-08-25

9.6 credits. Balance after: **484.8**. Same method as the shot-4 test — frames decoded and
measured, not judged by eye. "Motion per frame" is how much the picture changes between frames;
"blown pixels" counts near-white pixels, which is what a window glaring out looks like numerically.

## Shot 11 · Dawn — ⚠ much better, one fault left

| | v1 · mini | v2 · 1.5 Pro |
|---|---|---|
| Blown-out pixels, start → end | 1855 → **3250** | 2516 → **946** |
| Whole-frame brightness | 52.9 → 68.9 (**+30%**) | 53.9 → 56.2 (+4%) |
| Motion per frame | 16.11 | 11.53 |
| Total travel | 43.62 | 38.13 |

**The blowout is solved.** v1 climbed to a hot glare; v2 actually gets *less* bright at the window
as it goes, and the city stays readable behind the figure the whole way. Exposure holds. The move
is calmer.

**What is still wrong:** the framing drifts right. The figure starts just left of centre and ends
clearly right of centre, and the camera pushes further than "almost imperceptibly" — the travel
number only came down 13%, and it accelerates rather than holding one speed. Composition is the
remaining fix, not light.

## Shot 9 · The decision — ❌ still fails, and this is the important finding

| | v1 · mini | v2 · 1.5 Pro |
|---|---|---|
| Motion per frame | 2.31 | **4.16** |
| Peak motion | 4.71 | 8.84 |
| Change from opening frame | climbs steadily, then settles | **oscillates: 3.9 → 9.2 → 6.0 → 11.6 → 6.9 → 9.1** |

Anatomy is perfect — five distinct fingers throughout, ring on the ring finger, no melting. That
problem is genuinely gone.

But the hand still does not make one deliberate press. It slides across the frame, pulls back,
slides again. The oscillating numbers are the tell: a real press would be *stillness, one movement,
stillness*, which shows up as a rise and then a plateau. Instead the picture keeps returning toward
where it started and leaving again. That is fidgeting, and the better model made it more energetic,
not less.

## The lesson worth keeping

**Two different kinds of failure, and only one of them is fixed by paying for a better model.**

- **Photometric faults** — pulsing glow, drifting colour temperature, fading exposure, blown
  highlights. Seedance 1.5 Pro fixed every one of these on shots 4 and 11, first attempt.
- **Choreographic faults** — "do exactly one action", "hold this framing", "keep this subject
  centred". The better model is no better at these. Shot 9 got worse.

The generator will always fill four seconds with movement. It can be told how bright things should
be, but it cannot easily be told to *do less*. Which means: the film's meaning should not depend on
a generated performance. Shot 9 is the emotional beat of the whole piece and it is the one shot the
tool cannot deliver.

Three ways out of shot 9, cheapest first:

1. **Cut around it.** Use the approved still, hold it, and let sound carry the press. It is a 2.5
   second beat and a held frame with the right sound design may be stronger than any animation.
2. **Shorten the ask.** Generate the clip and use only the first second, before the drift starts.
3. **Change the shot.** Ask for something the generator is good at — the cyan glow under the hand
   resolving to green — and keep the hand still by not asking it to act at all.

## Where this leaves the remaining seven

Sorted by which failure class they belong to, which is now the thing that predicts success:

| Risk | Shots | Why |
|---|---|---|
| **Low — camera and light only** | 1, 10 | A dolly and an arc with light sweeping. Nothing has to *act* |
| **Medium** | 2, 5, 6 | 6 is the cyan line again, already proven on shot 4. 5 asks papers to settle into a grid, 2 asks monitors to flicker — both are movement the tool likes doing |
| **High — discrete events** | 3, 7 | Notification banners appearing one by one; check marks resolving down a list. These are the same class as shot 9: specific things happening in a specific order |

Suggested next batch: **shots 1, 2, 5, 6, 10 together — 24 credits.** Leave 3, 7 and 9 until the
approach for staged events is settled, because generating them now just buys more of the shot-9
result.

## Generation reference

- Media ids: shot 9 still `f7086f9c-8864-43ba-a859-b8b9c5559777` · shot 11 still `bac4e697-0f90-42be-9fc5-2ef6b8d1ba14`
- Job ids: shot 9 `87c85dfc-5174-4126-be7b-1a945529cf26` · shot 11 `3e2ae5c8-d1b8-48c6-9ad4-455b1e43ae28`
- Frames: `contact-sheet/shot-09-motion-v2-seedance15.png`, `contact-sheet/shot-11-motion-v2-seedance15.png`

---

# Batch of five — shots 1, 2, 5, 6, 10 — 2026-08-25

All five on `seedance1_5`, 4s, 720p, silent, from approved stills, with the constancy clause added
to each movement prompt. **12 credits. Balance after: 472.8.**

## Correction to the credit figures used earlier today

The real charge is **2.4 credits per 4-second 720p clip on `seedance1_5`**, not the 4.8 the cost
preflight quotes. Confirmed twice against the actual balance: 489.6 → 484.8 for two clips, and
484.8 → 472.8 for five.

`seedance_2_0_mini` really does cost 7.6. So the model that was being avoided to save money is
**three times cheaper**, not 37% cheaper as first written. Every budget figure above this line that
was based on 4.8 is roughly double the truth. The preflight tool over-quotes; trust the balance.

## Results — 2 pass, 2 partial, 1 fail

| Shot | Verdict | Measurement | What happened |
|---|---|---|---|
| **10 · Craft** | ✅ **Pass** | motion/frame 4.8–8.3, no acceleration; blown pixels ~0 | Best in the batch. Slow controlled arc, hard light sweeping the machined grooves exactly as written, cyan rim staying a thin bright edge on the metal. Blacks deep and unlifted throughout |
| **2 · The disconnected room** | ✅ **Pass** | motion/frame 6.5–10.9; blacks hold | Slow forward dolly, symmetry held dead centre the whole way, monitors genuinely mismatched — white, amber, green, blue. The +43% mean brightness is the monitors arriving, not a grade drift; the ceiling stays black |
| **6 · The room syncs** | ⚠ Partial | cyan area 47 → 11,642 px, **20% of frame**; cyan brightness flat 95 → 139 | The line itself is right — thin, on the wall seam, constant brightness, and each monitor does wake as it passes. But the **glow floods the wall and floor**. The rulebook says cyan is always thin and never a mist. This is the same fault that failed the shot-6 still on its first attempt |
| **5 · Order from above** | ⚠ Partial | brightness 89.8 → 153.0 (**+70%**); motion/frame 31.7 | A handsome rising reveal of the aligned grid, and it does read as order. Two problems: the blacks lift badly, breaking "deep pure blacks with unlifted shadows", and the move is far too fast. Also the papers never actually slide into alignment — they start aligned and the camera reveals more of them |
| **1 · Scattered documents** | ❌ **Fail** | brightness 78.2 → 40.1 (**−49%**) | Fades halfway to black despite `no fade` in the prompt, and a large black vertical band wipes across the frame — an object passing in the foreground that is not in the still. Unusable |

## What this adds to the pattern

The photometric/choreographic split from earlier still holds, but it needs a third line:

- **Camera and light, with nothing else asked of the frame** — shots 10 and 2. Both passed first
  try. This is the reliable case.
- **Choreography** — shot 5's papers were told to slide into alignment and simply did not. Same
  class as shot 9's hand. **The model has now refused a staged action three times out of three.**
  Treat "something performs an action" as a thing this tool does not do, not a prompting problem.
- **Exposure drift is not fully solved.** `exposure and colour temperature stay constant` and
  `no fade` were both in every prompt in this batch. Shot 1 still faded 49% darker and shot 5 lifted
  70% brighter. The clause helps — it is why shots 2 and 10 held — but it is not reliable when the
  frame is mostly one tone. Both failures were near-monochrome shots: white paper on black.

## Standing on the film

| Status | Shots | |
|---|---|---|
| **Clip approved** | 2, 4, 8, 10 | 4 of 11 |
| Needs another attempt | 1, 5, 6, 11 | each has a specific, known fix |
| Needs a different approach | 3, 7, 9 | staged events — the tool will not do these |
| Built in the editor | 12 | title card |

## Fixes for the next attempt

- **Shot 1** — the fade and the foreground wipe. Add `the camera stays in open space with nothing
  passing in front of the lens` and `the brightness of the paper does not change at any point`.
- **Shot 5** — drop the alignment choreography entirely and ask only for the rise, slower:
  `camera rises straight up very slowly, travelling a short distance; the documents are already
  aligned and do not move; the black desk surface stays pure black and never lifts to grey`.
- **Shot 6** — keep everything, add `the cyan light does not spill or glow onto the wall or floor;
  only the line itself is lit; the wall stays dark grey`.
- **Shot 11** — framing only, as noted above.

At 2.4 credits a clip, all four retries cost **9.6**. There is no financial reason not to iterate.

## Generation reference

| Shot | Media id | Job id |
|---|---|---|
| 1 | `a1b8f66f-d323-4f07-a262-f012b8fdbadd` | `f322aa0d-fccb-45e9-a6bb-c01d859bfb19` |
| 2 | `0d63010e-6887-40cb-86f4-ea43c090a822` | `9de072f9-b88c-44fe-b117-4e1e05d27850` |
| 5 | `3457e5d6-54ba-4bdf-8f95-c0994ba09d71` | `c39d588c-5465-4dc0-8df6-b0244e0c4252` |
| 6 | `22ec1767-ced4-4d83-9884-dc360228e150` | `c8951827-366c-471a-a7a7-600d5bf6e92c` |
| 10 | `81358788-8cde-4a99-b230-d9d1e0e542a1` | `859d2d02-f2e8-4914-86fd-92cae94522ca` |

Two operational notes for whoever runs the next batch:

1. **The API may answer with a preset instead of a job.** Shots 1 and 2 came back with
   `submission_failed` and a recommendation for a stock preset called "IN THE DARK". Resubmit the
   same request with `declined_preset_id` set to the offered preset id. A canned preset would
   override the visual bible, so always decline.
2. **Three concurrent jobs is the ceiling.** A fourth returns `429 rate_limit_reached`. Submit in
   groups of three and wait for `all_terminal` before the next group.

---

# Four known-fix retries — shots 1, 5, 6, 11 — 2026-08-25

All four on `seedance1_5`, 4s, 720p, silent, from approved stills. Submitted in two groups to stay
under the three-job ceiling: shots 1, 5, 6 first; shot 11 after those completed. Expected cost:
**9.6 credits** at the observed 2.4 credits per clip.

## Results from measurement pass

These clips still need a human eye check in the gallery or local player. The measurements below
are from 24 sampled frames per clip, scaled to 320px wide, so they are useful for detecting exposure,
cyan spread and gross composition drift, not for judging taste.

| Shot | Verdict | Measurement | What happened |
|---|---|---|---|
| **1 · Scattered documents** | ✅ **Candidate pass** | brightness 81.3 → 77.0, no cyan, motion/frame 10.54 | The hard failure appears fixed. No 49% fade and no obvious foreground wipe in the sampled metrics. Needs visual check, but this is probably usable |
| **5 · Order from above** | ⚠ **Improved partial** | brightness 91.5 → 121.9 (**+33%**), motion/frame 15.35 | Much better than v1's +70% lift and too-fast movement, but it still brightens across the clip. Possible grade/edit candidate, not a clean lock |
| **6 · The room syncs** | ❌ **Still fails** | cyan area 2 → 15,575 px at 320x180, about **27% of frame** | The no-spill wording did not solve the core problem. The cyan still expands into a wash, which breaks the rulebook. Do not keep iterating this exact ask |
| **11 · Dawn** | ✅ **Candidate pass** | brightness 55.7 → 59.5, blown px 294 → 575, dark-centroid x 0.392 → 0.424 | Exposure is stable and the framing drift is much smaller numerically than before. Needs visual check, but this is probably usable |

## New standing

| Status | Shots | |
|---|---|---|
| **Clip approved** | 2, 4, 8, 10 | 4 of 11 |
| **Candidate after retry** | 1, 11 | likely usable after eye check |
| Needs edit/visual decision | 5 | improved, but still lifts brightness |
| Needs different approach | 3, 6, 7, 9 | staged events or cyan-spill failure |
| Built in the editor | 12 | title card |

## What changed in the lesson

Shot 1 shows that the constancy clause can fix exposure drift when the prompt also blocks foreground
movement. Shot 11 suggests the framing problem can be reduced enough to use. Shot 6 is the important
negative result: once the tool wants to turn the cyan line into atmosphere, a stronger prohibition
does not stop it. Solve shot 6 by changing the shot, holding the still, or cutting around the line
movement rather than asking for the same travelling-line event again.

## Files

- `generated/shot-01-clip-v2-seedance15.mp4`
- `generated/shot-05-clip-v2-seedance15.mp4`
- `generated/shot-06-clip-v2-seedance15.mp4`
- `generated/shot-11-clip-v3-seedance15.mp4`

## Generation reference

| Shot | Media id | Job id |
|---|---|---|
| 1 | `a1b8f66f-d323-4f07-a262-f012b8fdbadd` | `2a645d0b-d475-4f3d-80dc-81879b263ca2` |
| 5 | `3457e5d6-54ba-4bdf-8f95-c0994ba09d71` | `d6e512a9-10e3-4650-8cc9-08d5c1573f6d` |
| 6 | `22ec1767-ced4-4d83-9884-dc360228e150` | `60ea5547-fb6c-40c7-a88d-b1924a3bf6db` |
| 11 | `bac4e697-0f90-42be-9fc5-2ef6b8d1ba14` | `da960044-dba9-4869-baa2-34e314c502f0` |

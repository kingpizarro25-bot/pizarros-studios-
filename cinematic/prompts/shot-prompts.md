# Paste-ready generation prompts
### From Chaos to Intelligence · 12 shots

Everything in the grey code blocks is written for the machine, not for you. Copy a block, paste
it in, generate. You do not need to understand the wording — the plain-English version of every
shot lives in `cinematic/storyboards/from-chaos-to-intelligence.md`.

---

## How to actually run this (read once)

**Make a still picture first, then turn it into video.** This is the single most important
production habit, for two reasons:

1. **Control.** A still costs 2 credits. A video costs 18 to 36. Getting the look right on
   still pictures first means you never burn video money on a shot that was wrong anyway.
2. **Consistency.** Once you approve a still frame, you feed that exact picture into the video
   step as its opening frame. The video then inherits the approved look instead of reinventing
   it. This is what stops twelve shots from looking like twelve different films.

So the order is always:

```
1. Generate still frame  →  2. You approve it  →  3. Feed it in as the first frame of the video
```

**Generate longer than you need.** The video tools have a four-second minimum, and several of
our shots are shorter than that. Always generate 4–5 seconds and trim it down in the edit. It
also gives you room to pick the best-moving portion of the clip.

**Which tools to use:**

| Step | Tool | Why |
|---|---|---|
| Still frames | `nano_banana_pro` at 2k, 16:9 | Sharpest, best at real materials and readable screens |
| Shot 7 specifically | `nano_banana_pro` | It is the only one that renders small interface text believably |
| Video from a still | `seedance_2_0`, with the approved still as `start_image` | Holds onto the reference picture properly |
| Cheap test passes | `seedance_2_0_mini` at 720p | Half the cost, good enough to judge movement |
| Shot 12 | No AI at all | Build the title in the editor so the lettering is perfect |

---

## The standard ending

**Add this to the end of every still-frame prompt.** It is the visual rulebook translated into
the wording the generators respond to.

```
cinematic, photographic, shot on ARRI Alexa, anamorphic lens, deep pure blacks with unlifted
shadows, single motivated light source, high dynamic range, restrained colour, brushed aluminium
and graphite and dark glass materials, generous negative space, precise composition, subtle
35mm film grain, no colour cast
```

## The standard banned list

**Add this to the "avoid" or "negative" field on every single generation, in addition to the
per-shot avoid list.**

```
glowing AI brain, humanoid robot, floating hologram, blue neon, falling code, cyberpunk city,
lens flare, futuristic HUD, glowing grid, circuit board, stock office photo, smiling people at
laptops, purple blue gradient, 3D render look, plastic sheen, warped text, distorted hands,
extra fingers, watermark, oversaturated, blurry, smeared motion, low contrast, lifted blacks
```

---

## Still-frame prompts, in order

Aspect ratio `16:9` and resolution `2k` for all of them.

### 1 · Scattered documents
```
Extreme close-up macro shot, 100mm lens, scattered white paper documents overlapping at irregular
angles on a dark graphite desk surface, shallow depth of field with only two pages in focus,
single hard directional light from low left, deep pure black shadows on the right side of frame,
no fill light, cold neutral grey colour, fine paper fibre texture visible, one bent corner,
pre-dawn office interior
```
*Also avoid:* any cyan, screens, people, hands, readable text, warm light.

### 2 · The disconnected room
```
Wide establishing shot, 24mm lens, empty modern open-plan office interior before dawn, seven
computer monitors glowing at different brightnesses and slightly mismatched colour temperatures,
isolated pools of light that do not connect, completely dark ceiling, large windows with faint
cold blue-grey pre-dawn light outside, clean architectural lines, deep blacks, no people
```
*Also avoid:* cyan, city skyline, warm office lighting, ceiling lights on, people.

### 3 · Notifications in glass
```
Close-up, 85mm lens, a smartphone lying face up on a dark desk seen as a reflection in a pane of
dark tinted glass in the foreground, notification banners stacking on the screen, a human hand
resting still on the desk beside it not reaching, phone screen is the only key light and is cold
and hard, one soft dull amber desk lamp far out of focus in the background, deep black
surroundings, shallow depth of field
```
*Also avoid:* readable text, a face, cyan, bright room light, distorted hand.

### 4 · The line is born
```
Extreme close-up macro, 100mm lens, a single thin bright cyan line of light drawing itself along
the machined edge of a dark graphite desk, the line hugs the physical surface exactly and does not
float, one white paper document edge catching the cyan light as the line passes it, deep black
background, hard side light from low left, shallow depth of field
```
*Also avoid:* floating light, particles, sparks, multiple lines, glow flooding the frame.

### 5 · Order from above
```
Overhead top-down shot, 50mm lens, camera directly above a dark graphite desk, white paper
documents in a precise aligned grid formation, a single thin cyan light line running along the
desk seam at the bottom of frame, even cool side lighting, deep blacks, clean composition with
generous negative space
```
*Also avoid:* hands, people, floating paper, glowing paper, readable text.

### 6 · The room syncs
```
Tracking shot composition, 35mm lens, a row of desks in a dark modern office seen from the side
with strong foreground and background separation, a thin cyan light line travelling along the wall
seam behind the desks, computer monitors showing one consistent cool tone, dark ceiling, no people,
deep blacks
```
*Also avoid:* floating line, neon spread, readable code, people, overhead lighting.

### 7 · Verification
```
Close-up, 50mm lens, a computer monitor shot at an oblique angle through a dark glass partition,
faint reflection of the room visible on the glass, on the screen a restrained dark user interface
with small monospaced labels checking a document line by line, thin cyan accent details, one small
green confirmation indicator, most on-screen text too small to read and slightly out of focus,
deep blacks
```
*Also avoid:* fake sci-fi interface, circular scanner, rotating globe, code rain, large readable
text, bright white interface, screen flat-on to camera.

### 8 · One system
```
High wide shot, 24mm lens, looking down across a dark modern office from above, thin cyan light
lines running along wall seams ceiling joins and floor edges connecting the workstations, subtle
and architectural like integrated lighting design, one small warm amber lamp glowing in the far
distance, first faint dawn light at the large windows, deep blacks, no people visible
```
*Also avoid:* network diagram, glowing nodes, holographic map, dotted connection lines, floating
data.

### 9 · The decision
```
Extreme close-up, 85mm lens, a single human hand at a desk lit from the left by a warm amber
practical lamp and from the right by a cool cyan screen glow, both light sources balanced and
equally strong, one finger making a single deliberate press, no face visible, dark background,
anatomically correct hand with five fingers, shallow depth of field
```
*Also avoid:* distorted hands, extra fingers, a face, glowing keyboard, dramatic gesture.

### 10 · Craft
```
Macro product shot, 100mm lens, a solid brushed aluminium block with extremely fine
precision-machined parallel grooves across its face, one narrow hard light raking across the metal
grain, thin cyan rim light on a single edge, pure black background, no other objects, real
manufactured object with believable tooling marks
```
*Also avoid:* glowing object, floating object, chrome, plastic render, sci-fi prop, logo, text,
particles.

### 11 · Dawn
```
Wide shot, 24mm lens, a modern open-plan office at dawn, warm golden daylight entering through
large windows, desks tidy and ordered, monitors showing consistent calm content, thin cyan light
lines dimmed and at rest along the architecture, one person standing small in silhouette at a far
window looking out, deep focus with everything sharp front to back, soft wide natural lighting
```
*Also avoid:* shallow focus, lens flare, sun stars, visible face, busy activity, neon.

### 12 · Title card
Not generated. Built in the editor. Specification is in the storyboard.

---

## Turning the stills into video

Once a still is approved, generate the video with the approved still as its opening frame. Keep
the video prompt **short** — it describes only the movement, because the picture already carries
the look.

| Shot | Video prompt — movement only |
|---|---|
| 1 | `camera slowly dollying right, documents completely still, subtle dust in the air` |
| 2 | `camera very slowly dollying forward down the room, monitors flickering slightly out of sync` |
| 3 | `static camera, notification banners appearing one after another on the phone screen, hand completely still, focus shifting from the glass reflection to the hand` |
| 4 | `camera sliding slowly left, the cyan line extending steadily along the desk edge at constant speed, paper edge straightening as the line passes` |
| 5 | `camera rising slowly straight up, paper documents sliding and rotating into aligned grid formation, settling smoothly without bouncing` |
| 6 | `camera tracking sideways past the desks with strong parallax, cyan line travelling along the wall seam, each monitor shifting to matching colour as the line passes it` |
| 7 | `static camera, rows of small check indicators resolving down the document on screen, one green confirmation appearing at the end` |
| 8 | `camera craning slowly upward, cyan architectural lines glowing steadily, dawn light very slowly increasing at the windows` |
| 9 | `static camera, one finger pressing down once slowly and deliberately, then stillness` |
| 10 | `camera arcing slowly around the aluminium block, hard light sweeping across the machined grooves` |
| 11 | `camera gliding forward almost imperceptibly, dawn light slowly warming, the distant figure completely still` |

**Video settings:** `seedance1_5`, aspect ratio `16:9`, duration 4 seconds, resolution `720p` for
tests and `1080p` for the final version, audio off (`generate_audio: false` — the sound is designed
separately and generated audio will fight it). The still is passed with role `start_image`.

> **Changed 2026-08-25.** This used to say `seedance_2_0`. That model is **not available on this
> account** — it rejects the job with "Requires plus plan or higher", and a cost preflight will
> still quote you a price without warning you. `seedance1_5` is available, costs 4.8 credits for a
> 4-second 720p clip against `seedance_2_0_mini`'s 7.6, and produced better motion in a direct
> test. See `../shot-lists/production-tracker.md`.

**Add to every motion prompt**, whatever the shot: say what must *not* change, not only what
should move. `holds one constant brightness and never dims or brightens`, `exposure and colour
temperature stay constant`, `nothing else moves`. The generator's default instinct is to make
glowing things pulse and to drift the grade; it will not stop unless told.

---

## What this costs, in real numbers

These are live prices checked against the account, not estimates:

| Item | Cost |
|---|---|
| One still frame, `nano_banana_pro` at 2k | **2 credits** |
| One 4-second video, `seedance_2_0_mini` at 720p | **10 credits** |
| One 4-second video, `seedance_2_0` at 720p | **18 credits** |
| One 4-second video, `seedance_2_0` at 1080p | **36 credits** |

**Three ways to make this film:**

| Approach | What you get | Credits |
|---|---|---|
| **Stills only** | 11 approved frames. A complete look-book you can show clients, and the whole style locked. No motion. | **22** |
| **Cheap full film** | 11 stills, then all 11 as 720p video | **132** |
| **Final quality** | 11 stills, then all 11 as 1080p video | **418** |

Add roughly 40% on top of any of these for regenerating shots that miss. Nobody gets 11 for 11.

**The honest recommendation:** spend the 22 credits on stills first. Judge the whole film as a
set of still frames. Only pay for motion on frames you would already be proud to put on the
website.

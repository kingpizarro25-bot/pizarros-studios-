# Pizarro Studios — cinematic production system

This folder is a repeatable way to make videos for Pizarro Studios, not a one-off project. The
first film built it; every film after this one reuses it.

## Start here

| If you want to... | Read |
|---|---|
| Understand the look and its rules | `brand-system/VISUAL-BIBLE.md` |
| See the first film shot by shot | `storyboards/from-chaos-to-intelligence.md` |
| Actually generate something | `prompts/shot-prompts.md` |
| Track what is finished | `shot-lists/production-tracker.md` |
| Put video on the website | `web-assets/WEB-INTEGRATION.md` |
| Learn the craft as you go | `LEARNING-GUIDE.md` |
| Know what state this is in | `PRODUCTION-STATUS.md` |

## What is in each folder

```
cinematic/
├── brand-system/     The rulebook. Read before writing any prompt.
├── storyboards/      Shot-by-shot plans, in plain language.
├── shot-lists/       Progress tracking.
├── prompts/          Paste-ready prompts + shots.json for automated runs.
├── references/       The reusable asset library plan.
├── generated/        Everything the generator produces. Keep the rejects.
├── approved/         Only frames good enough for the website.
├── audio/            Sound design direction.
├── web-assets/       Compressed video for the site, plus the code to embed it.
└── social-assets/    Short vertical versions.
```

## The first film

**From Chaos to Intelligence** — 40 seconds, 12 shots, four acts, no voiceover.

A business is full of information that does not talk to itself. Something starts connecting it.
By the end, the same complexity is still there, but it is under control. The audience should come
away understanding that Pizarro Studios does not build websites — it builds intelligent systems.

## How to make a film with this system

1. Read the rulebook, sections 2 to 5.
2. Write a shot-by-shot plan in the same format as the existing storyboard.
3. Generate **still frames** for every shot first. They are cheap. Approve them as a set.
4. Only then turn approved stills into video, using each still as the video's opening frame.
5. Edit, add sound built from the sound library, and grade.
6. Compress for the web using the commands in `web-assets/`.
7. Add anything reusable to the asset library.

## Rules that are not negotiable

- One accent colour leads per shot. Cyan is the system, amber is the human.
- Blacks stay black. Do not brighten shadows.
- Every light source can be pointed at.
- The cyan line always touches a real surface. It never floats.
- Nothing from the banned list, ever — if a frame hits it, regenerate rather than repair.
- The website works with every video switched off.

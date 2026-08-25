# Putting the film on the website

The site's job is to get someone to contact you. The film's job is to make them believe you are
serious before they read a word. If the video ever gets in the way of the first job, the video
loses.

## The rule

**The site must work perfectly with the video switched off.** Every video is decoration layered
on top of a page that already functions. Someone on a slow phone connection should get the still
picture and the same message.

## Where video belongs, in priority order

**1. Behind the hero — do this one first.**
The top of the page currently has the heading over a plain dark background. A very quiet loop
behind it, heavily darkened, adds enormous credibility for almost no risk. Use Shot 8 or Shot 11
— slow, wide, calm. Never a shot with fast movement; the text has to stay readable.

**2. Inside the project cards.**
Veridoc, MTI-JATT, and CCS each get a short silent loop that plays only when someone hovers or
scrolls it into view. This is where video earns its keep — it turns "we built a thing" into
"look at the thing".

**3. A "Watch" section, low on the page.**
The full 40-second film with sound, click to play, never automatic. Put it below the work, not
above it. Someone who scrolls that far is already interested.

**4. Between sections.**
A two-second near-black clip as a divider. Subtle. Optional. Do this last, if at all.

**Do not** put video behind the contact section, behind body text, or anywhere it competes with
something someone is trying to read.

## Preparing the files

Every video needs four versions. The commands below use `ffmpeg`, which is free.

**Desktop background loop** — 1920 wide, silent, no audio track at all:
```bash
ffmpeg -i source.mp4 -an -vf "scale=1920:-2" -c:v libx264 -crf 26 -preset slow \
  -pix_fmt yuv420p -movflags +faststart hero-desktop.mp4
```

**A smaller, more modern version** for browsers that support it — usually 30% smaller again:
```bash
ffmpeg -i source.mp4 -an -vf "scale=1920:-2" -c:v libvpx-vp9 -crf 34 -b:v 0 hero-desktop.webm
```

**Mobile version** — smaller frame, lower quality, because it is behind text anyway:
```bash
ffmpeg -i source.mp4 -an -vf "scale=1280:-2" -c:v libx264 -crf 30 -preset slow \
  -pix_fmt yuv420p -movflags +faststart hero-mobile.mp4
```

**The still fallback** — grab a frame from two seconds in:
```bash
ffmpeg -i source.mp4 -ss 00:00:02 -frames:v 1 -q:v 2 hero-poster.jpg
```

### Size limits — treat these as hard rules

| File | Maximum |
|---|---|
| Hero loop, desktop | **2.5 MB** |
| Hero loop, mobile | **1.2 MB** |
| Project card loop | **800 KB** |
| Still fallback picture | **150 KB** |
| The full film, on its own page | 20 MB, or host it elsewhere |

If a hero loop is over 2.5 MB, cut its length before you cut its quality. A three-second loop
that is sharp beats an eight-second loop that is mushy.

## The code

Drop this into the hero section of `index.html`, immediately inside `<section class="hero">`:

```html
<div class="hero-media" aria-hidden="true">
  <video autoplay muted loop playsinline preload="none"
         poster="cinematic/web-assets/hero-poster.jpg">
    <source src="cinematic/web-assets/hero-desktop.webm" type="video/webm">
    <source src="cinematic/web-assets/hero-desktop.mp4" type="video/mp4">
  </video>
</div>
```

And this into the stylesheet:

```css
.hero{position:relative;overflow:hidden}
.hero .shell{position:relative;z-index:2}
.hero-media{
  position:absolute;inset:0;z-index:1;
  pointer-events:none;
}
.hero-media video{
  width:100%;height:100%;object-fit:cover;
  opacity:.38;
  filter:saturate(.75);
}
/* Keeps the heading readable no matter what the video is doing */
.hero-media::after{
  content:"";position:absolute;inset:0;
  background:linear-gradient(180deg,rgba(5,7,10,.55),rgba(5,7,10,.92));
}
@media (max-width:760px){
  .hero-media video{opacity:.28}
}
/* Anyone who has asked their device to reduce motion gets the still picture */
@media (prefers-reduced-motion:reduce){
  .hero-media video{display:none}
  .hero-media{
    background:url("hero-poster.jpg") center/cover no-repeat;
  }
}
```

Four things that code is doing, and why each matters:

- `muted` and `playsinline` — without both, phones refuse to autoplay at all.
- `preload="none"` with a `poster` — the page loads fast and shows the still picture; the video
  only downloads once it is needed.
- The dark gradient over the top — this is what guarantees the heading stays readable regardless
  of what the video does. Do not remove it.
- The reduced-motion block — some people have set their device to cut down on animation, often
  because motion makes them ill. This respects that automatically, and it costs you nothing.

## Before it goes live

- [ ] Turn off JavaScript and reload. Does the page still make sense?
- [ ] Throttle to a slow connection in the browser tools. Does the heading appear immediately?
- [ ] Look at it on an actual phone, not a resized browser window.
- [ ] Turn on "reduce motion" in your system settings and reload. You should get a still picture.
- [ ] Check the heading is readable over the brightest frame of the loop.
- [ ] Confirm no video file autoplays with sound. Ever.

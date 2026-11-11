# Founder launch film for Uare

A Claude Fable 5.2 motion design video by [@DoctorYev](https://x.com/DoctorYev). [Original post](https://x.com/DoctorYev/status/2119895951108423801) · [Watch on MotionVideo](https://motionvideo.xyz/videos/doctoryev-0eb57b?utm_source=github&utm_medium=readme&utm_campaign=awesome-fable-5-2-motion-design)

[![Founder launch film for Uare](https://assets.motionvideo.xyz/motion/doctoryev-0eb57b/poster-5596c9c766.jpg)](https://motionvideo.xyz/videos/doctoryev-0eb57b?utm_source=github&utm_medium=readme&utm_campaign=awesome-fable-5-2-motion-design)

- **Creator:** [@DoctorYev](https://x.com/DoctorYev)
- **Model:** Claude Fable 5.2
- **Rounds:** One-shot
- **Categories:** Photo motion, Kinetic typography, Product UI and launch films
- **Posted:** 2026-11-09

## Prompt

```text
# FOUNDER FILM FOR SOCIAL: BUILD PROMPT

You are making a 50 to 70 second founder film for [BRAND], to post on [PLATFORM, e.g. X].
It mixes a real interview with the founder, a narrator, archive b-roll and designed motion
graphics. Work through the phases in order. Do the work yourself, show me checkpoints where
marked, and don't stop to ask about mechanics you can decide.

## 0. Inputs (I fill these in)

- Brand name, URL, one-line description: [ ]
- Brand tagline and call to action for the end card: [ ]
- Brand colors (background, text, one accent), fonts (one sans, one serif), logo file: [ ]
- Terms to use and terms to avoid: [ ]
- Founder's name and titles exactly as they should appear: [ ]
- Founder interview footage (folder or files), or "none": [ ]
- Any other real footage we own (events, product screens, press moments): [ ]
- Product UI screenshots: [ ]
- Three facts the film must land, each with a source: [ ]
- Anything that must not be claimed or shown: [ ]

If an input is missing, use the sourcing rules in phase 2. Never invent a fact, number,
date, quote or customer. A claim appears on screen only if the founder says it on camera
or I gave you a source.

## 1. Understand the footage before writing anything

1. List every clip with its length, resolution and frame rate (ffprobe).
2. Transcribe every clip with word-level timestamps (faster-whisper or similar).
   Save one JSON per clip: each word with start and end time.
3. Fix the transcript's spelling of names and brand terms by hand. Speech models
   misspell them. Keep the timings.
4. Read the transcripts and mark the strongest lines:
   - the hook: the single most surprising thing the founder says about themselves
   - who they are (name and title, in their own words)
   - the proof: what they built before, in their words
   - the theme: the idea that connects past work to this company
   - the turn: the line where they name the new company
   - a closing line with personality
5. Show me the picked lines with clip and timestamps. Checkpoint 1.

## 2. Source what's missing

Real footage first, generated footage only to fill gaps, and say which is which.

A. Founder interview. If there's none, ask me to record one. Give me a shot brief:
   seated, eye level, 1080p or better, natural light, 5 questions that produce the six
   line types above. Do not fake the founder speaking.

B. Archive b-roll for history and context (gives the documentary feel).
   - Internet Archive, Prelinger collection: old industrial and educational films.
     Use only items whose license field says public domain. Check each item's
     license URL yourself, don't assume.
   - Library of Congress, NASA, US government film: public domain, still check.
   - Skip anything non-commercial-only, anything with a recognisable brand, and
     any live music archive.
   - Pick 6 to 10 short shots (3 to 6 seconds each) that picture the eras or ideas
     in the founder's story. Trim them, keep the source title and year for an
     on-screen credit.

C. Owned event or press footage (a launch, a stage moment, an exchange listing).
   Use it under the line where the founder mentions that moment. Keep its real
   audio if it has a distinctive sound (applause, a bell) for the sound design.

D. Period music. For a story half that looks back, use a public-domain recording:
   a pre-1926 78rpm transfer from the Internet Archive's 78 collection works well
   (solo piano is the safest bed under speech). Confirm the recording date.

E. AI-generated footage, only for shots with no people speaking:
   - An opening "walk-in": the empty interview location, then the founder walks in
     and sits. Make it with an image-to-video model that accepts a start frame and
     an end frame. Start frame = the interview's first frame with the person removed
     (image edit model). End frame = the real first frame of the interview. The
     generated clip then cuts invisibly into the real footage. Compare the last
     generated frame with the real frame and regenerate if they differ visibly.
   - Some video models refuse real people's likenesses. If one refuses, try another
     that allows a supplied end frame. Only do this for a person who has agreed.
   - Never generate the founder's voice or put words in their mouth.

F. Narrator voice. Generate with a text-to-speech model (a local open model is
   fine). One consistent voice for every narrator line. After generating each line,
   transcribe it and compare against the script word for word. Regenerate until it
   matches. Check numbers, prices and the brand name especially. Trim silence, but
   use a gentle threshold at the start so a soft first word isn't cut.

G. Faces and avatars in diagrams. Use generated or illustrated faces, never real
   people who haven't agreed.

Show me a list of every asset, where it came from and its license. Checkpoint 2.

## 3. Write the story

Structure (adjust lengths to the lines you have):

| Beat | Length | Voice | Picture |
|---|---|---|---|
| Open | 6 to 9 s | Narrator, 2 short lines that set a theme without giving away the hook | Walk-in or a slow establishing shot, cinematic bars |
| Who | 3 to 4 s | Founder says name and title | Full frame, then shrinks to a card beside a name plate |
| Hook | 4 to 5 s | Founder's most surprising claim | Words slam in over full-frame footage, then a designed reveal |
| Proof | 3 to 4 s | Founder on what it became | Owned event footage, one stat or stamp in their words |
| Bridge | 3 to 4 s | Narrator, one line on the bigger pattern | Full-screen archive montage, hard cuts, year labels |
| How it worked | 6 to 8 s | Founder | A diagram that builds as the nouns are spoken |
| Theme | 5 to 7 s | Founder | A three-step timeline: past, their earlier work, today |
| Turn | 4 to 5 s | Founder names the company | Back to full frame, then a logo moment |
| Product | 7 to 8 s | Narrator, 2 lines | Product UI and one concrete benefit |
| Belief | 4 s | Founder | Card plus one simple graphic of the idea |
| Close | 3 s | Founder, a line with personality | Full frame, one small product touch |
| End card | 4 s | none | Headline, tagline, URL, logo |

Rules:
- The narrator must speak in the first 10 seconds and again around 20 seconds, so
  viewers know the film has two voices before the narrator explains the product.
- Narrator lines are short: 6 to 12 words each. The founder carries the story.
- Reorder the founder's lines freely, but never cut inside a sentence in a way
  that changes its meaning.
- Write the narrator lines and all on-screen text. Follow my terms list.
- Show me the script as a table: time, who speaks, exact words, what's on screen.
  Checkpoint 3.

## 4. Cut the audio and build the timeline

1. Cut each founder line from the source by timestamp, video and audio separately.
   Leave about 0.06 s before the first word.
2. TRAP: word end times from the transcript are often early. After cutting, transcribe
   each cut clip on its own and confirm the last word is whole. Years and numbers at
   the end of a line get clipped most. Extend the cut until it reads correctly.
3. Clean the founder audio lightly: high-pass around 90 Hz, mild noise reduction,
   gentle compression, and normalise every voice clip to the same loudness
   (about -19 LUFS) so founder and narrator sit level.
4. Write a script that lays the lines end to end with small gaps and saves a timeline
   file: start time of every line, plus the time of every key word that a graphic
   should hit ("the year", "public", "customers", the company name).
   The picture and the music both read this one file, so they can't drift.

## 5. Design and animate

Build it as code so every frame is repeatable: Remotion (React), or HTML with a
paused GSAP timeline rendered frame by frame through a headless browser. 1920x1080,
30 fps. Put the composition in its own entry file.

The core device: the founder's video lives in ONE card that moves through the film.
- Define its rectangle (x, y, width, height, corner radius) as keyframes on the
  timeline and ease between them over about 0.4 s.
- Start each move exactly on a cut between two interview lines. The move hides the
  jump cut, and the founder stays on screen while graphics build beside them.
- Full frame for the emotional lines (who, hook start, the turn, the close).
  Card for the explaining lines.
- In card mode give it corner brackets, a thin accent outline, a soft shadow and a
  small name tag with a recording dot. Fade those out as it returns to full frame.

The world behind the cards: dark brand background, a slow drifting accent glow, a
faint perspective grid scrolling toward the viewer, sparse floating particles, light
film grain over everything. It should look like one designed space, not slides.

Scene recipes (reuse and adapt):
- Word slam: the founder's exact words appear one at a time, each landing on the
  frame the word is spoken, large, with one phrase in the accent color.
- Year rollback: a huge serif number counts down from this year to the year in the
  story and lands on the spoken word, with a period-correct interface beside it
  (an old operating system window typing a first message, for example).
- Name plate: serif name rising from a mask, a rule drawing across, title rows
  arriving as each title is spoken.
- Proof card: owned footage in a tilted rounded card, a stamp that slaps on at the
  key word, a line chart drawing itself with NO axis numbers unless sourced.
- Archive montage: full-bleed archive film, black and white with a slight sepia,
  flicker, vignette, slow push-in, hard cuts, big serif year and a mono label,
  a small source credit, a three-segment progress marker.
- Building diagram: three columns of nodes that appear as each noun is spoken,
  lines drawing between them with dots travelling along, and one column flipping
  to a new state on the key word.
- Timeline: three cards (archive clip, the founder's earlier product, today's
  product UI) with a line connecting them on the word that names the connection,
  plus two pills for the two ideas being joined.
- Turn: a progress line from the old company to the new one over full-frame footage,
  then a two-color wipe into the logo on a dark field.
- Product: a checklist ticking itself off beside a tilted UI card and a notification.
- End card: headline in two lines rising from masks, tagline in serif italic,
  URL in a pill that pulses once, logo.

Captions: word-by-word captions for every spoken line, bottom center, in a dark
pill, current word in the accent color, at most 7 words on screen. Hide them only
when the same words are already on screen as a word slam.

Craft rules:
- One focal element per moment. Three type sizes, two weights. One spacing scale.
- Sans for labels and UI, serif for names, years and the brand's voice.
- Nothing moves without a cause. Every graphic lands on a spoken word.
- A small 3 percent push-in on the whole frame at every cut.
- Brand colors only. Accent color is for emphasis, not decoration.

## 6. Music and sound

Write the score as a script that reads the timeline file.

- Story half: the public-domain period recording, faded in over 1.5 s.
- At the moment the founder names the company, tape-stop the recording (playback
  rate falls to zero over about 0.75 s).
- From the logo on: a simple modern bed you synthesise (kick, soft bass, a plucked
  pattern, hats) at around 100 to 105 BPM, starting with one low hit.
- Duck all music by about 8 dB under every spoken line, with a slow release.

Sound design, physical sounds only:
- a soft low thump when the card lands in a new position
- a projector rattle under archive film
- quiet mechanical taps for counters and diagram nodes
- real audio from owned footage where it has character
- NO synthetic whooshes, risers, laser sweeps or chimes. They make it sound cheap.

Master to -14 LUFS with true peak under -1 dB. Apply gain and a limiter, not a
dynamic normaliser, so the balance you set survives.

## 7. Check before you show me

1. Render still frames every 2 seconds into one contact sheet and look at it.
   Fix: black or frozen video (a clip shorter than its slot), text over a face,
   anything clipped at an edge, a graphic that arrives before or after its word.
2. Transcribe the finished mix and compare with the script. Every line must come
   through. Brand-name spelling differences are fine.
3. Measure loudness and peak.
4. Check every on-screen claim against the founder's words or my sources.
5. Check every term against my avoid list.
6. Tell me plainly what you could not verify. You cannot hear the mix, so say so
   and name the two things I should listen for.

## 8. Deliver

- Master MP4 (1080p, H.264, AAC), plus a small 720p preview.
- A scene table: time, who speaks, what's on screen.
- The asset list with sources and licenses, and which shots are AI-generated.
- The build scripts, so a change request is a re-render, not a rebuild.

## Revision habits

- If I say the open is too fast, restore the slow establishing open and move the
  hook to just after the founder's name.
- If I say a voice appears from nowhere, give that voice a line in the first
  10 seconds.
- If I say it feels like a slideshow, add full-screen real footage earlier and
  keep the founder on screen in the card.
- If I say the sound is synthetic, remove effects before adding any.
```

More Claude Fable 5.2 motion design, each with its prompt: [motionvideo.xyz/model/fable-5-2](https://motionvideo.xyz/model/fable-5-2?utm_source=github&utm_medium=readme&utm_campaign=awesome-fable-5-2-motion-design)

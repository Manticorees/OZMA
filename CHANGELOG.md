# Changelog

All public OZMA releases are listed here, newest first.
Each release is on the [OZMA page on itch.io](https://orumet.itch.io/ozma) and on the [Releases](https://github.com/Manticorees/OZMA/releases)
page here, as `OZMA-<version>.zip` with its `.sha256`
(from 0.9 also `OZMA-<version>-knulli-experimental.zip` for Knulli).

## 0.9 (2026-11-12): any sound becomes an instrument, what you hear becomes a loop

- **MORPH, a new instrument.** Put in any sound (a file, your voice from the mic, your computer over USB, a loop)
  and play it on the keys. WEIRD turns it into a ringing object (MATERIAL, BODY, ROLL for a new object on every
  press); PLAY AS HIT, TUNE, HOLD or **LOOP**. A second layer B can follow A's level, talk with its rhythm, take turns,
  jump in or scratch along. TO SAMPLER prints a MORPH as a SAMPLER instrument.
- **MORPH LOOP.** A loop fitted to 1, 2 or 4 bars of your tempo where every key plays a piece of it. It follows the
  tempo the song plays at (TEMPO, TPO steps, MIDI clock in). On the Brick a new loop takes a second or two to get ready
  after a song opens.
- **MAKE LOOP.** On LIVE, X on a playing clip: everything you hear, including what you played by hand, becomes one
  loop in a new row on the next bar. The music never stops; B, L2 or B+A takes it back.
- **LOAD LOOP and smarter WARP.** X on an empty LIVE cell > LOAD LOOP: a library loop lands following your tempo. Drum
  loops are cut at their hits, the rest is stretched; x2 / ÷2 on BPM and BARS.
- **EFFECTS is a route map** with two groups (six one-knob effects: SQUEEZE, DRIVE, CRUSH, SMACK, GROWL, DUST), new
  DELAY ECHO, REVERB ROOM / HALL / PLATE / GATED, MOD FX ENSEMBLE / WIDE / VIBE, and a MASTER card.
- **DUCK MATTER:** sidechain pumping in one press, eight styles, a live picture of the dip.
- **Record from your computer.** With USB AUDIO = IN, Y on the REC card switches MIC / USB IN (up to 30 s, the mic
  10 s), saved as `Recordings/USB_nnn.wav`.
- **CLIP:** hold A + arrows for pitch, add R1 for length (LEFT / RIGHT) and loudness (UP / DOWN). The grid shows your
  notes. R1 + B picks a step, a row or the clip; FILL and DOUBLE in a few moves.
- **SAMPLER v4:** a new screen with a wave box and four tabs, no scrolling; the REGION screen is shared with MORPH.
- **LUNA DEEP SKY:** four new dials on the LUNA piano (CORE, EMBER, TIDE, AURORA).
- **BALANCE LEARN:** the mix balancer listens to your song once and keeps what it learned.
- **PERFORM:** hold L2 for DUCK pads; L2 + LEFT = CHAOS, A keeps a run you like.
- **A new hangar** (the engine picker), and **25 lessons plus 7 DEEPER** inside the app (MENU).
- **Fixes:** sound comes back after the Brick sleeps and wakes; saves are remembered at once (no duplicate after a
  power cut); ECHO past 100 % no longer grows into a drone; SAMPLER slices play right on any SCALE; a damaged WAV
  header no longer crashes OZMA at start; many screen and wording fixes.
- **Updates keep your changes:** from 0.9 on, an update never replaces a demo song or OZMA KIT sample you changed.
- **Songs:** 0.9 opens your 0.8.2 songs. A song that uses MORPH opens only in 0.9 and later (0.8.2 says LOAD:
  UNSUPPORTED INSTRUMENT and leaves it closed, nothing is deleted).
- **Knulli (experimental):** a separate download, `OZMA-0.9-knulli-experimental.zip`, installed by hand.
  Install new Knulli builds by hand (not with PROJECT > UPDATE).

`OZMA-0.9.zip` sha256: `bd1145a32636b75ffc86e40056349971a2e6963fa5dbc2de3f73144272559abb`
`OZMA-0.9-usb-gpl-source.zip` sha256: `38e2a306d29d07a88c0372f40e167c0b341ac8665e9e394a2a1fa0a7e1d00cf2`
`OZMA-0.9-knulli-experimental.zip` sha256: `380eccf50269b40a04cdb006849ebc36bf2a887d72efdef3753060f7b3b0e1fc`

## 0.8.2 (2026-11-09): plug in your other gear, update over Wi-Fi, learn OZMA inside OZMA

- **Update over Wi-Fi.** PROJECT > UPDATE: CHECK, DOWNLOAD, then hold A on INSTALL. Every download is signed and
  checked (signature, size, SHA-256) before anything changes; your songs, samples, recordings and settings stay. If the
  new version does not start, the old one comes back by itself; hold A on ROLLBACK to go back by hand. AUTO CHECK looks
  once a day (Wi-Fi on, music stopped) and never downloads by itself. From now on you don't need to unzip by hand.
- **Top USB port: OZMA is the host.** Plug in a MIDI keyboard or controller, or a groovebox / sound card that needs no
  driver (tested: Elektron Tonverk). A groovebox gets OZMA's sound and tempo over one cable. Plugging
  it in mid-song, or again after a replug, starts it on the right step.
- **Bottom USB-C port: OZMA is the device.** The Brick becomes a sound card + MIDI port called OZMA for a computer
  (tested on Windows) or a phone or tablet, no driver needed, and it charges over the same cable.
- **Settings** (PROJECT screen):
  - AUDIO > OUTPUT: AUTO, a sound card on the top port takes over the sound; SPEAKER, the sound stays on the Brick.
  - AUDIO > USB AUDIO (bottom port): OUT, the Brick plays into the computer; IN, the computer plays into the Brick;
    OFF as usual. Takes effect the next time you start OZMA.
  - MIDI > CLOCK OUT ON: other gear follows OZMA's tempo and start/stop. MIDI > CLOCK IN AUTO: OZMA follows a clock.
  - Groovebox: OUTPUT AUTO and CLOCK OUT ON on OZMA; clock receive and transport receive on the groovebox.
- **Lessons.** MENU opens 19 short hands-on lessons, basics first. A coach line shows each step and its buttons and
  ticks it off when you do it. The lessons build their own song (MYTRACK), so yours stays safe. The first launch
  offers the course: A LET'S GO, B LATER, X NEVER.
- **The hangar says what each engine is** (wavetable synth, FM bass and drum synth, chord and supersaw synth...) and
  its key limits, like how many voices it plays.
- **Smoother controls.** In JAM, R1+L2 undoes and R1+R2 redoes, while you play and on the JAM card. A quick tap on R1
  alone no longer jumps to another screen (hold R1 for the map, R1 + d-pad for screens). CLIP LIST always shows
  R1+X GRID.
- The zip has a `usb/` folder with OZMA's two USB drivers (Linux kernel modules, GPL-2.0). Their source is
  `OZMA-0.8.2-usb-gpl-source.zip` on the release page.

`OZMA-0.8.2.zip` sha256: `6efc1a45540aff0087766e7df30e37fb522ee5ccfdbc84972b7e9d411cd54f57`
`OZMA-0.8.2-usb-gpl-source.zip` sha256: `a53595cdb4f20bea8549ad3fff0d6e21e414a9696c3719cda8ba69ceecc9d4fc`

## 0.8-beta.1 (2026-11-07): first open beta

- A standalone music tracker that runs on the TrimUI Brick itself: 8 tracks, STEP and LOOP tracks, a LIVE and
  SONG grid of clips, trig conditions, probability, micro timing, retrigs, slides, parameter and sound locks.
- Instruments: ATLAS, KEPLER, ORBIT, CLUSTER, LUNA, SAMPLER (slices, warp, TO SAMPLER chops) and MIDI OUT.
- Mixer and effects: chorus, delay, reverb, master OTT, EQ, DJ filter and limiter; SCENES, PERFORM, QUICK MIX.
- JAM: play the notes of a scale live.
- BOUNCE: print a row to audio and keep playing it as a LOOP clip.
- Three demo songs made only with OZMA's instruments (DEEP FIELD, REDSHIFT, ION DRIVE) and OZMA KIT, a set of
  drum and FX sounds free to use in your music.
- Runs on spruce; stock TrimUI OS and CrossMix are experimental.
- Not in this beta: USB audio to a computer.

`OZMA-0.8-beta.1.zip` sha256: `28c6b61ccd78657cb6188f06fda1d68c6fc1bdb0631f842a917a28f445b299da`

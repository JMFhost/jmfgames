# Casino Life audio — MANIFEST

All music is ORIGINAL, synthesized from sine/noise primitives with numpy
(`make-audio-casino.py`, adapted from Block Fall's proven `make-audio.py`).
No samples, no copyrighted melodies.

## Music loops — stereo 44100 Hz MP3 192k, 256 s each

| File | Bytes | Duration | Style |
| --- | --- | --- | --- |
| casino-lounge.mp3 | 6,145,297 | 256.00 s | Smooth lounge jazz — mellow piano + brushed drums + walking bass |
| casino-swing.mp3 | 6,145,297 | 256.00 s | Upbeat big-band swing — brass stabs + walking bass |
| casino-bossa.mp3 | 6,145,297 | 256.00 s | Bossa nova — nylon guitar + soft shaker + gentle piano |

Music subtotal: **18,435,891 bytes**.

Seamless-loop construction: each track is a 32 s cycle tiled x8. Every chord
fades in/out inside its 8 s slot, plus a 0.2 s fade at the cycle edges, so the
exact tile point is silent on both sides.

Loop-seam check (decoded MP3, ffprobe + waveform analysis, Nov 23, 2026):
- End-of-file 50 ms RMS: lounge 0.0059, swing 0.0020, bossa 0.0051
  (vs overall peak ~0.63) — file ends essentially silent.
- 32 s tile boundary (±50 ms): max amplitude lounge 0.088, swing 0.047,
  bossa 0.075; RMS 0.018 / 0.011 / 0.014 — no click, just the fade dip.
- End-to-start discontinuity: lounge 0.023, swing 0.005, bossa 0.009.
- PASS — loops seamlessly.

## SFX — mono 22050 Hz MP3 128k

| File | Bytes | Duration | Description |
| --- | --- | --- | --- |
| sfx-chip.mp3 | 3,387 | 0.12 s | Chip click |
| sfx-card.mp3 | 6,731 | 0.33 s | Card flip |
| sfx-dice.mp3 | 10,075 | 0.54 s | Dice roll rattle |
| sfx-wheel-tick.mp3 | 19,688 | 1.13 s | Roulette tick (12 slowing clicks) |
| sfx-coin.mp3 | 17,598 | 1.00 s | Coin cascade |
| sfx-win.mp3 | 37,242 | 2.24 s | Win fanfare arpeggio + chord |
| sfx-rocket.mp3 | 33,480 | 2.00 s | Launch whoosh |
| sfx-explosion.mp3 | 25,539 | 1.50 s | Crash boom |
| sfx-scratch.mp3 | 17,598 | 1.00 s | Scratch scrape |
| sfx-button.mp3 | 3,805 | 0.14 s | Soft button tap |
| sfx-deal.mp3 | 7,567 | 0.39 s | Card deal whoosh |

SFX subtotal: **182,710 bytes**.

## Total

**18,618,601 bytes** (14 MP3 files) — clears the 18,000,000-byte target.

Generator: `~/workspace/phone-work-casino-overhaul/make-audio-casino.py`
Verified with ffprobe (duration + bitrate + channels + sample rate) for every file.
No game code written; index.html untouched.

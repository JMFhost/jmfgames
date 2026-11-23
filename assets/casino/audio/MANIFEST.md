# Casino Life audio — MANIFEST

Music: Casino Life uses the shell/console music only (the 7 shell themes),
per Jesse's standing rule (Nov 23, 2026): NO per-game additional music.
The three casino music loops (bossa, lounge, swing — 18,435,891 bytes)
were REMOVED in the Nov 23, 2026 Casino Life themes fix and are not
part of this push set. The Music toggle controls the shell music.

All SFX below are ORIGINAL, synthesized from sine/noise primitives with numpy
(`make-audio-casino.py`, adapted from Block Fall's proven `make-audio.py`).
No samples, no copyrighted melodies.

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

**182,710 bytes** (11 MP3 files).

Generator: `~/workspace/phone-work-casino-overhaul/make-audio-casino.py`
Verified with ffprobe (duration + bitrate + channels + sample rate) for every file.
No game code written; index.html untouched.

slate-v22 (2026-09-04):
  Listen false-positive harden: frequency Listen needs sustained peak
  (streak) + higher absolute/ratio floor; trained sound peak floor 0.012
  and 2-check streak; generic clap tighter; default matchTol 0.90.
  Master Choose frequency: clear stuck recBusy; auto-run Scan ambient
  (environment analyzer → Recommended Hz → Test → Use).

Second Sticks (working title; not final App Store)
MAAM = internal/code/repo only
(dummy film slate)
=================================

Open index.html in Safari. Best: host the folder on GitHub Pages or
Netlify (free, https), then Share → Add to Home Screen.

HOW THE DAY WORKS
  Watch 3 short ads on Home. Slate, Train, and Log unlock for 24 hours.
  Ads never appear on the board the camera sees.
  These ads are placeholders. Real AdMob needs a native iOS/Android app.

DONATIONS
  Paste your Ko-fi / PayPal.me / Cash App / Stripe link in More.
  Tips are separate from ads. After you tip you can unlock the day
  without watching ads (honor system — a web page cannot verify PayPal).

LISTEN
  Tap Listen, hold the board up to camera, make the mark sound (or tone).
  Generic mode: any sharp clap / snap.
  Trained mode: active mark — sound fingerprints or frequency band.
  Board trained Listen matches like Test for sound marks (rolling peak
  cosine). Frequency marks watch a narrow FFT band above ambient.
  Enroll success shows a big GOT IT confirm.

MOCK DEVICE ROOM (slate-v20)
  Home or More → Room: Create room (5-char code) or Join room.
  Master pushes shared board fields (not Camera) on field blur, after
  Mark/take bump, and via Push now. Followers apply pushes; cam stays local.
  Transport: BroadcastChannel name “second-sticks-room” + localStorage key
  slate-room-CODE (storage event) — works same-browser tabs / same-origin
  profiles that share storage. Two different phones on GitHub Pages alone
  cannot sync (localStorage is per-device). Optional: More → LAN sync
  WebSocket URL (ws://LAPTOP-IP:8787) after running sync-server on Wi-Fi.
  Origin owns real multi-device sync later. Honest mock for weekend tabs.

ROOM TEST STEPS
  1) Tab A: Master → Create room → note code → edit Scene/Take → Push now.
  2) Tab B (same origin): Follower → Join room with that code → fields apply.
  3) Tab A: Mark (take increments) → Tab B should get new take.
  4) Two phones: set LAN sync URL to a laptop running sync-server, or wait
     for Origin. Pages + BroadcastChannel alone will not bridge devices.

MASTER SLATE PATH (slate-v19)
  Master happy path is slate-centric: Open slate → Choose frequency or
  Choose custom sound (strip CTAs) → after Use/save return to Slate →
  when the active mark is a frequency, Broadcast plays that Hz for
  followers/cameras (playFreqTone). Train tab remains for library/power users.
  Follower UI unchanged (Train sync, Listen to sync, Test).

FOLLOWER HOME (slate-v17)
  When This device = Follower: Home stack is Watch ads · unlock (if locked),
  Train · learn sync mark (primary), Open slate, then tip. Lede shortens to
  “Follower board — learn the master’s sync mark, then Listen to sync.”
  body.role-follower keeps follower-only CTAs visible; paintPro never hides
  btnHomeTrainFollow. Slate: Listen to sync is the dominant control.

MASTER / FOLLOWER (slate-v16)
  state.role = master | follower (default master — single-device testing unchanged).
  Home or More → This device is Master / Follower.
  Master: full Train, Learn frequency (scan→recommend→Test→Use/Change), Learn sound,
  full slate edit, mark library delete tools.
  Follower: Train = Learn sync mark (enroll sound OR Use master’s frequency / Listen·lock
  tone — no open-band Learn frequency). Slate: Listen to sync (trained/freq only → sticks
  + SYNC HEARD + toast that board would update from master when connected), Test the mark
  (MATCH/HEARD confirm), Mark escape. Shared board fields read-only; Camera stays local.
  Room mock (slate-v20) uses BC+localStorage; optional LAN sync-server URL in More. Fingerprints only. Not LTC.

MARK NAMES (slate-v16)
  Default save name = today’s date (MM.DD.YYYY via todayStr) + abbreviated frequency
  or Mark/Sound — not the words “Today’s Date…”. Examples: 09.04.2026 · 15.3kHz,
  09.04.2026 · 15kHz, 09.04.2026 · Mark (· Sound / · Mark 2 on collision).
  Prefills trainNameInput; maxlength 48.

MARK LIBRARY (slate-v15)
  Each mark is its own library entry (fingerprints only — never raw WAV).
  state.marks[{ id, name, kind, prints|hz, created }] + activeMarkId.
  Migrate: old single prints[] → one “Mark 1” sound mark, set active.
  Train tab: list, tap to activate, Learn new sound, Learn frequency,
  Rename, Delete, Test listen. Slate shows Mark: name near Listen;
  Change / Learn sound / Learn freq. Scene change asks keep vs pick.
  Learn new sound reuses #trainOverlay (Yes → 5…0 → Make Noise → GOT IT
  → name). Extra samples append to the active sound mark until Learn new.

FREQUENCY MARKS (MVP / Pro-path test)
  kind: "frequency" stores { hz, bandHz }. Train → Learn frequency:
  1) Scan ambient ~1.5s → Recommended: NNNNN Hz (quietest bin ~12–20 kHz,
     or 8–18 if Nyquist is weak). 2) Test the mark — plays that Hz from
     this speaker. 3) Use this frequency → name & save, or Change frequency
     → back to scan/slider, re-test. Manual “or pick Hz” slider 1000–20000.
  Listen: soft energy above ambient in that band → sticks slam. Honest
  limit: near-ultrasound may fail on some iPads / speakers; weak ambient
  scan warns you. Test with a Samsung S22 tone generator (or same-device
  Test the mark) aimed at the slate mic while Listen is armed.

TRAIN A CUSTOM SOUND MARK
  Train tab → Learn new sound or Record → “Ready…?” → Yes → countdown
  5…4…3…2…1…0. Mic opens on Yes and stays warm through the countdown
  (iPad-friendly). Capture starts 0.5s before 0; at 0 the overlay says
  “Make Noise now” for the rest of a 1s window. Print = peak-energy
  structure. Fail floor is low; errors show measured peak RMS.
  Repeat 5 times (save allowed at ≥3). Test listen (~3.5s). Match
  threshold (More) sets cosine strictness. Fingerprints only — no WAV.

MARK
  Tap Mark or the sticks if Listen misses. Always available once the
  day is unlocked.

MIC
  Safari over https or a Home Screen app from a hosted page.
  Opening the raw file from Files often cannot use the microphone.
  Train keeps the mic warm from Yes through the 1s capture so iOS does
  not hand back a silent stream after stop/reopen.

PRIVACY
  Mic is on while Listen is armed, or from Train Yes through the ~1s
  capture (including the 5…0 countdown), or during frequency scan.
  Matching is on-device. Mark fingerprints / Hz and the shot log stay in
  localStorage (slate-app-v2). Reusable across shots. No raw enrollment
  audio. No account, cloud, or analytics. Placeholder ads are not AdMob.

DISCLAIMER
  Dummy slate. The clock is wall time, not LTC. Fast enough to cut with.
  Not a Denecke. External tips are not tax-deductible.


IPAD MVP
  Host this folder on https (GitHub Pages or Netlify).
  iPad Safari → Share → Add to Home Screen.
  Open the Home Screen icon, rotate landscape, unlock the day, Open slate.
  Scene / take type is sized for a camera across the set. Nav stays off the board face.
  Mic still needs https. file:// from Files usually cannot listen.
  Near-ultrasound frequency marks are not proven on all iPads.
  Not an App Store binary. Not LTC. Not a lockit box.


MORNING SETUP
  After you unlock the day (ads or honor tip), a first-sign-in flow opens.
  Step 1 — Train Your Mark: Record → ready Yes → countdown 5…0 →
  Make Noise now (~1s peak window; five times). Fingerprint only, not
  a recording. Or skip and use Learn frequency from Train later.
  Step 2 — Test: make the sound / tone once; MATCH means you are ready.
  Step 3 — Board: Listen → hold up → make the mark → take is logged.
  You can skip to generic clap, or keep yesterday’s mark if you already trained.

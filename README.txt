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

MARK LIBRARY (slate-v14)
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
  Scan ambient ~1.5s, pick quietest bin in ~12–20 kHz (or 8–18 if the
  device Nyquist is weak); confirm with a short speaker tone; name & save.
  Manual Hz slider 1000–20000 when auto-scan fails. Listen: soft energy
  above ambient in that band → sticks slam. Honest limit: near-ultrasound
  may fail on some iPads / speakers; weak ambient scan warns you.
  Test with a Samsung S22 tone generator (or same-device Play tone) aimed
  at the slate mic while Listen is armed.

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

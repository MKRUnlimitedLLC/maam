MAAM — Make Anything A Mark
(working name; dummy film slate)
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
  Tap Listen, hold the board up to camera, make the mark sound.
  Generic mode: any sharp clap / snap.
  Trained mode: only the sound you enrolled.

TRAIN A CUSTOM MARK
  Train tab → Record → “Ready to record your mark?” → Yes → countdown
  5…4…3…2…1…0. Mic opens on Yes and stays warm through the countdown
  (iPad-friendly). Capture starts 0.5s before 0; at 0 the overlay says
  “Make Noise now” for the rest of a 1s window. The sample fingerprint
  is the prominent/peak-energy structure in that second, not a flat
  average of silence. Fail floor is low; errors show measured peak RMS.
  Repeat 5 times. Test listen (~3.5s peak window, always shows MATCH/NO MATCH 0.xx). Match threshold (More) sets how strict
  cosine match is (lower = looser). Fingerprints only — no raw audio.

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
  capture (including the 5…0 countdown). Matching is on-device.
  Fingerprints and the shot log stay in localStorage. No raw enrollment
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
  Listen / Train algorithms are unchanged. Noisy-room enrollment is not proven yet.
  Not an App Store binary. Not LTC. Not a lockit box.


MORNING SETUP
  After you unlock the day (ads or honor tip), a first-sign-in flow opens.
  Step 1 — Train Your Mark: Record → ready Yes → countdown 5…0 →
  Make Noise now (~1s peak window; five times). Fingerprint only, not
  a recording. That print is the mark Listen will fire on. Match
  threshold in More.
  Step 2 — Test: make the sound once; MATCH means you are ready.
  Step 3 — Board: Listen → hold up → make the mark → take is logged.
  You can skip to generic clap, or keep yesterday’s mark if you already trained.

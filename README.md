# EMERGE — Sound v3 Deploy

Stamps: SCENE 1 v19.53 keyboard stays up, SIDEREAL v19.23, TROPICAL v18.32. Routes ?v=1923 / ?v=1832, engine ?v=3.
Deploy the WHOLE folder together, plus "Sidereal Solar System.mp4" and "Tropical Solar System .mp4"
(exact names, note the space before .mp4 in the Tropical file) in the repo root.
calc-sky.mp4 can stay in the repo but is no longer played. Verify the on-screen stamp before judging sound.

v3 changes:
1. Two-perspectives screen now has its own bed (19_two_perspectives.wav): the void hands off
   to two barely-detuned low voices with one slow interference cycle, the duality made audible.
2. Digit tones are now GENERATED in the engine, not a sound file: one fixed clock-set beep,
   identical pitch and level on every keystroke. No file, no cache, cannot be inconsistent.
3. The calculation layer breathes out over ~2s before the page turns; no hard cut into
   the reveal's held silence.
4 & 6. The recurring whoosh during chart drawing (both systems) was the breath bed (13)
   swelling on its loop; it is fully retired. The drawing now plays dry: construction,
   sweep, tokens only.
5. REVEAL MY CHART: new angelic ascension (20_reveal_ascension.wav) blooms with the light
   beam, a choir of pure harmonics entering low to high, layered over the clean impact.

Scene 1 v19.51 — persistent back navigation:
- Prominent BACK pill (peach/champagne gradient) sits beneath the birthplace country
  inside the globe marker, visible on the date and time steps only.
- Date screen: BACK returns to the birthplace search. Time screen: BACK returns to the
  date of birth. One button, its meaning follows the screen.
- Backward navigation preserves entered values: date, time, and birthplace are never
  cleared by Back. Re-entering a value overwrites the saved one through the normal
  input handlers.

Scene 1 v19.52 — direct to reveal (TEST BUILD):
- The calculation scene has moved out of index.html: tapping a system card saves the
  payload as before, then routes straight to the selected reveal page. Genesis code and
  CSS remain in the file but are no longer called (easy rollback); calc-sky.mp4 is no
  longer preloaded or played.
- Each reveal file now opens with its own system-specific solar-system movie
  (object-fit:contain, plays once, muted): Sidereal = classical grahas, Tropical =
  includes the outer planets. "Calculating your sky" + cycling status lines sit over it.
- Tap-to-reveal is gated: pointerdown does nothing until the movie has ended and faded.
  Only the user's tap after that sets t0 and starts the existing chart timeline.
  Fallbacks (autoplay rejection, video error, 12s watchdog) skip the intro rather than
  trap the user.
- Back → Date → Time fix: returning to a previously entered birth time highlights it,
  so the first keystroke replaces it cleanly and the HH:MM field + AM/PM pills are fully
  functional again.
- Sound untouched this round: no audio files renamed, emerge-sound.js unmodified, the
  old genesis calc loop simply no longer runs. Movie soundtrack sync comes later.

Scene 1 v19.53 — keyboard stays up:
- Birth Time focus fix only: the fourth time digit no longer blurs the input, so the
  iPhone keyboard stays open and the visualViewport lift holds the prompt + HH:MM box
  in their raised position while AM/PM is chosen. AM still arms as the default; the
  pills stay tappable with the keyboard up; completion proceeds exactly as before.

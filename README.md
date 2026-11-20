# Color Clash Academy v4.0 — UNO Reaction Challenge

Color Clash Academy is an educational color-matching card game for grades 5–8. It runs entirely in the browser with no student accounts.

## New in v4.0

- Dedicated UNO and CATCH controls, with U and C keyboard shortcuts in solo/tournament play.
- A visible reaction countdown immediately after any card play that leaves exactly one card. The first valid call wins. Educational questions and wild color selection wait until the race finishes.
- Classic (2 cards), Competitive (4 cards), Chaos (7 cards) and Disabled penalty modes. False/early calls draw 2 cards. If nobody makes a valid call before time expires, the round continues without a penalty. UNO penalties bypass Knowledge Shields.
- Adjustable reaction profiles (independent of normal card-playing difficulty): Standard, Relaxed, Speed Challenge, Expert. Standard is the default.
- Solo, tournament and shared-device play. Shared-device races have labeled buttons for each opponent; the U key declares for the one-card player.
- UNO reaction statistics, visual feedback, reduced-motion and high-contrast support.
- A compact arena layout for shorter Chromebook screens.

### Standard AI reaction timing

| Opponent difficulty | Random reaction time | Chance of forgetting its own UNO call |
| --- | --- | --- |
| Easy | 2.5–5.0 seconds | 35% |
| Normal | 1.5–3.5 seconds | 20% |
| Hard | 0.8–2.0 seconds | 10% |
| Expert reaction profile | 0.5–1.5 seconds | 5% |

Relaxed increases reaction timing by 65%; Speed Challenge reduces it by 25%. Rivals may also miss a catch or occasionally make a false call. Each rival reacts independently; these timings and probabilities are initial tuning values, not measured student reaction times. A reaction window lasts the slowest configured AI delay plus 0.7 seconds. The timer pauses when the page is hidden. Settings are applied to new matches; an existing saved match retains its stored UNO settings.

## Existing v3.0 features retained

- Card travel and match-start animations, rival characters and speech bubbles.
- Prism Classic, Arcane Glow, Neon Arcade, Pixel Pop and Nature Quest deck styles.
- House rules: stacking, draw-until-playable, force play, 7-0 hand swap/rotation and starting hand size (5, 7, or 10).
- Original educational question bank, solo/pass-and-play/tournament modes, local progress, saves, collectible card backs and achievements.

## Install

Replace `index.html` and `README.md` in the existing `color-clash-academy` GitHub repository. No PlayForge homepage changes are needed. Keep any other repository files if you have added them. Existing browser-local progress is not intentionally reset.

## Verification

The baseline was reconstructed and matched the live GitHub blob SHA `f44e9dfcd7ca864ce9c104e45e6243f55522e7fa` before changes. All JavaScript passed syntax checks. Automated Chromium scenarios checked human declaration, AI declaration and timing, successful and false catches, timeout, Chaos/Competitive penalties, color selection, question sequencing, pass-and-play, disabled mode and restart cancellation. Browser tests loaded HTML directly with a localStorage test shim because the runtime blocks local URL navigation. Real student reaction balance and live GitHub Pages deployment remain to be verified.

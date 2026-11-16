# Color Clash Academy — Expanded Edition v2.0

An original, colorful, educational color-matching card game for grades 5–8, with Foundations questions, designed for the Naches Learning Hub. No student account or backend is required.

## How to launch

1. Create a new public GitHub repository (suggested: `color-clash-academy`).
2. Upload `index.html` to the repository root.
3. Enable **Settings → Pages → Deploy from a branch**, selecting the main branch and root folder.
4. Open your GitHub Pages website. `index.html` is the only file needed to PLAY; the CSV and README are for teachers and maintainers.

You can also open `index.html` directly in a browser. Progress and saved matches depend on the browser's storage settings. GitHub Pages hosting is recommended.

## Play modes

- **Solo Arena**: face three AI opponents. Set Friendly, Skilled, or Master difficulty in Settings.
- **Pass & Play**: 2–4 local human players share one device. Hand-off screen conceals the next player's hand. Players must look away between turns. Learning challenges appear on the active player's turn.
- **Prism Tournament**: five stages in Math, Grammar, Science, History, and Technology. Stages unlock through victories. A loss allows retry without resetting your tournament stage.

## Rules

The match follows its own original rules, inspired by color-and-number matching games. Play by matching color, number, or action symbol. Wilds change the active color. +4 requires the player to have no card of the active color. The first player to empty their hand wins. Action effects require educational questions for human players. Wrong answers cancel the action's effect, but the card still plays. The AI has difficulty-adjusted power activation odds.

Every second number card played offers an optional knowledge challenge by default. Correct answers earn Spark. At 3 Sparks, the game automatically makes the next player draw one bonus card and resets the Spark meter. When available, the Spark Power button lets students spend Sparks on:

- **Knowledge Shield** (2 Sparks): blocks the next draw-card penalty targeting that player.
- **Color Storm** (3 Sparks): gives a selected opponent two cards.
- **Double Challenge** (2 Sparks): answer two questions correctly to make a rival draw two.
- **Second Chance** (2 Sparks): save one retry for a later incorrect knowledge challenge.

These are **Spark skills**, not extra physical cards. There is no paid economy or in-app purchase system.

## Question bank

There are **1,011 distinct question prompts** in the embedded bank (not 1,011 independently verified pedagogical concepts). The questions are selected from:

- Grammar Kingdom (edited and de-duplicated)
- Naches Knowledge Showdown (selected questions)
- Original Color Clash Academy math, science, history, and technology prompts

Each item includes subject, grade band, four answer choices, correct answer, brief explanation, and source. All questions are embedded in `index.html`; `TEACHER_QUESTION_BANK.csv` is provided for easy review and editing. Editing the CSV **does not automatically modify the game**. To update gameplay questions, they must also be replaced in the `QUESTIONS` array in `index.html`.

Question selections avoid recent question IDs and randomize answer placement for each new encounter. The Mixed deck rotates among subjects, rather than sampling from a combined bank dominated by Grammar.

The bank has undergone structural checks (unique prompt text, four unique options, valid correct-answer marker, and nonempty explanations), but is **not a substitute for teacher review of academic content**.

## Achievements and local storage

- 47 earnable achievement milestones (including subject-specific mastery), five selectable card backs, points, per-subject accuracy, streaks, and lifetime stats.
- `Awards & Stats` includes a JSON export and import for transferring progress between Chromebooks.
- `Save Match` saves a stable point in the current game to the device; the Home screen offers `Resume saved match`.
- **No cross-device automatic sync.** All progress is browser-local. Clearing browser storage, private browsing, or switching devices can erase progress unless exported.
- Stats are **practice indicators**, not verified grading evidence. Students control browser-local data, and exported JSON is user-editable. Do not use this data as secure assessment proof.

## Teacher and accessibility settings

- AI difficulty: Friendly / Skilled / Master.
- Question timer: none / 15 / 30 / 60 seconds.
- Challenge frequency: special cards only / default / every number card.
- Optional fixed subject for subsequent Solo or Pass & Play matches.
- High-contrast color cards with shape symbols, and reduced-motion mode.
- Interactive five-step tutorial and in-game rules.

These are convenient local settings, **not password-protected restrictions**. Anyone using the device can change them.

## Technical details

The app is one self-contained HTML file with inline CSS, JavaScript, graphics, sound effects, and questions. It uses no external fonts, analytics, images, scripts, accounts, APIs, or servers. Works best in recent Chrome, Firefox, Safari, and Edge.

## Originality

Color Clash Academy uses original naming, card visuals, characters, and educational gameplay rules. It is not affiliated with or endorsed by UNO or its rights holders.

## Known limitations / follow-up ideas

- A pass-and-play game relies on players honoring the privacy hand-off. Other people must look away from the screen.
- AI is heuristic-based, not a perfect expert opponent.
- Shared devices share local progress unless a different browser profile is used.
- Exported local progress is not tamper-proof.
- Multiplayer across multiple devices/networking is not yet available.
- Teacher should review question content before using for graded assessment.

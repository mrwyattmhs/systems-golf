# Elimination Golf ⛳

A 9-hole golf game for learning to solve 3-variable systems of equations by elimination. The whole point: **reading the system before you touch a pencil is the skill.** Strokes punish brute force, reward intuition.

**Play it:** everything is one file — `index.html`. No build, no server, no dependencies.

## Put it on GitHub Pages

1. Create a new repository (e.g. `elimination-golf`).
2. Upload `index.html` to the repository root (drag-and-drop on github.com works).
3. Go to **Settings → Pages**, set **Source** to `Deploy from a branch`, pick `main` and `/ (root)`, save.
4. Your game is live in about a minute at
   `https://<your-username>.github.io/elimination-golf/`

Share that link with students — it works on phones, tablets, and laptops. (You can also just double-click `index.html` locally.)

## How a hole works

| Phase | Golf name | The decision |
|---|---|---|
| 1 | **The Read** | Which variable's coefficients cooperate? Pick the variable to eliminate — it must vanish from *two different pairs* of equations. |
| 2 | **The Approach** | On the resulting 2-variable system, choose multipliers so the target column **sums to zero**, then add the lines. |
| 3 | **The Putt** | Back-substitution. Free — watch the values roll home. |

## Scoring

- Each **combine** (adding two lines) = 1 stroke
- Each multiplier that isn't ×1 / ×−1 = 1 stroke
- Multipliers past ±10 are **out of bounds**: +1 penalty and back to the tee (stroke and distance)
- Putts (back-substitution) are gimmes — free
- Par = the strokes of a perfect read. Beat it for birdies.

Every hole is generated fresh: integer solutions, no zero coefficients, all coefficients under 16, and a guarantee that a perfect read can always finish in bounds. Later holes plant hazard variables — coefficient triples where the *tempting* pair is cheap but the second elimination is impossible. Reading both eliminations before committing is the lesson.

## Classroom notes

- **Perfect read ⭐** is tracked separately from strokes on the scorecard — a student can shoot bogeys while still learning to read correctly, and see that progress.
- **Ask Caddie** on any shot teaches the LCM reasoning without giving the multipliers away.
- **Take a Drop / Pick Up Ball** (menu) keep anyone from getting permanently stuck.
- Best round is saved locally in the browser.

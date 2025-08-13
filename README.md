# Guillotine League Arcade (Static Site)

A sleek, single‑page website with mini‑games and tasks that award **credits** to your league members.  
At the end of each week, the **top credits** earner gets **first choice of draft pick**.

No backend needed — everything runs in the browser and persists via `localStorage`.  
If you want to sync across devices, use **Export/Import** from the Leaderboard tab.

## Features

- 🎮 **Mini‑games** with sensible daily limits:
  - **Daily Trivia**: 5 questions/day, +1 credit per correct.
  - **Field Goal Timing**: skill meter, 3 attempts/day, +1 credit per make.
  - **Reaction Drill**: click on green; under 300ms = +1, under 200ms = +2.
  - **Memory Match**: complete fast to earn +1 or +2 (1 run/day).
- 🏆 **Leaderboard**: live ranking with last activity timestamps.
- 🛠️ **Commissioner Console**:
  - Set the **week window** (defaults to next Monday → Sunday).
  - Add/rename/delete players; manual awards (for off‑site tasks like memes).
  - End week & auto‑advance window; zero all credits; audit logs.
- 💾 **Export / Import** data as JSON for backup or sharing.
- 🔐 **PINs**: Players set a 4‑digit PIN on first login; commissioner has a separate PIN.

## Get Started

1. Open `index.html` in your browser (or host on GitHub Pages / Netlify).
2. Go to **🛠️ Commissioner** tab and set a Commissioner PIN (first unlock sets it).
3. Add your league’s players.
4. Share the page. Players select their name, set a **4‑digit PIN**, and play.

## Week Ending & Winner

Use the **End Week & Reset** button in the Commissioner tab. It'll:
- Announce the winner (top credits)
- Reset credits/logs
- Auto‑advance the week window by 7 days

You choose how the winner claims the **draft slot** (e.g., first pick of any slot).

## Notes

- This is a static site. If you want cross‑device, real‑time sync, wire in a small backend (Firebase, Supabase) by replacing the `saveData`/`loadData` functions.
- Anti‑cheat is minimal by design. For higher integrity, run play sessions in a shared screen meetup or ask owners to record screens for big payouts.
- You can tweak game rewards/limits in `index.html` JavaScript (search for `FIELD GOAL`, `Reaction`, `Memory`, `TRIVIA_BANK`).

Have fun and may the axe spare you. 🪓

# TempoTrainer

A single-file HTML workout tempo trainer with voice control. It guides you through
concentric (Op), isometric hold (Vast), and eccentric (Neer) phases with a full-screen
overlay, per-second countdowns, audible beeps, and progress tracking.

## Features

- **Phase countdowns** — Op / Vast / Neer phases count down remaining seconds on the overlay
- **Audio beeps** — WebAudio ticks, phase-start tones, and start countdown (no external files)
- **Voice control** — Dutch speech commands to start, pause, resume, restart, stop, adjust tempo, and more
- **Fullscreen mode** — button, `F` key, or voice
- **Keyboard shortcuts**
- **Progress bar & stats** — live fill, set/rep counters, remaining time (localStorage)
- **Rest phase** between sets

## Usage

1. Open `index.html` in a modern browser (Chrome / Edge recommended).
2. Set **Op**, **Vast**, **Neer**, **Reps**, **Sets**, and **Rust**.
3. Press **Start (s)** to begin.
4. Follow the overlay countdown; the background color changes per phase:
   - Red = Op (up)
   - Orange = Vast (hold)
   - Blue = Neer (down)
   - Green = Rust (rest)

## Controls

| Action           | Button / Key  | Voice            |
|------------------|---------------|------------------|
| Start            | Start / `S`   | "start"          |
| Pause / Resume   | Pauze / Space | "pauze" / "verder" |
| Restart          | —             | "opnieuw"        |
| Stop             | Stop / `Esc`  | "stop"           |
| Fullscreen       | FullScreen / `F` | "beeld" / "scherm" |
| Faster (all)     | —             | "snel"           |
| Slower (all)     | —             | "lang"           |
| Op faster/longer | —             | "op" / "trager"  |
| Vast shorter/longer | —         | "kort" / "houden" |
| Neer faster/longer | —          | "vlot" / "neer"  |
| Rest longer/shorter | —         | "rust" / "minder" |
| Reps +1          | —             | "rep"            |

> Note: voice recognition requires browser speech support and microphone permission.
> The settings inputs are the source of truth; voice commands adjust them live.

## Files

- `index.html` — the entire application (single file, no dependencies)

## Notes

- (Obsolete) Training stats and history are saved to `localStorage`.
- The `totalTime` / `Resterend` values recompute live when settings or voice change.

# Per Aspera

*Per aspera ad astra.* A CrossFit WOD timer made to look like the LED clock on the box wall. It runs on your phone, a laptop, or a Fire TV hooked up to the gym display.

**▶ Live: https://ultra-sonic.github.io/per-aspera/**

It is one static `index.html` with no build step and no dependencies apart from a Google Font. It works offline once the page has loaded.

## Features

### Timer modes

| Mode | What it does |
|---|---|
| **For Time** | Counts up, with an optional time cap. |
| **AMRAP** | Counts down from the set duration. |
| **EMOM** | Restarts every *n* seconds for a set number of rounds. |
| **Tabata** | 20 s work / 10 s rest × 8 by default. All three values can be changed. |
| **Intervals** | Your own work, rest and round counts. |

### Display

- A six-digit LED panel like a wall timer. The round number is in white and the time is in green.
- The time turns **red** during rest and **amber** during the 10-second countdown.
- **1/100 s toggle:** switches the panel to `MM:SS.hh` with tenths and hundredths of a second, counting up or down depending on the mode, including the optional 10-second countdown. Final time, total and split times show hundredths too. The round number then moves to the stats row under the clock.

### Sound

- A 3-2-1 beep before every transition.
- A long tone at the start and at the finish.
- A double beep at checkpoint times.

### During a workout

- **+ Round** records split times.
- **Stop** freezes your final time on screen.
- **Reset** clears everything and starts over.

### Screen and fullscreen

- Pressing **Start** switches to fullscreen.
- The screen stays on while the timer runs. This uses the Screen Wake Lock API, with a silent looping video as a fallback for browsers that don't support it.
- In landscape the clock fills the screen, with a low button bar underneath.

### Presets

- **CrossFit Open:** every Open workout from 11.1 to 26.3. You can filter by year or search by movement. Workouts whose time cap extends as you finish stages (13.5, 17.3, 19.2, 23.3) run as For Time and beep at each checkpoint.
- **Benchmarks:** Fran, Cindy, Grace, Helen, Annie, Diane, Elizabeth, Karen, Jackie and Nancy, with Rx loads.

Rx loads are listed as men/women in lb. Check the official standards on [games.crossfit.com](https://games.crossfit.com) before you compete.

## Fire TV support 📺

You can show the timer on a Fire TV stick connected to the box display and run it with the normal remote.

### Setup

1. On the Fire TV, install **Amazon Silk**. You can search for it or say *"Alexa, open Silk"*.
2. Open `ultra-sonic.github.io/per-aspera` and bookmark it.
3. Press **Start** and the timer goes fullscreen. If it doesn't, press the ☰ menu button on the remote to turn on fullscreen.
4. Turn off the Fire TV screensaver: **Settings → Display & Sounds → Screensaver → Start Time → Never**. The page asks the browser to keep the screen on, but a TV may not allow it, so this setting is the reliable fix.

### Remote control

| Remote button | Action |
|---|---|
| ⏯ **Play/Pause** | Start / pause / resume |
| **OK** (center) | Count a round |
| ⏩ **Fast-forward** or ↩ **Back** | Stop and keep the final time |
| ⏪ **Rewind** | Reset |

When the timer recognises a button press, it shows a short label at the top of the clock. If nothing appears when you press a button, Silk isn't passing that button to the page. In that case, open an issue and say which button it was.

## Keyboard

| Key | Action |
|---|---|
| `Space` | Start / pause |
| `Enter` / `L` | Count a round |
| `F` / `Esc` | Stop |
| `R` | Reset |

## Install on a phone

Open the page in your mobile browser and choose **Add to Home Screen**. It then starts fullscreen like an app.

## License

[MIT](LICENSE) © 2026 Oliver Markowski

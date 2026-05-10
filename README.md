# Guitar Scale Trainer

A self-contained, offline-capable guitar practice app for the **25-week CAGED scale programme**. Works on iPad, iPhone, and desktop — no installation required, just open the HTML file.

## Live App

👉 **[Open Guitar Scale Trainer](https://evgeniberenstein.github.io/guitar-scale-trainer/)**

## Features

### 25-Week Programme
- 19 scales across all styles: Major, Minor, Pentatonic, Blues, Modes, Harmonic Minor, Whole Tone, Diminished
- **Every 4th week** is a test week — 8 questions on notes, chords, relatives & formulas
- **Weeks 26–32**: C Major Complete — 7 modal patterns (Ionian → Locrian), K. Hicks method

### CAGED Position System
- 5 positions per scale across the full neck
- Interactive SVG fretboard diagrams with Note Names / Scale Degrees / Finger # modes
- Relative scale toggle (e.g. A Major Pentatonic ⇄ F# Minor Pentatonic)
- Relative root highlighted in teal on all diagrams

### Chord Voicings
- Diatonic chord diagrams for every position
- Voicings sourced from the CAGED system (E-shape, A-shape, D-shape barre chords)
- All 12 keys × major / minor / dim / hdim / dom7 / maj7 / min7
- Labels: Note Names, Scale Degrees, or Finger Numbers

### Mic-Based Practice
- **Scale Runs** — pitch detection via Web Audio API autocorrelation
  - Detects notes in real time, verifies against scale
  - One complete run (play up & down, then pause) = 1 rep counted
  - Shows live note name + ✓ In scale / ✗ Wrong note
  - Run history with accuracy % and problem notes flagged
- **Chord Plays** — amplitude detection, counts one chord sequence per pause

### Metronome
- Web Audio API scheduler (precise timing, no drift)
- BPM: 20–300, adjustable by ±1 or ±5
- Visual beat indicator (4/4)
- Sessions logged to daily practice log

### Practice Tracking
- **30 scale reps + 30 chord reps** per position = position complete
- Timer per position (2:10 default, auto-starts with mic)
- **Daily Practice Log** — per-day with date, scale name, accuracy, problem notes, metronome sessions
- Weekly rep summary per position
- Progress heatmap and test score history

### Offline-Capable
- All chord voicings embedded locally (~5KB)
- Pitch detection runs on-device (Web Audio API)
- State saved to localStorage
- Only Google Fonts requires internet (falls back to system serif/monospace)

## Usage

1. Download `guitar-scale-trainer.html`
2. Open in Safari (iOS/macOS), Chrome, or any modern browser
3. Allow microphone access when prompted for mic-based rep counting

No build step. No dependencies. No server.

## References

- **Chord voicing shapes**: CAGED system (public domain music theory)
  — Reference: [tombatossals/chords-db](https://github.com/tombatossals/chords-db) (MIT License, © 2015 David Rubert)
- **Modal scale patterns (Weeks 26–32)**: K. Hicks method, MUS1131 Guitar Ia
- **Pitch detection**: Autocorrelation algorithm (public domain)
- **Fonts**: IM Fell English SC & Courier Prime (Google Fonts, OFL)

## License

MIT — free to use, modify, and share.

# Guitar App — Plan

## What it is

A standalone low-latency guitar processing app. Open it, plug in, play.
No project files, no setup wizard, no waiting. Faster than opening a DAW.
Remembers everything from last time.

---

## The problem it solves

Opening a full DAW (Pro Tools, Reaper, Studio One) just to noodle on guitar
is overkill. This app does one thing well: get a processed guitar signal
running as fast as possible.

---

## Signal chain

```
Guitar
  └─ Audio Interface
       └─ [Pre-IR VST Bank]  ← 3 slots (gate, compressor, amp sim, etc.)
            └─ IR Loader     ← cab/room simulation
                 └─ [Post-IR VST Bank]  ← 3 slots (delay, reverb, etc.)
                      └─ Output (headphones / monitors)

Tuner — taps the input signal in parallel, always visible, never in the chain
```

---

## Features

### Audio engine
- Detects and lists available audio interfaces on startup
- Lets you choose input/output device and buffer size (buffer size = latency)
- Remembers your last interface settings

### Tuner
- Always visible — reads from the raw input signal before any processing
- Chromatic, accurate enough for quick checks before playing

### Pre-IR VST bank (3 slots)
- Loads VST3 plugins from your drive
- Typical use: noise gate → compressor → amp sim
- Each slot can be bypassed individually
- Plugins open their own editor window when clicked

### IR Loader
- Loads impulse response files (.wav / .aif) for cabinet/room simulation
- **Inline folder browser** — no popup dialog box
  - Left panel: navigate folders
  - Right panel: files in the selected folder
  - Click a file to load and audition immediately
- Remembers last folder and file

### Post-IR VST bank (3 slots)
- Same as pre-IR bank
- Typical use: delay → reverb → any other post processing

### Settings persistence
- On close: saves all loaded plugins, IR path, interface choice, and bypass states
- On open: restores everything exactly as left

---

## UI direction

Minimal, dark, professional. Single window.
Think hardware rack unit meets modern software — not a toy, not a DAW.
No clutter. Everything visible at once without scrolling.

---

## Technology

**JUCE** — a C++ framework used by professional audio companies to build
exactly this kind of app. Handles:
- VST3 plugin hosting
- Audio interface management (ASIO on Windows for low latency)
- IR convolution
- Plugin editor windows

This is a native app — not a web page. It runs directly on your computer,
which is what makes real-time low-latency audio possible.

---

## Build order (start small, work up)

1. **Audio passthrough** — interface in, interface out, hear yourself clean
2. **Tuner** — tap the input, show pitch, quick win
3. **One VST3 slot** — proves plugin loading works end to end
4. **IR loader with folder browser** — the most unique part of the UI
5. **All 6 VST slots** — expand from 1 to the full 3+3 layout
6. **Settings persistence** — remembers everything on next open
7. **UI polish** — make it look the way it should

Each step produces something that works before the next one starts.

---

## What could go wrong

- **Plugin crashes** — a badly behaved VST3 can take down the host; needs
  crash protection around plugin loading
- **Latency** — depends on the audio interface's ASIO driver quality;
  buffer size will be user-adjustable
- **IR formats** — need to handle at least .wav and .aif cleanly
- **Plugin GUI windows** — VST3 editors open their own OS windows;
  needs careful management so they don't float loose

---

## What this is NOT (v1)

- No recording
- No MIDI
- No preset system (beyond "remember last state")
- No built-in effects — everything comes from your own VST3s and IRs

These are things that could come later if you want them.

---

## Working title

Needs a name. Something short, one word. Not "GuitarApp".

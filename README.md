# WO Countdown

Live countdown to the end of a WATCHOUT 6 cue.

WO Countdown shows the time left until the end of a cue in WATCHOUT 6, without rendering a countdown video. Place a transparent container image on the timeline and stretch the cue to the length you need: WO Countdown reads the cue from the saved show file, follows the playhead live from the Production PC, and counts down to 00:00 exactly at the end of the cue.

## Features

- Container-based countdown — any timeline, any layer, as many cues as needed
- Follows the playhead in real time, including jumps, pauses and stops
- Overview of every timeline: state, position, active countdown or time to the next one
- Automatic reload of the `.watch` file within two seconds of saving the show
- Window / HDMI output, windowed or fullscreen on the chosen monitor, custom colours, optional timeline name
- NDI output with optional transparent background
- Web page output reachable from any browser on the network, with URL options for transparency and colours
- Bitfocus Companion custom variables — time, hours, minutes, seconds, total seconds, active flag, timeline, media
- Connection log for connections, disconnections and reconnections

## Use cases

- Speaker or stage countdown driven directly by the WATCHOUT show
- Countdown overlay in vMix or OBS via NDI or a transparent browser source
- Countdown on Stream Deck buttons through Companion
- Timing walk-ins, video playbacks and segments built on WATCHOUT timelines

## How to use

1. Select the show's `.watch` file with **Browse**
2. **Settings → Project → Create container PNG in project folder**, then import `WO_COUNTDOWN.png` into WATCHOUT
3. Place the container on a timeline, stretch the cue to the countdown length, and save the show
4. Enter the IP address of the Production PC and wait for **Connected**
5. Press **Open output** for the countdown window

## System requirements

- Windows 10 / 11 (64-bit)
- WATCHOUT 6 Production PC reachable on the network (TCP port 3040)
- NDI (optional): NDI runtime available on the PC

## Technical notes

- WO Countdown is read-only: it never starts, stops or changes anything in WATCHOUT
- Cue times are read from the saved show file, not from the live session — save the show after moving a container cue
- When two countdowns are active at the same time, the one started last is shown
- Web page on port 8088 by default
- Configuration and log are stored in `%APPDATA%\StageTools\WOCountdown\`

## Version

See the Releases tab for the full version history.

---

Made by Riccardo Nessi — [Stage Tools](https://stage-tools.github.io/stagetools/)

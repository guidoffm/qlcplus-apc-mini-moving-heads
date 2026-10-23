# QLC+ Moving Head Demo for the AKAI APC mini mk2

A demo workspace for [QLC+ 5](https://www.qlcplus.org/) that drives **32 moving heads** on four trusses (8 heads per truss). The show is shown in the QLC+ 3D view, so no real lights are needed.

You can run everything from the QLC+ virtual console or from an **AKAI APC mini mk2** connected via USB. The console page has the same layout as the controller, and the controller's RGB pads show the current state.

In the demo video, a software emulator of the APC mini mk2 stands in for the hardware controller.

The project was partially created with the help of AI, including the background music of the video.

## Requirements

- QLC+ 5 (tested with 5.3.0)
- Optional: AKAI APC mini mk2 (the first-generation APC mini has no RGB pads, so its feedback colors won't match)

The workspace only uses resources that ship with QLC+:

- Fixture: beamZ *MHL-74 Wash 7x10W 4in1 RGBW* (12-channel mode)
- Input profile: *Akai APC Mini mk2*

## Getting started

1. Open `moving-heads-apc-mini.qxw` in QLC+. The workspace starts in the virtual console.
2. To see the stage, go to **Fixtures & Functions** and click **3D View**. A left click opens the view inside the main window, and a right click opens it in a separate window. The separate window lets you watch the stage and the virtual console side by side.
3. Optional: connect the APC mini mk2. Under **Inputs/Outputs**, select it as input and as feedback output for universe 1, using the profile *Akai APC Mini mk2*. The workspace was saved with a device called "Virtual APC Mini", so you'll need to change this setting.
4. Under **Inputs/Outputs**, set the DMX output to your own interface. If you only want to use the 3D view, you don't need a DMX output.

Command line start (macOS):

    /Applications/QLC+.app/Contents/MacOS/qlcplus5 -o moving-heads-apc-mini.qxw

## Controller layout

The pads are counted from top to bottom, as on the device:

| Pad row | MIDI notes | Function |
|---|---|---|
| 1 | 56–63 | Colors: Red, Green, Blue, Cyan, Magenta, Yellow, Amber, **Strobe** |
| 2 | 48–55 | Colors: Lime, Orange, White, Purple, White LED, Pink |
| 3 | 40–43 | Positions: Center, Edge, Cross, Audience |
| 4–6 | 16–39 | Light effects (chase, ping-pong, police, rainbow, plasma, fire, radar, meteor, waves, aurora, thunderstorm, …) |
| 7 | 8–15 | Movement: Circle, Circle Wave, Figure 8, Pan Sweep, Tilt Wave, Lissajous, Diamond, Leaf |
| 8 | 0–5 | Auto shows that switch every 4, 8, 16, 32, 64 or 128 s |
| Right column | 112–119 | Scene buttons, the last one is **Blackout** |
| Faders | CC 48–56 | Intensity and color mix (Red, Green, Blue, White) |

Each group is a solo frame, so pressing a pad replaces the active program of that group. Groups combine with each other: you can run a color, a position, an effect and a movement at the same time.

The movement effects are relative, so they move around whichever position is active.

## Files

| File | Description |
|---|---|
| `moving-heads-apc-mini.qxw` | The QLC+ workspace |
| `LICENSE` | MIT License |

## License

Released under the [MIT License](LICENSE).

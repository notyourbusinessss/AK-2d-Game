# Summit Trail — Ak hiking game

A small 2D, retro/pixel-style climbing game written in **Ak**. The mountain never ends: climb ledge to ledge, manage stamina, rest when needed, and see how high you can get. Your height and best height are shown in the HUD.

![Start](docs/start.png)
![Climbing](docs/climbing.png)

## Requirements

- Linux with an X11 display or XWayland
- The [Ak language repository](https://github.com/notyourbusinessss/AI-codinglanguage-), including its `lib/x11.aklang` and `lib/canvas.aklang` files

The target game repository is separate from the language repository, so the X11 graphics library is not bundled here. Clone both repositories side by side, or adjust the `use` path at the top of `game.aklang`.

Example layout:

```text
projects/
  AI-codinglanguage-/
    lib/x11.aklang
    lib/canvas.aklang
  AK-2d-Game/
    game.aklang
```

With that layout, from `AK-2d-Game/` run:

```sh
ak game.aklang
```

If `ak` isn't on your PATH, follow the setup instructions in the Ak language repository first.

## Controls

- **Arrow keys** or **WASD** — move
- **Space** — rest and recover stamina
- **R** — restart
- **Q** or **Esc** — quit

## Notes

Ledges are generated as you climb, and neighbouring ledges always overlap, so there is always a way up. This is a compact starter game, intended to be easy to extend. The graphics use Ak's native X11 canvas API, not a browser or JavaScript game engine.

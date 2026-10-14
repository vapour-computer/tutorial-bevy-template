# Vapour tutorial branch

This branch of [bevy_game_template](https://github.com/NiklasEi/bevy_game_template) is the sample project for the
**Bevy tutorial** in the [Vapour handbook](https://vapour-computer.github.io/vapour-dev-docs/). What was added on top of upstream:

| File | What it is |
| --- | --- |
| `vapour.toml` | Game manifest, a custom Trunk build (`build.command = "custom"`) and a one-stick phone `[controller]` |
| `.github/workflows/vapour.yml` | Builds the web bundle on every push; publishes to Vapour on `v*` tags |

Output goes to `dist/`, not `build/web/`: upstream keeps source files in `build/web/` and Trunk empties its output folder.
Upstream's license (CC0-1.0) is unchanged.

```sh
vapour build        # runs the custom Trunk command, then checks dist/index.html
vapour test         # run it locally with the FPS overlay and profiler
```

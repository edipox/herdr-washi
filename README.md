# Paper Kanso

A light theme for the [Herdr](https://herdr.dev) desktop app. The sidebar, tab bar and status bar use Herdr's built-in `paper` colors. The terminals and their pane headers use the warm cream and muted colors from [Kanso Day](https://github.com/jlopezlira/herdr-kanso), which is easier on the eyes than paper's white.

![Paper Kanso](preview.svg)

## Install

```sh
curl -fsSL https://raw.githubusercontent.com/edipox/herdr-paper-kanso/main/themes/paper-kanso.json \
  -o ~/.config/herdr-app/themes/paper-kanso.json
```

Then pick `paper-kanso` in Settings, or run `herdr-app do app.theme --name paper-kanso`. To follow the system appearance, set `"theme": {"light": "paper-kanso", "dark": "graphite"}` in `~/.config/herdr-app/settings.json`.

## How it's built

The top-level `background`, `foreground`, `selection`, `cursor` and `ansi` values are Kanso Day's, so the terminals get them. Herdr would derive the panel colors from those too, so `colors` pins each one back to paper's value. `background` is the one color left unpinned, because the pane frame and the pane header both draw with it.

## Credits

Terminal palette from [jlopezlira/herdr-kanso](https://github.com/jlopezlira/herdr-kanso) (Apache-2.0). Panel palette from Herdr's built-in `paper` theme.

## License

MIT

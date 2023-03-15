# wttr.in client

This is a simple Bash client for [wttr.in](https://wttr.in) - a phenomenal weather service that
produces terminal-friendly output:
![Current weather in London](https://wttr.in/London)

This tiny client is a convenient replacement for `curl` calls, i.e.:

| Operation | With curl | With wttr client |
| ---- | ---- | ----- |
| Weather for current location | `curl wttr.in` | `wttr` |
| Weather for London | `curl wttr.in/London` | `wttr London` |
| Get weather as JSON and color it with bat | `curl wttr.in/London?format=j1 | bat -j json` | wttr
-o json London` |

## Features

- Support for XDG config file with preferences (locations, units, formats, etc)
- Automatic detection of `$TERM` to support graphic output
- Human-readable params
- JSON output coloring (with [bat](https://github.com/sharkdp/bat), if present)

## Syntax

```bash
wttr [options] [location]
```

- `location`: Name of a city/town. When omitted wttr will try to determine current location based on
  IP. Multiple values allowed if provided as comma-separated list
- `options`:
    - `--output`: output format. Allowed values: `txt`, `png`, `json`, `auto` (default). `auto`
      works like `png` if terminal allows (i.e. Kitty with imagemagick), `txt` otherwise.

## Credits

Many thanks to [Igor Chubin](https://github.com/chubin) for creating the great [wttr.in](https://github.com/chubin/wttr.in)!



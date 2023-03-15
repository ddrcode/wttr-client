# wttr.in client

This is a simple Bash client to [wttr.in](https://wttr.in) service.
It is a convenient replacement for `curl` calls

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

Many thanks to [Igor Chubin](https://github.com/chubin) for creating great [wttr.in](https://github.com/chubin/wttr.in)!



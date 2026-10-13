# Switch Control Card

A responsive, theme-aware Home Assistant Lovelace card for one configurable `switch` entity.

## Features

- Shows the switch's actual `on`, `off`, or unavailable state
- Sends `switch.turn_on` or `switch.turn_off` based on the last reported entity state
- Optional title and icon overrides
- `aurora`, `ocean`, `sunset`, and `lavender` accent palettes
- Responsive layout and long-press More Info
- HACS compatible; no external runtime dependencies

## Install with HACS

1. In HACS, open **Frontend** → **Custom repositories**.
2. Add `Liionboy/lovelace-switch-control-card` with category **Lovelace**.
3. Install **Switch Control Card**.
4. Add the card to a dashboard:

```yaml
type: custom:switch-control-card
entity: switch.your_switch
title: Device
icon: mdi:power
palette: aurora
```

## Configuration

| Option | Required | Description |
| --- | --- | --- |
| `entity` | Yes | A Home Assistant `switch` entity |
| `title` | No | Display name; defaults to the entity's friendly name |
| `icon` | No | Optional Material Design Icon override |
| `palette` | No | `aurora`, `ocean`, `sunset`, or `lavender` (default: `aurora`) |

Switches are stateful entities, so the card reflects the entity's reported state; it does not infer an on/off state from an action timestamp.

## License

MIT

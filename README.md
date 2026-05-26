# FFXIJSE

Job Specific Equipment tracker with a GSUI-style window.

A fork of [Nalfey's JSE](https://github.com/Daleterrence/JSE) — same core
data modules (`inventory.lua`, `currency.lua`, `job_equipment.lua`,
`jobs/`), new main file with a draggable UI instead of chat-only output.

## Install

```
cd path\to\Windower4\addons
git clone https://github.com/mullerdane85-hash/FFXIJSE.git
```

In-game:

```
//lua load FFXIJSE
```

To autoload every session, add `lua load FFXIJSE` to
`scripts\init.txt`.

## Window

Press **J** to toggle the window (chat-aware — the key passes through
to chat when typing). Or run `//fj` (or `//ffxijse`).

Layout (matches GSUI's visual style — blue border, dark title bar,
tab buttons inside the title bar):

```
┌─ 3px blue border ────────────────────────────────────────────┐
│ FFXIJSE       [AF][Relic][Empy]                      [WAR]   │
├──────────────────────────────────────────────────────────────┤
│  Pummeler's Mask              ✗ NEED  +2 → +3                │
│     P. WAR Card           0/12    ✗                          │
│     Kin's Scale           4/1     ✓                          │
│     Khoma Cloth           0/1     ✗                          │
│  Pummeler's Lorica            ✓ MAXED (+4)                   │
│  Pummeler's Mufflers          ✓ MAXED (+4)                   │
│  ...                                                          │
└──────────────────────────────────────────────────────────────┘
```

Per-piece status indicator:
- `✓ MAXED (+4)` — piece is at maximum tier
- `✓ READY +2 → +3` — you have ALL materials to do the next upgrade
- `✗ NEED +2 → +3` — you own the piece but lack some materials
- `? owns NONE → +1` — you don't own the piece at all

Below each non-maxed piece, the required materials list:
- `✓` = you have enough
- `✗` = you need more

## Commands

| Command | What |
|---|---|
| `//fj` (or `//ffxijse`) | Toggle the window (same as J key) |
| `//fj show` / `//fj hide` | Explicit show/hide |
| `//fj af` / `//fj relic` / `//fj empy` | Switch tab |
| `//fj job <JOB>` | Override displayed job (e.g. `//fj job war`) |
| `//fj job auto` | Clear override; track current main job |
| `//fj refresh` | Re-scan inventory + currency |
| `//fj help` | Command list |

By default the window auto-detects your current main job and updates
on job change / zone change. The `J` key toggles visibility.

## Data behavior

Same as the original JSE:
- Reads inventory across **all storage slips** (Storage NPCs, Mog
  Wardrobes, etc.) via the Slips library
- Tracks Rem's Tale Chapters, Apollyon Units, Temenos Units, and
  Gallimaufry via currency packets
- Per-character data file written under `data/` (gitignored)
- Cross-character mule check is NOT yet ported from JSE's `//jseall`
  command — TODO

## Credits

- **Nalfey of Asura** — original JSE addon (data modules, scanning,
  job equipment database). All credit for the actual upgrade-data
  research and packet handling goes to Nalfey.
- **Daleterrence** — hosts JSE at github.com/Daleterrence/JSE with
  Nalfey's permission. FFXIJSE is derived from that mirror.
- **mullerdane85-hash** — GSUI-style window UI rewrite.

BSD 3-clause license inherited from JSE — see `LICENSE`.

## TODO / future extensions

- `//ffxijse all` cross-character / mule check (port from JSE's
  `//jseall`)
- Auto-refresh when the player approaches a known ??? NPC for
  upgrade turn-ins (Voliathon's request — proximity-based refresh)
- Job picker dropdown in the title bar (currently job override is
  command-only)
- Per-tier filter (e.g. show only pieces stuck at +2)

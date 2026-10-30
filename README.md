# Skunkgarage

A catalog of hardware we can build with or build from. It covers machines that make parts, tools that debug boards, and reference designs worth copying.

Each entry is a single YAML file in [`designs/`](designs/). The catalog holds open and closed hardware alike: every entry records **how open** the design is, so you can see before you start whether you can modify it, manufacture it or only buy it.

## Index

| Design | Category | Openness | License | Skill |
|---|---|---|---|---|
| [Voron 2.4](designs/voron-2-4.yaml) | 3D printer | open-source | GPL-3.0 | advanced |
| [Original Prusa i3 MK3S](designs/prusa-i3-mk3s.yaml) | 3D printer | open-source | GPL-2.0 | intermediate |
| [LumenPnP](designs/lumenpnp.yaml) | Pick-and-place | open-source | CERN-OHL-W-2.0 (hardware) | advanced |
| [Glasgow Interface Explorer](designs/glasgow-interface-explorer.yaml) | Interface tool | open-source | 0BSD OR Apache-2.0 | intermediate |
| [Bus Pirate 5](designs/bus-pirate-5.yaml) | Interface tool | open-source | MIT | beginner |
| [ThunderScope](designs/thunderscope.yaml) | Oscilloscope | open-source | CERN-OHL-P-2.0 (hardware) | advanced |
| [OpenFlexure Microscope](designs/openflexure-microscope.yaml) | Microscope | open-source | CERN-OHL-S-2.0 | intermediate |
| [Adafruit Feather RP2040](designs/adafruit-feather-rp2040.yaml) | Microcontroller board | open-source | CC-BY-SA | beginner |
| [Arduino Uno Rev3](designs/arduino-uno-rev3.yaml) | Microcontroller board | open-source | CC-BY-SA-4.0 | beginner |
| [Libre Solar MPPT 2420 HC](designs/libre-solar-mppt-2420-hc.yaml) | Power | open-source | CERN-OHL-W-2.0 | advanced |

## Entry format

One file per design, `designs/<slug>.yaml`:

| Field | Meaning |
|---|---|
| `name` | Product or project name as the maker writes it. |
| `category` | `<area>/<kind>`. The areas are `fabrication`, `test-and-debug` and `electronics`. |
| `openness` | `open-source`: design files are published under a license that allows modifying and making it. `source-available`: files are published but the license restricts use, e.g. non-commercial (NC) terms. `closed`: no design files; buy only. |
| `license` | Map of part to license. Use SPDX IDs where one exists. Split by part when the maker does (hardware, software, branding). Closed entries use `proprietary`. |
| `maker` | Who designs and maintains it. |
| `source` | Where the design files live. For closed entries, the product page. |
| `docs` | Build or user documentation. |
| `get_it` | How to obtain one: kit, assembled, or build from files. |
| `formats` | CAD and EDA formats of the files. |
| `summary` | What it is, in two or three sentences. |
| `use_it_for` | Why it is in this catalog. |
| `skill_level` | `beginner`, `intermediate` or `advanced`. |
| `verified` | When the license and source were last checked against upstream, and what was checked. |
| `notes` | Caveats: trademarks, beta status, upstream warnings. |

## Adding an entry

1. Copy an existing YAML file and fill in every field.
2. Read the license from the upstream source itself (the LICENSE file, or the license page in the design zip), not from a store page or a summary. Record what you checked under `verified`.
3. Add a row to the index above.

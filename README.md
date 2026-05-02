# Retro Handheld Mod

A personal project to repurpose a Tectoy handheld console
into a functional Raspberry Pi-based emulation device.

## Motivation

Built as an anniversary gift for my girlfriend — combining a sentimental object
with real embedded systems engineering. The goal was to create something
meaningful that could also serve as a functional device.

## Goals

- Reuse original casing and buttons
- Integrate Raspberry Pi Zero 2W
- Run Linux-based emulation software
- Document the full process as a learning experience

## Hardware (original)

- Console: Tectoy Mega Drive Portátil
- PCB: GP2628 V5.1 20000329
- SoC: Sengoku KIZUNA Series (Maruho) — proprietary, not reusable

## Internal Dimensions

| Measurement | Value |
|-------------|-------|
| Length | ~140mm |
| Width | ~50mm |
| Depth | ~15mm |

## Components

### Reused
- Casing (front and back shells)
- D-pad and action buttons (UP, DOWN, LEFT, RIGHT, MENU, X, Y, Z, 1-A, 1-B, 1-C, PLAY)
- Volume wheel (potentiometer/encoder)
- Reset switch
- Speaker

### Replaced
- PCB (original discarded)
- Display (original proprietary flat cable, incompatible)
- Battery (original NP60-2 3.7V 750mAh, insufficient capacity)

## New Components (planned)

- Raspberry Pi Zero 2W
- Display 3.5" SPI (ILI9341 or ST7789)
- LiPo battery + TP4056 charging module
- MicroSD 16GB+
- PAM8403 mini amplifier

## Status

- [x] Disassembly and hardware inspection
- [ ] Component sourcing
- [ ] GPIO mapping
- [ ] Display integration
- [ ] Software setup
- [ ] Final assembly

## Build Log

### Day 1 — Disassembly and inspection

Disassembled the console completely. The original PCB runs a proprietary
Maruho SoC and is not reusable. All button contacts are labeled directly
on the PCB, which simplifies mapping.

The casing has enough internal space to fit the Pi Zero 2W, a flat LiPo
battery, and wiring without structural modification.

**PCB overview:**
![PCB back](docs/images/PCBback.png)
![PCB front](docs/images/PCBfront.png)

**Button contacts (directional):**
![Directional buttons](docs/images/BUTTONSdir.png)

**Button contacts (action):**
![Action buttons](docs/images/BUTTONSac.png)

**Casing — all parts:**
![Casing disassembled](docs/images/CASEall.png)

**Internal dimensions:**
![Case depth](docs/images/CASEprof.png)

Components confirmed for reuse: casing, all buttons, volume wheel,
reset switch, and speaker.

Next step: source components and map GPIO pins.

# Assembly Notes

## Build progression

Казкар moved through three visible stages:

1. **Breadboard prototype** — proving SD-card playback, button handling, and speaker output
2. **Temporary plastic-box build** — early physical integration and control placement
3. **Laser-cut MDF enclosure** — final documented build with a more coherent front-panel design

## Stage 1 — Breadboard proof of concept

The first stage established the system architecture:

- Arduino Uno controller
- microSD card playback over SPI
- three-button interface
- direct speaker output

At this stage the goal was simply to prove that the core interaction worked.

## Stage 2 — Temporary integrated build

The intermediate build placed the electronics in a rough clear plastic housing. This was useful because it forced early decisions about:

- cable routing
- button placement
- how the device would be handled physically
- whether the front controls were understandable

## Stage 3 — Final enclosure version

The final version in this repository brings the project into a stronger portfolio state:

- custom front and back panels
- mounted speaker
- color-coded buttons
- LightBurn-designed enclosure
- portable power by USB power bank

## What I would preserve in a next revision

Even if the electronics were redesigned later, I would preserve:

- the three-button interaction model
- no screen
- direct speaker playback
- removable media workflow
- a design centered on a single child-friendly task

## What I would improve in a next revision

A second-generation build would likely focus on:

- cleaner internal mounting
- more robust wire management
- perfboard or PCB transition
- a cleaner power integration strategy
- stronger serviceability and assembly discipline
- inclusion of volume control

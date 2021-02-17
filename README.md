# Control Specification Explorations
A place to discuss a potential custom new audio control format for use with the RustyDAW project.

# Objective
Why create a new audio control standard?

The MIDI standard is old and doesn't support all the features we want.

The MIDI2 standard is more promising, but there are several issues we take with it:
* The spec is huge and complicated.
* We would have to rely on a third party organization to include any potential features in the future.
* It heavily prioritizes being fully backwards compatible with MIDI. We have some doubts on how acheivable this actually is.
* MIDI2 wants to take control of aspects we believe should be left to the plugin spec instead, such as plugin parameters.
* MIDI2 is new and has little adoption. We have no idea if it will even be successful in the long run.

As a community of passionate developers and artists, we believe we are equipped to create a new standard from the ground-up to support the needs of modern developers and artists, as well as leaving room for robust futureproofness. This document aims to spark discussions on what features should be implemented in the final spec, and how to best futureproof this spec.

# Key Features

* The ability to convert to and from standard MIDI. It doesn't need full backwards compatibility (in fact, we think that would be a hinderance), but enough to support the majority of DAWs and plugins on the market.
* Fully open-source and community driven.
* This standard should not deal with plugin parameters at all. This should be left to the plugin api.
* No CCs for automation controls. Instead, we will use "automation nodes" that behave like audio inputs/outputs but for automation data.
* The ability to create as many input/output automation nodes as desired at runtime, with the ability to connect these nodes in any way.
* Accurate timing controls from the host, such as beats, bpm, and swing.
* Per-note modulation (i.e velocity, pan).
* Micro-pitch expressions with automatable pitch curves per-note.
* Automatable velocity and pan curves per-note.
* Support for non-12 EDO scales.
* Sample-accurate automation.
* The ability for the host to properly voice each note, removing this burden from the plugin developer.

# Specification

This checklist is currently incomplete. Please open a PR with your additions/removals!

TODO

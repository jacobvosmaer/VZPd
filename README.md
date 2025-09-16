# Pure Data emulation of Casio VZ-1 synthesis

This is an (incomplete) emulation of the Casio VZ-1 synthesis engine in [Pure Data](https://puredata.info/). The goal of this project is not to recreate the entire synth, but to better understand what it is capable of.

There is a [demonstration video on Youtube](https://www.youtube.com/watch?v=fxs7wTaExAc).

Also see [my blog](https://blog.jacobvosmaer.nl/tags/vz-1.html).

## Currently implemented

- `[vzphasor~]` phasor (works the same as regular Pd `[phasor~]`).
- `[vol~]` volume/mute abstraction. Use minimum volume 5 to simulate VZ "always on" behavior.
- `[vzshaper~]` VZ wave shaper. Takes creation argument or right inlet integer 0-5 where 0 means sine, 1 means saw1, ..., 5 means saw5.

This is enough to simulate MIX and PHASE modes, including "external phase".

## Would like to add

I would like to add RING mode because I think it's an important tool to get more different sounds out of the wave shaping.

## Probably won't bother

I don't think I'll implement noise mode or envelopes. But who knows.

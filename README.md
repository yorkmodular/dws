## DWS - The Diodular Wave Strangler

Proof, if any were needed, that you don't always need a ton of components to make a boring old sine (or triangle, or sawtooth - square waves don't work too well) wave much more interesting. We're going to achieve this with the aid of an op-amp and a bunch of passives (diodes and resistors, mainly)

Here you'll find:

- The Bill of Materials (BOM) - these are the bits you'll need to complete the module.
- The schematic
- Design files for the front panel, should you be seized with a desire to roll your own.

### In use

Twiddle the knobs.

Seriously.

The effectiveness of each of the diode stage pots seems to depend a lot on the settings of the SCALE and SLOPE pots - in some cases, you'll find that only the first four stages have any real effect, whereas in others the later stages will have quite a profound effect instead. Experimentation is the key.

I find that the best results can be obtained from sine and triangle waves, whereas the effects on square waves are minimal at best. The effects on a sawtooth are somewhere in between - in any event, a bit of post-filtering can work wonders for the sound.

A good starting point would be to have the SCALE pot fully counter-clockwise and the SLOPE pot at around 10 o'clock - when adjusting the levels in the diode stages, try and avoid consecutive 'extreme' values.

### Build notes

The build is pretty straightforward - there are no surface-mount or wilfully strange parts, unless you count Schottky diodes.

* R20 can either be a 1k resistor _or_ a 100nF film capacitor. The latter will remove any DC offset in the folded signal - this is what I recommend (ceramic capacitors will work, but I prefer to use film caps for DC offset removal purposes)

* I strongly recommend using Schottky (or germanium) diodes for both the diode stages (D1-D8) and the soft-clipping section (D10, D11) - ideally, the voltage drop for these diodes should be no more than 0.3V - for pre-built modules I use Vishay SD101C-TR diodes, but any small-signal Schottky will do. It's OK to use 1N4148s for the power supply diodes (D13, D14)

* In terms of pots, RV1 to RV8 should be 100k audio taper - linear taper will work fine, but I found that the log taper pots gave me more control. SCALE1 and SLOPE1 pots should be 100k linear, whilst the OUTPUT_GAIN pot should be 100k audio.

* Reduce the value of R19 if you want more gain.

* The op-amp doesn't need to be anything particularly exotic - I generally use TL084s on pre-builts. TL074 will work just as well.

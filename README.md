# br.max

## Max/MSP abstractions and Ableton Max for Live devices by Brian Riordan
   
By Brian Riordan  
[guaguanco127@gmail.com](mailto:guaguanco127@gmail.com)  
[brianriordanmusic@gmail.com](mailto:brianriordanmusic@gmail.com)   
[https://www.brianriordanmusic.com/](https://www.brianriordanmusic.com/)  
[https://github.com/guaguanco127/](https://github.com/guaguanco127/) 

This repository is a project started by Brian Riordan in 2023. Users with access to either Max/MSP or Ableton Live Suite will be able to use customized patches, abstractions, externals, or Max for Live devices. Users with access to RNBO can build their own VST or AU audio plugins for free to use with their own DAW.    

The purpose of this project is primarily educational. However, some basic patches or VSTs here are designed with "DAW agnosticism" in mind. If you have access to fundamental mixing plugins, then it doesn't matter which DAW you use.

The naming system (br.xxxx.xx.1.0) is because all of these are prototypes. A more "proper" name will occur when these reach a certain level of quality regarding their stability and GUI. When that happens, the effect may move to a Gumroad account. 

Please contact me at the emails provided above if you have any questions, notice any errors, or have any requests. 


## Links to Max/MSP Patches, Abstractions, Externals, RNBO, VSTs, and Ableton Max for Live:

[Basic Utility Effects](#utility) 

[Mixing/Routing](#mixing)

[Delay Effects](#delay)

[Glitch/Granular Effects](#grain)

[Spectral Effects](#spectral) 

[Oscillators](#oscillators)

[Modulation Tools](#modulation)

[Filters](#filters)

[Dynamics](#dynamics)

[Waveshapers](#shapers)

[Distortion](#distortion)

[Future Effects/Instruments](#future) 

## <a name="utility"></a>Basic Utility Effects

These effects are modeled after the Ableton Utility audio effect. Inspect the patchers to see how they are built. The benefit of having access to these effects as a VST is that they can be used in any DAW, and you can decide on the placement and order of these effects. Additionally, these can be used as externals or abstractions in Max/MSP.  

Many of these effects have a RNBO patch included that allow the user to export as either a Max/MSP external, or a VST. 

[br.utility.gain](https://github.com/guaguanco127/br.utility.gain)  A click-free gain in dB (-72 = silence, 0 = unchanged, up to +35), mono or stereo, with or without a Gain dial, with a State outlet on the UI versions that reports the gain by name. Version 2.2.

[br.utility.mute](https://github.com/guaguanco127/br.utility.mute)  A click-free mute (10 ms S-curve fade), mono or stereo, with or without a Mute button, with a State outlet on the UI versions that reports the mute by name. Version 2.2.

[br.utility.mono](https://github.com/guaguanco127/br.utility.mono)  Click-free stereo to mono, with four mix settings for how L + R are combined (0 / -3 / -4.5 / -6 dB: one side, stereo, full mix, dual mono), with or without controls, with a State outlet on the UI version that reports both settings by name. Version 2.2.

[br.utility.monobass](https://github.com/guaguanco127/br.utility.monobass)  Click-free bass to mono: sums the lows below an adjustable crossover to mono and leaves the highs in stereo, with four mix settings (0 / -3 / -4.5 / -6 dB) and no comb filtering when switching, with or without controls, with a State outlet on the UI version that reports every setting by name. Version 2.2.
 
[br.utility.stereo](https://github.com/guaguanco127/br.utility.stereo)  Stereo modes (swap, left, right, mid, side), mid/side width from mono to extra wide, and pan as a Balance (like Ableton Utility) or Dual panner, all click-free, with a State outlet on the UI version that reports every setting by name. Version 2.2.

[br.utility.stereomix](https://github.com/guaguanco127/br.utility.stereomix)  A per-channel mixer for fixing one side of a stereo pair: polarity invert, gain and constant-power pan for each channel, all click-free, with a State outlet on the UI version that reports every setting by name. Version 2.2.

[br.feedback](https://github.com/guaguanco127/br.feedback) Max/MSP abstractions that let a signal feed back into itself: a tapin~/tapout~ pair adds the one-vector delay MSP needs to run a loop. Mono and stereo versions, with an FM feedback example.

## <a name="mixing"></a>Mixing/Routing

[br.xfade](https://github.com/guaguanco127/br.xfade) Max/MSP abstraction: a click-free A/B crossfader. One Position control for dry/wet mixing or switching sources, an adjustable fade time, and Equal Power or Linear law. Stereo and mono, with an RNBO host and a State outlet on the UI versions that reports every setting by name. Version 1.2.

[br.aux](https://github.com/guaguanco127/br.aux) Max/MSP abstraction: a minimal aux send for parallel effects. Outputs a click-free copy of the signal at a Level in dB, for an effect you add back to the dry signal. Stereo and mono, with an RNBO host and a State outlet on the UI versions that reports the level by name. Version 1.2.

## <a name="delay"></a>Delay Effects   

[br.delay.digital](https://github.com/guaguanco127/br.delay.digital) A clean stereo digital delay: time changes crossfade to the new time instead of bending the pitch (Xfade from a quick cut to a 5 s blur), Linked / Stereo / Ping-Pong modes, straight or cross feedback up to a never-fading 1, tone filters on the echoes, Hold to freeze the loop, and On/Off. Click-free, including mode switches. Max/MSP, RNBO and Max for Live, with a State outlet on the UI version that reports every setting by name. Version 1.1.

[br.delay.pitch.a](https://github.com/guaguanco127/br.delay.pitch.a) A stereo delay with a pitch-shifter inside the delay line, so every repeat is shifted again. Protected feedback loop (soft saturation, Highpass/Lowpass) that can hold or build, low CPU at rest.

[br.delay.pitch.b](https://github.com/guaguanco127/br.delay.pitch.b) Version b of br.delay.pitch: the same pitch-shifting delay plus just-intonation pitch steps (overtone scale) with fine-tune cents, and randomizing of pitch, delay time and feedback -- by button, automatically, or on every attack you play.

[br.delay.swarm](https://github.com/guaguanco127/br.delay.swarm) (formerly br.spacedelay) A stereo multi-voice delay: up to 12 voices keep skipping to random delay times (crossfaded, click-free), each with its own randomly moving filter, amplitude and panning, plus a freeze that loops only the last moments of the delay.

[br.delay.tape](https://github.com/guaguanco127/br.delay.tape) A stereo tape-style delay: time changes bend the pitch like tape, Linked / Stereo / Ping-Pong modes, straight or cross feedback that can build into a dub runaway, tone filters on the echoes, drive, wow and flutter, and On/Off. Click-free, including mode switches. Max/MSP, RNBO and Max for Live, with a State outlet on the UI version that reports every setting by name. Version 1.2.

## <a name="grain"></a>Glitch/Granular Effects

[br.munge](https://github.com/guaguanco127/br.munge) A real-time granulator and an emulation of the munger~ external object from Max/MSP. Additional features, such as the processing of a stereo signal, additional amplitude and stereo envelopes, ping-pong feedback, and a freeze that keeps the grains playing from only the last moments of the input, are included.

[br.stutter.a](https://github.com/guaguanco127/br.stutter.a) An abstraction/device that is built around the Max/MSP stutter~ object. A real-time granular glitch effect that is a signal capture buffer. 

[br.stutter.b](https://github.com/guaguanco127/br.stutter.b) An abstraction/device that is built around the Max/MSP stutter~ object. This contains all features as br.stutter.a but with extras. This effect adds LFOs in sync with each grain that can manipulate a filter, amplitude, and panning. 

[br.stutter.c](https://github.com/guaguanco127/br.stutter.c) An abstraction/device that is built around the Max/MSP stutter~ object. This contains all features as br.stutter.b but with extras. This effect includes an auto re-triggering feature, auto-detection, adjustment of the phase (starting position) of the grains, and a refresher that restarts the grain when it reaches a certain position within the phase.




## <a name="spectral"></a>Spectral Effects

[br.freeze](https://github.com/guaguanco127/br.freeze) A spectral freeze Max/MSP object and Max for Live Device. It can also freeze automatically on every attack you play, and a Feedback control layers each new freeze onto the one you are hearing.  

[br.freezex](https://github.com/guaguanco127/br.freezex) A spectral freeze object/device similar to br.freeze, except this allows for crossfading into the next freeze by as much as 10 seconds. It can also freeze automatically on every attack you play, and a Feedback control layers each new freeze onto the one you are hearing.

[br.freeze.partials](https://github.com/guaguanco127/br.freeze.partials) A spectral-style freeze Max/MSP object and Max for Live Device: tracks the partials of live stereo input and holds them as a bank of 16 sine voices per side with Buchla-style folding and per-partial levels. Crossfades between freezes, can freeze on every attack, and includes sigmund~ (Mac + Windows).

[br.pitchshift](https://github.com/guaguanco127/br.pitchshift) A pitchshifting device/object with slight latency and no artifacts. Preferred for harmonization.

[br.whammy.1.0](https://github.com/guaguanco127/br.whammy.1.0) A pitch-shifting device/object with no latency and some artifacts. 

## <a name="oscillators"></a>Oscillators

[br.osc](https://github.com/guaguanco127/br.osc) An anti-aliasing Max/MSP oscillator with 8 morphing shapes, skew and hard sync: clean at audio rate, and just as good as an LFO.

## <a name="modulation"></a>Modulation Tools

[br.scale](https://github.com/guaguanco127/br.scale) Max/MSP abstractions that turn an LFO, oscillator or function generator (bipolar or unipolar) into volume or frequency on curves that sound even to the ear: equal-loudness gain, and octave-even pitch or filter sweeps. Each comes as a plain object whose controls take signals and a version with dials and a State outlet that reports every setting by name. The example lets you hear the curves against a plain linear scaling. Includes RNBO patches for building an external or plugin. Version 1.2.

[br.am](https://github.com/guaguanco127/br.am) Max/MSP abstraction for click-free stereo tremolo that morphs into ring modulation, from LFO to audio rate. Comes as a plain object whose controls take signals (an LFO on Ring morphs AM into ring mod) and a version with dials and a State outlet that reports every setting by name. Includes an RNBO patch for building an external or plugin. Version 1.1.

[br.function](https://github.com/guaguanco127/br.function) Max/MSP abstraction: a mono rise/fall function generator in gen~, in the spirit of a Make Noise Maths channel. Envelope, slew/portamento and cycling LFO in one, with curved Rise and Fall, click-free retrigger, and end-of-rise/end-of-cycle pulses for chaining. Comes as a plain object whose controls take signals and a version with dials and a State outlet that reports every setting by name. Includes an RNBO patch for building an external or plugin. Version 1.1.

## <a name="filters"></a>Filters

[br.filter](https://github.com/guaguanco127/br.filter) Max/MSP abstractions: a family of stereo biquad filters in gen~ with click-free controls. Lowpass, highpass, bandpass, notch, allpass, peak and shelves, plus an all-in-one biquad and level-matched versions. Each comes as a plain object whose controls take signals (sweep it with an LFO) and a version with dials and a State outlet that reports every setting by name. Includes RNBO patches for building externals or plugins. Version 1.1.

[br.eq3](https://github.com/guaguanco127/br.eq3) Max/MSP abstraction: a stereo 3-band EQ in gen~ that sums back exactly flat at 0 dB. Two movable crossovers, ±24 dB per band, a mute for each band, all click-free. Comes as a plain object whose controls take signals and a version with controls and a State outlet that reports every setting by name. Includes an RNBO patch for building an external or plugin. Version 1.2.

## <a name="dynamics"></a>Dynamics

[br.comp](https://github.com/guaguanco127/br.comp) Max/MSP abstraction: a linked stereo compressor in gen~ whose controls mean what their units say. Soft knee, peak/RMS detection, dry/wet, sidechain and a gain reduction output, all click-free. Comes as a plain object whose controls take signals and a version with dials and a State outlet that reports every setting by name. Includes an RNBO patch for building an external or plugin. Version 1.2.

[br.limit](https://github.com/guaguanco127/br.limit) Max/MSP abstraction: a safety brickwall limiter in gen~. The output never goes above the Ceiling, however hard Drive pushes it. Lookahead is optional: 0 ms means no latency. True Peak option. Stereo and mono, with an RNBO host and a State outlet on the UI versions that reports every setting by name. Version 1.2.

## <a name="shapers"></a>Waveshapers

[br.shaper](https://github.com/guaguanco127/br.shaper) Max/MSP abstractions: a family of mono waveshapers in gen~ for synthesis, antialiased and click-free. Wavefolder, wrapper, hard clipper and Buchla-style sine folder, plus an all-in-one with click-free mode switching. Works on audio and LFOs. Each comes as a plain object whose controls take signals and a version with dials and a State outlet that reports every setting by name. Includes RNBO patches for building an external or plugin. Version 1.1.

[br.tanh](https://github.com/guaguanco127/br.tanh) Max/MSP abstraction: a mono and stereo tanh saturator in gen~ for synthesis, normalized, antialiased and click-free. Drive sweeps from clean to near-square at the same peak level, with a Mix for parallel saturation. Works on audio and LFOs. Comes as a plain object whose controls take signals and a version with dials and a State outlet that reports every setting by name. Includes RNBO patches for building an external or plugin. Version 1.1.

## <a name="distortion"></a>Distortion

[br.crush](https://github.com/guaguanco127/br.crush) A stereo bit-crusher and sample-rate reducer: float Bits that morph smoothly between depths, Auto-gain so lowering Bits never jumps in level, a curved Rate dial with most of its travel in the low rates, a post low-pass, Dry/Wet and On/Off. Click-free, with a State outlet on the UI version that reports every setting by name. Max/MSP, RNBO and Max for Live. Version 1.2.

[br.overdrive](https://github.com/guaguanco127/br.overdrive) A stereo overdrive built in gen~: antialiased tanh drive up to 128 dB, Bias for tube-style even harmonics, a Tight high-pass before the drive and a Tone low-pass after it, Auto-gain so Drive changes the sound and not the level, Level, Dry/Wet and On/Off (Off pauses the DSP). Click-free, with a State outlet on the UI version that reports every setting by name. Max/MSP, RNBO and Max for Live. Version 1.0.

## <a name="future"></a>Future Effects/Instruments

These are planned effects to be released at a later date. 

br.scrub A granular effect that scrubs through a buffer in real time. 

br.delay.reverse A reverse delay effect. 

br.skipper A granular effect that acts like a chaotic digital delay that randomly skips between delay times. 

br.repeater A type of looper that plays back the most recent "n seconds" of a stereo signal, between 0 and 10,000 ms. This differs from a regular looper in that it reads from a circular buffer. It is reactionary in the sense that if you hear something that just happened you can go back and grab it. Scrubbing and speed features will be available. 

br.strong A Karplus-Strong style synth with different features. Higher fidelity and deeper sound than the traditional synth. 

br.retrigger A granular sampler that can retrigger any sample as frequently as the Nyquist frequency without changing the pitch. Pitch shifting for timbral adjustments will be a feature. 

br.comber Not your typical comb filter. A cascade of allpass filters creates many chaotic possibilities. Almost a granular sound. 

br.looper Not your typical looper. Various granular effects will be a feature. 

br.modulator A variety of modulators (chorus, flanger, phaser, vibrato) with a variety of LFOs with folding and chaotic features. 

br.synth.detect A synth that takes in an audio signal and turns it into a synth.

Many more...

# M0SS-101 Manual

M0SS-101 is a monophonic virtual analog synth, programmed in the Faust DSP language, on the BL616 microcontroller, which includes:

- 2 oscillators (OSC), with stackable square and sawtooth waveforms, each with octave (OCT) and pulse width (PW) control. Oscillator 2 can be detuned (DTN).
- 1 filter (VCF), with high-pass, low-pass or bandpass response, resonance control, and optional key-tracking (K-T).
- 1 low frequency oscillator (LFO), with square (SQR), triangle (TRI), or random (RND) waveforms, and a frequency (FRQ) range of 0.01hz to 10khz.
- 1 amplifier (VCA).
- 1 envelope generator (ENV), with attack, decay, sustain and release controls (ADSR), with timings from 0.1ms to 20s, adjustable curves, and a gain inversion mode.
- 1 noise generator (NSE) with pink (PN) or white (WN) noise algorithms.
- 1 XOR module, applied to the square waves of the 2 oscillators.
- 1 mixer (MXR) with inputs from each oscillator, the noise generator, and the XOR module.
- 1 delay module, with time (D-TM), feedback (D-FB), and mix (D-MX) controls.
- 1 glide module with adjustable speed.
- 1 pitch-bend module with adjustable upward and downward range.
- 9 modulation paths with individual gain, connecting the LFO and ENV to the VCF cutoff, PW, OSC-1 pitch, and VCA, or to trigger the ENV from the LFO square wave.
- 1 flash memory unit to store up to 17 presets, and to remap MIDI channels per preset.
- 2 MIDI inputs (USB-A Host and 1/8" Type-A input), with OMNI / assignable channel.
- 1 MIDI thru 1/8" Type-A output.
- 1 1/4" mono audio output, line level, 100kOhm impedance.
- 1 9V dc power input, center negative.
- 1 knob to adjust parameters, which can be depressed (clicked) to trigger the ENV.

The primary function of each control is stamped above the control.  
The secondary function is stamped to the right, or beneath the control, hold ATL to access the secondary function.

If you activate a control, the row of bulbs near the bottom will often display its value in one of two ways:

**FADER:** this shows a value from 0 to 100, each bulb represents 10, and its faded value represents the 1's.  
**SWITCH:** the left 5 bulbs glow for on, the right 5 for off.

Most toggling and switching controls have a corresponding bulb which will glow yellow to indicate its state.  
For most signals, a corresponding bulb will glow green, pulsing with its signal level.

When the LFO is set to its high range (LO-HI), this signal will instead show as red~yellow, and the color temperature indicates its frequency.

Sometimes a control will have a specific numeric value (ex. MIDI channel).  
In this case a bulb will light near a control which has a small number stamped to its left.  
There are bulbs and controls for numbers 1 ~ 17.

---

## ENV GAIN INVERSION

When this control is active (it is active by default) attenuating the ENV.VCA signal will result in a higher initial gain for this signal.  
When this control is deactivated, the ENV.VCA signal operates more intuitively, where attenuating the signal results in a lower maximum gain.

---

## SAVE

1. Activate save mode (ATL + CTF) - free slots glow green, occupied slots glow orange.  
2. Press any slot to save (this can overwrite a slot).

---

## LOAD

1. Activate load mode (ALT + RES) - current slot glows green, loadable slots glow yellow.  
2. Press any loadable slot to load it (you will lose your current settings, if not saved)

**NOTE**  
Preset 17 comes pre-saved with some default settings. This is the preset that will always load at startup. You can customize your defaults by saving to this slot.

---

## Unmarked Controls

- **Hold (ALT + LFO.VCF)** = pitch-bend down semitones (1 ~ 12)
- **Hold (ALT + LFO.OSC)** = pitch-bend up semitones (1 ~ 12)
- **Hold (ALT + LFO.PWM)** = MIDI channel (1 ~ 17, 17 = OMNI)
- **Hold (ALT + A)** = ENV curves (1 ~ 9) (1 = very logarithmic, 5 = linear, 9 = very exponential)
- **Hold ALT + click knob + turn knob** = transpose pitch (semitones)
- **Hold ALT + turn knob** = fine-tune pitch (cents)
- **ALT + ENV.VCA** = ENV inversion mode (de)activate
- **ALT + LFO.ENV + click knob** = Panic/Reset
- **ALT + LFO.ENV + OSC-1 WAV + OSC-2 WAV + click knob** = Full Factory Reset

---

## MIDI LEARN

1. Activate MIDI learn mode (ALT + ENV.PWM) - bulbs all glow orange.  
2. Select any control parameter - bulbs all glow yellow.  
3. Send any MIDI CC - bulbs all glow green (optionally repeat steps 2 and 3).  
4. Press ALT to exit.

This CC is now mapped to this control parameter. Save the preset to conserve this mapping.

To map aftertouch, hold a note on the keyboard, perform steps 1 and 2, then modulate the aftertouch.  
To map velocity, perform steps 1 and 2, and then press a key on the keyboard.

**NOTE**  
MIDI mappings are saved per preset.

---

## GLOSSARY

| Term | Meaning |
|------|---------|
| WAV | waveform |
| SQR | square waveform |
| SAW | sawtooth waveform |
| PW | pulse width |
| OCT | octave |
| MXR | mixer |
| NSE | noise generator |
| LFO | low frequency oscillator |
| WN.PN | white noise or pink noise |
| TRI | triangle waveform |
| RND | random waveform |
| FRQ | frequency |
| LO-HI | low or high range |
| CTF | cutoff |
| RES | resonance |
| HP | high pass |
| LP | low pass |
| BP | band pass |
| K-T | key tracking |
| A | attack |
| D | decay |
| S | sustain |
| R | release |
| D-TM | delay time |
| D-FB | delay feedback |
| D-MX | delay mix |

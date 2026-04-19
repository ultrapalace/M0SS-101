**V 1.0** - October 1st, 2025
- Initial release.
---
**V 1.1** - March 25th, 2026
- Bug fix: Program Change above 17 crashed the device.
- Bug fix: USB MIDI did not respect Program Change or Channel Pressure commands.
- Bug fix: Undocumented default CC mappings existed. I removed them.
- Bug fix: Only the first MIDI USB cable was read (MIDI devices with multiple cables not respected).
- Feature: Button combo to clear all learned CC mappings (**ALT + LFO.ENV + OSC-2 WAV + click knob**).
---
**V 1.2** - April 18th, 2026
- Bug fix: Note-off should purge all matching notes in the stack.
---
**V 1.2_dualenv** - April 18th, 2026
- Feature: Dual Envelopes, press **ALT + A** to toggle between ENV I and ENV II.
- NOTE: This firmware removes ADSR curves, you are stuck with linear.
---
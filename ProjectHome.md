The GMS is a Gestural Music Sequencer developed in Processing by John Keston. The application samples video and displays it either normally or inverted so it looks as though you’re looking into a mirror. Each frame is analyzed for brightness, then the X and Y data of the brightest pixel is converted into a MIDI note. The X axis is used to select a pitch, while the Y axis determines the dynamics. As users move, dance, gesture, or draw in front of the capture device, notes are generated based on a predetermined scale. Currently the available scales are pentatonic minor, whole tone, major, minor, and chromatic, all of which can be dynamically selected during a performance.

The scale can also be adjusted using probability distributions. Each note in the twelve tone chromatic scale can be given weighted randomness from zero to one hundred. Notes set to zero will not play, and notes set to one hundred are most likely to play when the probability distributions are enabled.

Other dynamic controls include MIDI out channel, BPM, low and high octave, transposition, sustain, duration selection (manual or randomized with probability distributions), BPM adjustment, and note randomization. A “free” mode allows the durations to be manipulated by the mean brightness of the video input. Finally, four, simple video filter presets were recently added that can be applied by pressing shift + [1-4]. The application works especially well in dark lighting while using a light source to control the sequencer. More information on the controls and features can be found in the readme.txt file distributed with the download.

Important notes:
1. Read the readme.txt!
2. There are known bugs in this software (see step 1).
3. Please follow the steps in the getting started portion of the readme.txt before emailing me.
4. To use the inter-application drivers (IAC Drivers) with the GMS to send MIDI to and receive external sync from external applications like, Ableton Live, or Reason, you must install the Mac OS X universal binary java Midi subsystem (mmj.jar).
5. Have fun and if you make something cool post a link in a comment at http://audiocookbook.org/gms.

View a video short about the GMS
http://audiocookbook.org/one-sound-every-day/gestural-music-sequencer-documentary-short/

Audio examples and more video produced using the GMS
http://audiocookbook.org/category/gms/

Acknowledgements:
Special thanks goes to Grant Muller for his extensive work on improving the RWMidi library for Processing.org. Grant was also an essential resource on external MIDI synchronization and optimization of the application. Thanks, also to Ali Momeni for his suggestion of using probability distributions and inspiring me to develop the software as a potential tool for Minneapolis Art on Wheels (minneapolisartonwheels.org).
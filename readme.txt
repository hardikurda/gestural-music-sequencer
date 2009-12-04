TITLE: GMS Version 0.9
AUTHOR: John Keston
VERSION DATE: August 9, 2009
WEB: http://audiocookbook.org/category/gms/


DESCRIPTION:
The GMS is a gestural music sequencer developed in Processing (processing.org). The application samples video and displays it either normally or inverted so it looks as though you're looking into a mirror. Each frame is analyzed for brightness, then the X and Y data of the brightest pixel is converted into a MIDI note. The X axis is used to select a pitch, while the Y axis determines the dynamics. As users move, dance, gesture, or draw in front of the capture device, notes are generated based on a predetermined scale. Currently the available scales are pentatonic minor, whole tone, major, minor, and chromatic, all of which can be dynamically selected during a performance. 

The scale can also be adjusted using probability distributions. Each note in the twelve tone chromatic scale can be given weighted randomness from zero to one hundred. Notes set to zero will not play, and notes set to one hundred are most likely to play when the probability distributions are enabled.

Other dynamic controls include MIDI out channel, BPM, low and high octave, transposition, sustain, duration selection (manual or randomized with probability distributions), BPM adjustment, and note randomization. A "free" mode allows the durations to be manipulated by the mean brightness of the video input. Finally, four, simple video filter presets were recently added that can be applied by pressing shift + [1-4]. The application works especially well in dark lighting while using a light source to control the sequencer.

Note: to use the inter-application drivers (IAC Drivers) with the GMS to send MIDI to and receive external sync from external applications like, Ableton Live, or Reason, you must install the <a href="http://www.humatic.de/htools/mmj.htm">Mac OS X universal binary java Midi subsystem</a> (mmj.jar). 

LICENSE:

This software is licensed under the terms of the GNU General Public License as published by the Free Software Foundation, version 3 or later. However, I have not released the source yet so that I can clean things up a bit before other developers get involved in the project. For now the release is limited a compiled version of the application for Mac OS X only. The GMS Version 0.9 is distributed "as is" from http://audiocookbook.org/gms/ in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details. See http://www.gnu.org/licenses/ for a copy of the license.


ACKNOWLEDGMENTS:

1. A special thanks goes out to Grant Muller (grantmuller.com) for his extensive work on improving the RWMidi library for Processing.org. Grant was also an essential resource on external MIDI synchronization and optimization of the application. 

2. Thanks to Ali Momeni (alimomeni.net) for his suggestions on using probability distributions and inspiring me to create the software as a potential tool for Minneapolis Art on Wheels (minneapolisartonwheels.org).


GETTING STARTED:

1. To create sound using the GMS start by selecting a MIDI out device. 
2. Next choose a camera that's either attached or built into the computer.
3. Click the internal sync radio button.
4. Press spacebar to start playing.
5. For external sync, choose the SYNC device first then click the external sync radio.
6. Try setting different MIDI channels, scales, octave ranges, etc. to each preset.
7. Switch the presets with ctrl + (1-0)
8. External control is currently available for the Korg MS2000 only. 
 

KEYBOARD CONTROLS:

[alt+h]                                         = show or hide status / help
[ctrl+0-9]                                      = Choose a preset from 0 to 9
[space]                                         = stop / start
[shift]                                         = toggle sustain
[tab]                                           = toggle box around brightest coordinates
[f]                                             = toggle between free and bpm mode
[up/down]                                       = calibrate free mode or +/- bpm
[left/right]                                    = change MIDI output channel
[z,x,c,v,b,n,m]                                 = set durations from whole to sixty fourth
[.]                                             = dot the current duration
[q,2,w,3,e,r,5,t,6,y,7,u]                       = transpose starting from C through B
[g,h,j,k,l]                                     = choose the scale
[/]                                             = toggle duration probability distributions
[;]                                             = toggle note probability distributions
[-]                                             = toggle video mirror image
[esc]                                           = toggle full screen mode
[`]                                             = toggle soft full screen mode (for multiple monitors)
[delete]                                        = panic button (stop all notes on all channels)
[!,@,#,$]                                       = filter video


OPEN ISSUES:
1. 2009-05-09 Set directory for load / save to GMS parent folder
2. 2009-05-09 Filter files to .gms and .mov in dialog
3. 2009-05-09 Loading a video loop sometimes causes exception and application crashes
4. 2009-05-09 Choosing a camera that's not available may cause an exception and crash
5. 2009-05-09 Choosing the same camera again may cause an exception and crashes
6. 2009-05-11 Setup a key control to show/hide the video???
7. 2009-06-02 Allow loading separate XML files for external controllers


RECENT FIXES:
1. 2009-05-08 Change panic button from delete to to something else (SOLVED)
2. 2009-05-08 Use SAVE and LOAD dialogues instead of fields (interferes with key controls) (DONE)
3. 2009-05-09 Investigate solutions for MIDI latency issue (IMPROVED)
4. 2009-05-09 Fix bug where turning off note probabilities reverts to Chromatic scale (FIXED)
5. 2009-05-09 Fix bug where turning off duration probabilities uses last played duration (FIXED)
6. 2009-05-10 Fix stuck note after stopping (FIXED)
7. 2009-08-05 Change from JFileChooser to FileDialog for load/save operations (DONE)
8. 2009-08-06 Prevent GMS start on external sync start message (DONE)
9. 2009-08-06 Resequence presets to 1-10 vs 0-9 (DONE)
10. 2009-08-09 Adjust external control for MS2K and add version number to UI (DONE)
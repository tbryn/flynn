Version History

FLYNN 3.0 .mat input (EEGLAB format
FLYNN 2.0 trial eeg text file input, multiple .mat output
FLYNN 1.0 average eeg text file input, single .mat output

Major/Minor Revision History

3.5.0
FLYNN now interpolates missing channels and reorders them to match the user-specified locs file.

3.4.8
Fixed bug where program crashed if there was only one instance of a marker. Added commmented out code that does a moving window for artifact rejection.

3.4.7
Fixed a bug where FFT.data did not exist (should be EEG.data).

3.4.6
Further fixed the artifact vector for ALL analyses - was messing up on epoched versus continuous data.

3.4.5
Fixed the artifact vector for ALL analyses.

3.4.4
Updated the DISC summary to include proportion of rejected trials (as opposed to accepted). DISC now stores participant and condition names.

3.4.3
Made the visualization a function; changed the way artifacts are displayed (as a 2D plot instead of a bar graph).

3.4.2
Minor bug fixes

3.4.1
doFFT now returns power instead of amplitude. Additional comments added to doFFT.

3.4.0
Flynn now requires a user-defined electrode locations file. Removed code associated with not having a user-defined locs file.

3.3.5
Artifact bug in ALL analysis when more than one ALL was specified.

3.3.4
Fixed two bugs in WAV code.

3.3.3
Removed some test code (including a stray "for").

3.3.2
Bug fix in FFT baseline.

3.3.1
Fixed a bug for ALL anlyses of only one marker type.

3.3.0
FLYNN can now take continuous EEG data from Analyzer. Also fixed a bug where single participant summaries didn't display rejected trials properly.

3.2.2
Bug in artifact rejection (gradient criterion was only counting increases in voltage). 

3.2.1
Function now returns DISC.

3.2.0
FLYNN now takes as optional second argument a user-specified locs file. The variable chanlocs is compared to the user-specified locs file - chanlocs and data are reordered as needed.

3.1.5
Compare chanlocs of first participant with subsequent participants. Add info to DISC. Display warnings if chanlocs inconsistent.

3.1.4
Changed isRejected to isArtifact for clarity.

3.1.3
Allow for case where user does not provide a path name (default to FLYNNConfiguration.txt)

3.1.2
Added ALL as an analysis type (all trials)

3.1.1
Removed audio, since it won't work in Westgrid anyway

3.1.0
FLYNN is now a function that takes the config file as argument
WAV data now saved properly
doWav actually returns wavelet now
Baseline subtraction now uses repmat to be compatible with older versions of Matlab

3.0.1
Removed working directory (users will just add it to the config file, line one)
Removed tic/toc (users can add this if they wish)
Removed TODO list (will appear below)
Initialized all WAV variables
Use dsearchn to find indices (baseline, ERP, FFT, WAV)
Allow for no EEG baseline, 

TODO
- deal with missing config file
- restrict all ERPs to have the same timepoints?
- warn if about to overwrite exisiting .mat files?
- output a text summary of artifacts by participant and condition
- make artifact rejection a function
- deal with the case that there is only one condition (extra legend entries at end)
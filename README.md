# PYNQ-Z2-Audio

This project involves using the PYNQ Z2 board to play with audio and use peripherals such as the OLED display to show information about the audio files being played.
![alt text](https://github.com/Teirminator/PYNQ-Z2-Audio/blob/master/Images/r1.png)

## Breakdown of Files
A full copy of all files is included within the GitHub page, a full breakdown of these is listed as follows:

Images				- The folder containing all of the pictures in the Notebook <br>
Overlays			- The folder containing the custom overlays used on the board <br>
Audio.ipynb			- The main Jupyter Notebook file containing all of the code <br>
Highwaytohell.wav		-  The song file that is used with all functions <br>
README.md			- This file <br>
__init__.py			- The TinyTag initiation Python file <br>
__main__.py			- The TinyTag launch Python file <br>
fspan.wav			- The spanning frequency sound used for testing <br>
test.wav			- The filter test - clean <br>
test1.wav			- The first filter test - noisy <br>
tinytag.py			- The External TinyTag Library <br>

## Libraries Used Within Code

Pmod				- Allows the use of external peripherals <br>
Grove_OLED			- Allows the OLED to be used with predefined commands <br>
Ipywidgets			- Allows widgets to display in the Jupyter Notebook <br>
Wave				- Allows to read and write WAV files in Python <br>
Numpy			- Allows a specific type of array to be used with in the program <br>
Matplotlib			- Allows MATLAB figures and graph to be created and used <br>
Scipy				- Used on conversion from an array back into a WAV file <br>
Time				- Allows the use of timers – used in execution time <br>
Xlnk				- Allows the use of Python buffers <br>
IPython.display		- Lets audio files be played in the notebook through interactions <br>
TinyTag			- Extracts metadata from provided WAV or MP3 files. <br>

## Features Within Code
### OLED Readout
The OLED is set up to be able to display any alphanumeric character – as shown in intro.

### Streaming Audio Through Board
Takes an input and an output connection through the board and can control the individual channels of left and rights gain values to increase or decrease the volume.

### Reading WAV File
Reads a WAV file into an array to allow it to be filtered in a later stage and to be displayed in Amplitude waveforms and frequency spectrums

### Displaying Amplitude Waveform (WAV Only)
With the array assembled of the WAV file, it is then plotted using MATLAB commands to make waveforms for the channels in the sound as shown below.
![alt text](https://github.com/Teirminator/PYNQ-Z2-Audio/blob/master/Images/r2.png)

### Filtering Sound – See Filter Overlay Section below

### Displaying Frequency Spectrum (WAV Only)
With the array assembled of the WAV file, it is then plotted using MATLAB commands and Fourier transform commands to make waveforms for the frequency spectrum in each of the channels for the sound as shown below.
 
![alt text](https://github.com/Teirminator/PYNQ-Z2-Audio/blob/master/Images/r3.png)
### LED Bar
Lights up and is in progress to represent individual volume channels

### Recording and Playing Back Audio
Records up to a 60 second audio clip and plays it back to the user. Also allows a widget to be displayed to the user so the sound can be played out through the board.

### Info From Audio File(WAV or MP3) – Uses TinyTag
Returns the parameters of the audio file that is placed in the path. Then shows these parameters on both OLED displays to allow more information to be shown to the user. An example is shown in the following two images.

 ![alt text](https://github.com/Teirminator/PYNQ-Z2-Audio/blob/master/Images/r4.png)
 ![alt text](https://github.com/Teirminator/PYNQ-Z2-Audio/blob/master/Images/r5.png)
## Overlays
There are three overlays that are used within the project. These are the base overlay that is included in the board. An overlay that gives the ability to stream audio directly through the board and an overlay that allows the PS and PL regions of the board to be connected and a sound filtered through.

### Filter Overlay
The overlay was designed in System Generator and exported to Vivado. It is shown below.
![alt text](https://github.com/Teirminator/PYNQ-Z2-Audio/blob/master/Images/r6.png) 
The following waveforms show the outputs of the filter in the Jupyter Notebook, the first one being in software and the second using the hardware.

  ![alt text](https://github.com/Teirminator/PYNQ-Z2-Audio/blob/master/Images/r7.png)
  ![alt text](https://github.com/Teirminator/PYNQ-Z2-Audio/blob/master/Images/r8.png)

There are minute differences between the two waveforms. The execution times are vastly different. This can be further seen by opening the Jupyter Notebook.



## References
[1] TinyTag
https://pypi.org/project/tinytag/

[2] FIR Filter
https://www.fpgadeveloper.com/2018/03/how-to-accelerate-a-python-function-with-pynq.html

[3] Beautiful Soup 
https://www.crummy.com/software/BeautifulSoup/

[4] PyLyrics
https://pypi.org/project/PyLyrics/

[5] LyricMaster
https://pypi.org/project/lyricsmaster/

[6] LyricWikia
https://pypi.org/project/lyricwikia/

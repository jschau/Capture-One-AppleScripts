# Capture One AppleScripts

### Digital Zoom FOV Simulation

The Leica Q3 43 allows the photographer to apply a digital crop, aka digital zoom, to images. When shooting in DNG RAW format, the camera retains the full uncropped image and simply writes these zoom values as metadata instructions. When shooting in JPEG format, however, the digital crop is baked into the file destructively. 

Capture One initially displays your image without the digital crop applied.

This script crops the primary variant to the FOV of the digital zoom focal length. The FOV is basically what you see in the viewfinder at that focal length.

Specifics for the Leica Q3 43's digital crop sizes: 

* Native: 43mm (Zoom Ratio: 1/1) 
* 60mm equivalent: approx. 1.4x (Zoom Ratio: 1.4/1) 
* 75mm equivalent: approx. 1.7x (Zoom Ratio: 1.7/1) 
* 90mm equivalent: approx. 2.0x (Zoom Ratio: 2.0/1) 
* 120mm equivalent: approx. 2.8x (Zoom Ratio: 2.8/1) 
* 150mm equivalent: approx. 3.5x (Zoom Ratio: 3.5/1)

### Requirements

1. An image file from a Leica camera with digital zoom, such as the Q3 43.
2. The Unix app, exiftool, must be installed in /usr/local/bin/. ExifTool by Phil Harvey can be found at https://exiftool.org. Download the latest macOS package.
3. Install the script in Capture One's scripts folder: Scripts > Open Script Folder.

### Using the script

Select a Leica file and run the script.

### Notes and Warnings

The macOS package installs the ExifTool command-line application and libraries in /usr/local/bin.

If you run Digital Zoom FOV Simulation within Script Editor or Script Debugger, the part of the code that is meant to send keystrokes to Capture One will end up in the script itself. 

The script is Leica only.

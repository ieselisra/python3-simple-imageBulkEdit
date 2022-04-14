# python3-simple-imageBulkEdit
Simple Python3 Script did for a "Google IT Automation" course challenge.

Rotate, Resize and convert to JPEG all files on a single directory*.

The new images are stored with the original Filename and without extension**



## Usage:
python3 python3-simle-imageBulkEdit.py

### The script ask for 4 inputs:
pathOrigin = The original (full or relative) Path to the images directory.
pathDestination = Directory where the images are going to be saved.
desiredRotation = Rotation in degrees (clock direction) for the new image.
desiredSize = Tuple with the desired size (like "128, 128")

## WARNINGS
### Warning 1 *
WARNING: The directory can only contain images (May be a future update).

### Warning 2 **
Without extension: Set the "desiredExtension" variable to set up an extension for your files.

### Warning 3
All parameters must to be given to avoid a crash

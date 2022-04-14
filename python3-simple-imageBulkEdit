#! /usr/bin/env python3

# import modules
import os
from PIL import Image

# Directories
pathOrigin = input("Original Directory (full or relative path): ")
pathDestination = input("Destionation Directory (full or relative path): ")

# Desired Parameters
desiredRotation = int(input("Desired Rotation (º)"))
desiredSize = int(input("Desired Size x, y (ex: 128, 128)"))
desiredFormat = "JPEG"
desiredExtension = "" # like ".jpeg"

# Get the list of all files and directories
# TODO Filter files > only images
imagesList = os.listdir(pathOrigin)

# Info: Number of images found
print("Images found on the directory :", len(imagesList))


for image in imagesList:
  with Image.open(pathOrigin + "/" + image) as im:
    im= im.rotate(desiredRotation)
    im= im.resize(desiredSize)

    # Get original Filename without extension
    originalName = os.path.basename(image).split('.')[0]

    # Create destinatio path, with FileName and Extension
    objectiveFilename = pathDestination + "/" + originalName + desiredExtension


    #Check if destination dir exists, create if not
    if(not os.path.isdir(pathDestination)):
      os.makedirs(pathDestination)

    # Convert to RGB (a must for JPEG) and save
    im.convert("RGB").save(objectiveFilename, desiredFormat)

    # Info
    print("Saved image: " + objectiveFilename)

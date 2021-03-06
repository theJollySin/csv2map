# CSV 2 Map

This project is a collection of simple Python 2.7.x scripts designed to take a CSV file of lat/lon point data and plot it in a more geographic format.

Currently, the two geographic formats supported are KML and ESRI-formatted shapefiles. These utilities are described in more detail below.

## CSV 2 KML

### Purpose of this utility

This utility is not meant to be a general solution to creating KML files. Instead, it is a simple tool to create a set of point markers in Google Earth.

This tool has grown out of the need to occasionally look at geographic point data. There are obviously many ways to do that, but I found this script to be the fastest.

To the student, this file will also serve as an introductory example of object-oriented programming in Python.

### Input file formatting

The only thing absolutely required by this script is that the input CSV file has at least two columns: lat and long. The script is forgiving as to the spelling of these names: Lat, lat, Latitude, Lon, long, Longitude, LongITUdE, et cetera.

As a bonus, this script will make use of the time slider in Google Earth if there is a column labeled "datetime".

### Flags and Options

    -i: input CSV path (default is ./locations.csv)
    -o: output KML path (default is /path/to/filename.csv)
    -p: map icon path (default is a circle)

## CSV 2 SHP

### Purpose of this utility

This utility is not meant to be a general solution to creating shapefiles. Instead, it is a simple tool to place a set of points into a shapefile.

### Requirements

Because ESRI shapefiles are a proprietary, binary format, and involve projection math, some non-standard Python libraries are used. In order to run this script, you will need to install OSGEO and PYPROJ. 

### Input file formatting

The only thing absolutely required by this script is that the input CSV file has at least two columns: lat and long. The script is forgiving as to the spelling of these names: Lat, lat, Latitude, Lon, long, Longitude, LongITUdE, et cetera.

### Flags and Options

    -i: input CSV path (no defaults)
    -o: output Shapefile path (default is /path/to/your_csv.shp)
    -p: map projection (default is currently a California Lambert grid)


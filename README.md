# ShotPlot
A simple plotting program for visualising survey data primarily collected in a cave environment that can be run in a web browser.

### Overview

ShotPlot ingests a .csv file containing various sections of information, a sample file is provided as [```Sample.csv```](https://github.com/EdwardALockhart/ShotPlot/raw/main/Sample.csv). The .csv file is formatted in a specific way with different sections separated by blank lines.

The top section is the project header which contains the project name and the deviation value in decimal degrees of magnetic north from grid north (east is positive, west is negative). This can be left blank if no correction is to be applied to compass readings.

The next section is the fixes header. Here XYZ coordinates can be supplied for specific stations that represent surface locations with subsequent stations progressing underground. These coordinates must be in a coordinate system that uses metres as its unit of measurement. If no surface coordinates are available, supply at least one fix for an origin station of coordinates XYZ, all other stations will be plotted from this location.

The final sections, which can be separated by blank lines to aid organisation, hold the raw survey data which represent station-station measurements of distance, azimuth and inclination. These station-station measurements can be supplied in any order as they will be intelligently connected to any fixes or origin points. When the ToStation is noted by a hash (#), this represents a splay which captures the expanse around the FromStation and is plotted differently.

### Usage
Visit [![ShotPlot](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/EdwardALockhart/ShotPlot/blob/main/ShotPlot.ipynb) and follow the instructions.

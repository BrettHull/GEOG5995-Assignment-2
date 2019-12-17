# GEOG5995
### Assignment 2 of GEOG 5995 - Site Location Problem
 
## About
 
This project takes three raster input files to create a map of Great Britain in a 530 x 335 grid. The raster files contain values representing the population, geology and transportation options available in that area.

Running through the model creates a window in the notebook which shows a map with population, geology and transportation set to equal weights. There are three sliders which allow the user to adjust the weights to their preference on a scale of 0 to 100. Please note that setting all of the weights to 0 is not possible. The code will automatically set the weights for each attribute to 50 and reload the  map.

The final block of code allows the user to view the map, adjust weights for each attribute, submit updated weights and save the weighted raster data to an output file named 'output.txt'.

## Installation

The program is included in the zip file with this README. If you do not have the zip file it can be found in the relevant github repository at [here](https://github.com/BrettHull/GEOG5995-Assignment-2)

## Running the model

In order to run this model, you will need to unzip the Assignment 2 folder, open Jupyter Notebook and navigate to the directory of the unzipped folder and open the Site Location notebook. 

Once open, the user will need to run through the code from top to bottom.

## License 

Please find the license included in the zip folder with this README. It can also be found at the github repository [here](https://github.com/BrettHull/GEOG5995-Assignment-2).

## Development log

This software was developed using the waterfall model. The initial stage was to read through the design brief and marking scheme to fully understand the requirements. After this a design was put into place on paper in order to better understand how the code would need to be laid out. The code was then written with tests conducted at each stage. If an error was raised, the code was modified until working correctly and in an efficient manner. The code was then tested in full. Following completion, the software and documentation was assessed against the requirements to maximise satisfaction. 
 
The waterfall model was chosen due to the relatively small size of the project and the limited interaction available with the end user. With more involvement from an end user, an interative design such as Agile with opportunies for feedback.   

| Date  | Issue  | Resolution |
|-------|--------|------------|
| 12/11/2019| Investigated the best way to import rasters| Discovered the rasterio package which claimed to be faster|
| 12/11/2019| Rasterio package did not read the raster files and were imported in a different format | Reverted to reading the raster files as was taught in the module| 
| 15/11/2019| Ideally wanted to load a seperate window for the program to show map, sliders and buttons.| Considered using Qt, Plotly and Bokeh to make an interactive map but all had issues running the program. I eventually settled for using normal widgets and having it appear inline |          
| 08/12/2019 | Issues arose regarding ensuring the values of each location on the map were between 0 and 255. I had plans to take the maximum value and adjust it to 255 with every other score being proportionate | This solution was needlessly complex and inefficient. The weightings themselves are now recalculated in the code to ensure they added to one whilst the user could still chose any value between 0 and 100 on the slider|   
| 12/12/2019| If all sliders were set to 0, the application would crash due an error dividing by 0 | Implemented an If statement in the normaliseWeightings function which  checked if the total score of each slider was 0 before creating the new plot|  
| 12/12/2019| The above If statement printed an error message but the processData function would still try to run after the issue was corrected in the normaliseWeightings function and a different error would occur. This error was due to the processData function not having any weightings to use| Ensured that the If statement in the normaliseWeightings function returned default values|  

## Authors and acknowledgement

This work has been completed by Brett Hull and will be assessed towards completion of the GEOG5995 module. 

It has used and modified code taken from the practicals taught in the module which can be found at [https://www.geog.leeds.ac.uk/courses/computing/study/core-python-phd/](https://www.geog.leeds.ac.uk/courses/computing/study/core-python-phd/)

Information was also taken from the Jupyeter Widgets site found at [ipywidgets.readthedocs.io/](ipywidgets.readthedocs.io/)

Background research was also completed using the Geo-Python 2019 course by the University of Helsinki found at [geo-python.github.io](geo-python.github.io) and 'Learning Python with Raspberry Pi' book by Alex Bradbury and Ben Everard. 
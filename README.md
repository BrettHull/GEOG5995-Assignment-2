# GEOG5995
### Assignment 2 of GEOG 5995 - Site Location Problem
 
## About
 
This project takes three raster input files to create a map of Great Britain in a 530 x 335 grid. The raster files contain values representing the population, geology and transportation options available in that area.

Running through the model creates a window in the notebook which shows a map with population, geology and transportation set to equal weights. There are three sliders which allow the user to adjust the weights to their preference on a scale of 0 to 100. Please note that setting all of the weights to 0 will cause the program to have an error. 

The final block of code allows the user to view the map, adjust weights for each attribute, submit updated weights and save the weighted raster data to an output file named 'ouput.txt'.

## Installation

The program is included in the zip file with this README. If you do not have the zip file it can be found in the relevant github repository at [here](https://github.com/BrettHull/GEOG5995-Assignment-2)

## Running the model

In order to run this model, you will need to unzip the Assignment 2 folder, open Jupyter Notebook and navigate to the directory of the unzipped folder and open the Site Location notebook. 

Once open, the user will need to run through the code from top to bottom.

## License 

Please find the license included in the zip folder with this README. It can also be found at the github repository [here](https://github.com/BrettHull/GEOG5995-Assignment-2).

## Development and testing

Further to the 'Site Location' notebook, a second notebook called 'Assignment 2 Development' is also available. This notebook is used for developing new features and testing the code. It therefore includes testing code and should not to be used by casual users.

#### Development log

This software was developed using the waterfall model. The initial stage was to read through the design brief and marking scheme to fully understand the requirements. After this a design was put into place on paper in order to better understand how the code would need to be laid out. The code was then written with tests conducted at each stage. If an error was raised, the code was modified until working correctly and in an efficient manner. The code was then tested in full. Following completion, the software and documentation was assessed against the requirements to maximise satisfaction. 
 
The waterfall model was chosen due to the relatively small size of the project and the limited interaction available with the end user. With more involvement from an end user, an interative design such as Agile with opportunies for feedback.   

| Date  | Issue  | Resolution |
|-------|--------|------------|
|       |        |            |
|       |        |            | 
|       |        |            |  
|       |        |            |  
|       |        |            |  
|       |        |            |  
|       |        |            |  
|       |        |            |  
|       |        |            |  
|       |        |            |  




## Authors and acknowledgement

This work has been completed by Brett Hull and will be assessed towards completion of the GEOG5995 module. 

It has used and modified code taken from the practicals taught in the module which can be found at [https://www.geog.leeds.ac.uk/courses/computing/study/core-python-phd/](https://www.geog.leeds.ac.uk/courses/computing/study/core-python-phd/)

Information was also taken from the Jupyeter Widgets site found at [ipywidgets.readthedocs.io/](ipywidgets.readthedocs.io/)

Background research was also completed using the Geo-Python 2019 course by the University of Helsinki found at [geo-python.github.io](geo-python.github.io) and 'Learning Python with Raspberry Pi' book by Alex Bradbury and Ben Everard. 
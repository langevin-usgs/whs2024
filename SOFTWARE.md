# Software Installation
To get the most out of this workshop, you will need to come prepared with a laptop computer that has Python installed.  We will be using the Miniforge software to help us download and install Python and required dependencies needed for the workshop.  

The following instructions will guide you through the installation process and setup of a whs2024 environment.

## Part 1 -- Install Miniforge
1. Go to the miniforge website and download the installer (https://github.com/conda-forge/miniforge) for your platform.
2. Run the installer program that you downloaded.  On Windows the installer is called Miniforge3-Windows-x86_64.exe.
3. Click through the installer options, and select "Just Me (recommended)" if asked.  Default installation options should be fine, with the exception that you should select an installation location that does not have any special characters or spaces in it.
4. After installation, you should see "Miniforge Prompt" as a program under the Windows Start menu.

## Part 2 -- Create an Environment File
We will use an environment file to create a containerized version of Python and packages needed for the class.  An environment file is simply a list of packages that we want to install.

1. Using a text editor, such as Notepad or Notepad++, create a file called `environment.yml`.  It should have the following 
contents.  Save this file to your hard drive, preferably near the miniforge installation location.

```
name: whs2024
channels:
  - conda-forge
dependencies:

  # primary dependencies
  - python=3.12
  - numpy
  - matplotlib
  - scipy
  - pandas
  - flopy

  # other useful packages
  - pip
  - jupyter
  - jupytext
  - jupyterlab
  - openpyxl
  - xlrd
  - netcdf4
  - pyshp
  - rasterio
  - rasterstats
  - fiona
  - descartes
  - pyproj
  - shapely
  - geos
  - geojson
  - geopandas
  - xarray
  - rioxarray
  - uxarray
  - pyyaml
  - rtree
  - pyvista
  - vtk
  - imageio
  - requests
  - pytest
  - statsmodels
```

## Part 3.  Create the whs2024 Environment

1. Start the miniforge prompt from the Windows start menu.  This will bring up a Windows terminal.
2. At the terminal prompt enter the following command, where `<path to file>` is the location of the environment.yml file that you created in Part 2.  You will need to be connected to the internet for this to work properly.
```
mamba env create --file <path to file>/environment.yml
```
3.  After the environment has been installed, you may activate this new class environment with the following command
```
mamba activate whs2024
```
4.  The windows terminal prompt should reflect the current environment:
```
(whs2024) C:\Users\JaneDoe>
```
5.  We will be using jupyter notebooks in the workshop.  To test if jupyter is installed and working properly use the following command.  After entering this command, the default web browswer should open to a Jupyter Lab page.
```
jupyter lab
```

The setup is complete.  We will start using jupyter notebooks the morning of the workshop.

# Preparation for the Workshop
If you have never used Python before, there are many online resources for getting started.  A recommendation is to start with the tutorial at https://cscircles.cemc.uwaterloo.ca/.
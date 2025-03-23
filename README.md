# Photogrammetric Flight Plan Generator

This Jupyter Notebook provides a tool for generating photogrammetric flight plans based on user-defined parameters. It calculates essential flight parameters such as the Ground Sample Distance (GSD), flight altitude, photo coverage area, flight path, and Ground Control Points (GCPs). It also creates a KML file with the generated flight plan that can be viewed in mapping software (e.g., Google Earth).

## Features

- **User Input Parameters:**  
  The notebook prompts the user to enter camera specifications (sensor size, image resolution, focal length), desired GSD (in cm), overlap ratios, and study area coordinates. Default values are provided if no input is given.

- **Calculations:**  
  - **GSD Calculation:** Computes the actual GSD based on camera parameters and flight altitude.  
  - **Flight Altitude:** Determines the required flight altitude to achieve the desired GSD.  
  - **Photo Coverage Area:** Calculates the ground area covered by a single photo.  
  - **Flight Path Generation:** Creates a grid-based flight path that ensures proper photo overlap.  
  - **GCP (YKN) Positions:** Determines the positions of Ground Control Points based on the study area dimensions.
  
- **KML File Output:**  
  The notebook saves a KML file containing the study area, flight path, and GCP locations. This file can be imported into mapping applications for visualization and further planning.

## Requirements

- Python 3.12
- [NumPy](https://numpy.org/)
- [SimpleKML](https://simplekml.readthedocs.io/en/latest/)
- [JSON](https://www.json.org/json-en.html)
- [Matplotlib](https://matplotlib.org/)
- [Jupyter Notebook (or JupyterLab)](https://jupyter.org/)

Make sure you have the required libraries installed. You can install them via pip:

```bash
pip install numpy simplekml matplotlib

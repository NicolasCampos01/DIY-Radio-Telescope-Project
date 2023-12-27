# DIY-Radio-Telescope-Project
This repository contains a set of Jupyter Notebooks for the analysis of astronomical spectroscopy data obtained from a radio telescope. We aim to study the galactic rotation curve by detecting the 21 cm hydrogen spectral line. Inspired by Jonathan Williams and the RET program at the University of West Virginia. The notebooks are organized in a sequential order to guide users through the calibration, inspection, and analysis process.

# Key Points
Codes for data processing, data obtained with the telescope and GNU Radio Software.

# Code Overview

## calibration.ipynb
Purpose: Calibration of astronomical spectroscopy data using the methodology from the book "Essential Radio Astronomy" (Chapter 3.6.6).
Functions:
Calculate average spectra (hot and cold).
Analyze the Hot/Cold ratio.
Fit a quadratic polynomial for adjustment.
Calculate receiver temperature and system gain.
Output: Results saved in a calibration.csv file.

## inspect.ipynb
Purpose: Inspection of spectra in different directories to identify outliers.
Function:
inspect(directory): Visualizes spectra in a single panel.
Output: Spectra images saved as .png files.

## calibrate.ipynb
Purpose: Calibration of spectra from (frequency, counts) to (velocity, temperature).
Functions:
Convert frequency to radial velocity.
Calculate average spectrum.
Calibrate spectra in each subdirectory.
Output: Calibrated results saved in the calibrated_spectra directory.
## baseline.ipynb
Purpose: Adjustment of a baseline to calibrated spectra and application of barycentric velocity correction.
Output: Resulting spectra saved in the reduced_spectra directory.

## rotation_curve.ipynb
Purpose: Detailed fitting of 21 cm lines using Gaussian functions through the gausspy tool.
Functions:
Decompose spectral lines.
Fit Gaussian functions.
Analyze and plot the galactic rotation curve.
Output: Detailed graphs and a file containing the rotation curve as a function of galactocentric distance.

# How to Use
Start with calibration.ipynb to calibrate your data.
Use inspect.ipynb to identify and handle outliers, if any.
Proceed with calibrate.ipynb for further data calibration.
Apply baseline adjustments and barycentric corrections using baseline.ipynb.
Finally, use rotation_curve.ipynb to perform a detailed fit and obtain the galactic rotation curve.
Feel free to explore and adapt the codes for your specific data and analysis needs. If you encounter any issues or have questions, please refer to the respective notebook for guidance.
For any inquiries please contact me at: nicolas.campos.a@usach.cl







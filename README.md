# isoclassify_direct_implementation
Author: Aniket Sanghi

Institution: The University of Texas at Austin

This is a general purpose python notebook to work with the isoclassify package to extract stellar parameters using photometry stored in a table in the FITS file format. As the user, you just have to specify the filepaths on your system (corresponding to the location of your files and installations) and the names of the columns in your FITS file. Follow the comments starting with USER. Generally, users will just have to modify cell 1.1 and run subsequent cells as is.

Pre-Requisite: Installation of Isoclassify from https://github.com/danxhuber/isoclassify

Note: The program will NOT crash if your data has NaN values.

# From isoclassify README:

## Direct Method:
Uses bolometric corrections and extinction maps to derive stellar parameters using direct physical relations. Masses and densities are only calculated for cool stars within the empirical relations by Mann et al. 2019 (to derive masses for any star, use grid modeling mode described above). Options are:

RA/DEC + Photometry + (Spectroscopy) + Parallax -> Teff, R, L, distance, Av (+ M & rho for cool stars). Uses Monte-Carlo method to implement exponentially decreasing volume density prior with a length scale of 1.35 kpc (Astraatmadja & Bailer-Jones 2016)

RA/DEC + Asteroseismology + Spectroscopy -> logg, rho, rad, mass, lum, distance, Av. Uses Dnu scaling relation corrections by Sharma et al. (2016) [not yet implemented]

Bolometric corrections are interpolated in (Teff, logg, FeH, Av) from the MIST grid (http://waps.cfa.harvard.edu/MIST/model_grids.html)

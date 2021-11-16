# AGN-data-Mrk335

This repository contains the time lags (lag-frequency) for the combined spectral data and also groups of hi and lo spectral flux. It also contains the source arf and rmf files and the associated background and grouped spectral files for swift reporduction and further work. Details of the data reduction process is as follows:

## Observations and data reduction
Each observation was downloaded from the XMM-Newton archives and processed using HEASOFT SAS software version 18.0.0. Following the standard methods, the data was cleaned of background flaring activity by creating the 10--12 keV light curve with \texttt{PATTERN==0} in 100 bins, and removing high particle flaring generally above 0.4 counts s$^{-1}$ before further processing. These flares were commonly seen at the beginning and end of each observation. Once background flaring was removed and the light curves were then generated in 0.3--0.8 and 1--4 keV with \texttt{FLAG==0} and \texttt{PATTERN<=4}. These energy ranges were chosen because of the higher signal to noise ratio at lower energies and to provide a benchmark range comparable to existing literature. Each source was examined in \texttt{ds9} and extracted using a radius of 35 arcsecs. The associated background was selected with the same radius far from the source, whilst remaining on the same CCD chip to create background subtracted soft and hard photon light curves in 10s bins. 

# SITELLE Notes

*Notes from the SITELLE Workshop, May 12 — 14.*


## Laurent

- 350 -- 900 nm e2v detectors
- 11 x 11 arcmin.
- R = 1 to 20,000 (just 17,000 in red)
- comissioning fall 2013. Shared-risk 2014A.

Originally thought of as an application for JWST (circa 2000). SpiOMME is the prototype for SITELLE at Mégantic.

FTS = imager + MM interferometer. Beam splitter to fixed mirror or moveable mirror. FT on interferogram reconstructs the spectrum per pixel. A traditional michaelson sends half the light back to source. SITELLE uses two output ports (two CCD detectors) to recover *all* the input light.

Modulation efficiency: hard to push SITELLE to UV (early in IR). SITELLE can go to 350 nm.

10 kHz servo to set Michelson path lengths.

OH fringing: coadding the images in your desired bandpass can remove fringing. Caused by the sky light coming in from different angles (with different path lengths).

**Both spectral resolution and S/N increases as you increase the number of steps!** Set cube program time -> set resolution -> define exposure time per step.

Noise: at every step the flux from the entire bandpass is recorded. Thus works best for emission lines (but Laurent promises that absorption will work too). The noise comes from the continuum!

Filters and Aliasing: 2 sec readout overhead. Best to use filters and set step size for the features your want to observe.

### Strategies

Don't use it for spectra of single stars. For cosmology, there are certain sky windows (Ha at z=0.24; 0.4, for example).

Filters: $5K to $21K per filter. $50K for filters; we can make perhaps 10 of them. 5 filters in wheel. QSO planning will be important.

### Institutional stretegy:

- MegaCam RED with Euclid
- NgCFHT by 2017

Thus we have three years to use SITELLE. We need to build large programs to collaborate on the precious little observing time available.

- M31 deep emission
- MW turbulence
- SNAGS
- NGVS follow-up?

## SITELLE Design, Performance and Progress Report (Julie Mandar)

Bigger instrument (compared to SpiOMM), so flexure is more of a consideration.

Do filters have to always come back to exactly the same position? (possibly a 10 pixel backlash in planetary gear).

How to make a two-port output: angles or corner cubes. Corner cubes require outstanding alignment for Near-UV. Thus needed to use off-axis angular separation. This limits the spectral resolution.

NUV performance requires v. flat optics under gravity and temperature changes (servo control very important).

Mirror vibration -> path length changes (breathing) -> hurts modulation efficiency. Any tilt can also hurt. Need 0.5 µrad tilt maximum.

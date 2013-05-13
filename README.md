# SITELLE Notes

*Notes from the SITELLE Workshop, May 12 — 14.*

****

# Sunday Morning

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

Design weight started at a tonne! Now 400 kg. Carbon fibre is used to build the instrument chassis! Cool stuff.


## SITELLE at CFHT (Daniel Devost)

It records fringes! Records many images that need to be indexed in a DB (probably WIRCam-style in data volume). Great datareduction is critical for getting high-impact papers out quickly.

Pipelines need to be scalable and reliable. A CFHT astronomer validates products. A *realtime* version is required for QSO observers.

Suggestions for algorithm testing and integration are welcome! (*nb.* I can vouch for this with WIRCAM).

E.g. MegaCam was originally designed for point source photometry. New Elixir-LSB mode added (there's a new SNR model for ELSB; need to talk about this with JCC). With WIRCam, a staring mode was added.

### ORBS Pipeline (Martin)

This pipeline will be integrated almost entirely into the system. Just needs to add a RT variant. Funding for Martin to work on-site for a year to champion the pipeline (much like JCC's role).

Possibility of providing PIs with analysis tools! E.g. a DS9 SITELLE (already DS9 variants for MegaCam and WIRCam exist for real-time interactive analysis).

### Science Verification Program (Glenn Morrison)

- 10--15 nights of science verification (SV) observations. This data will end up in the CFHT archive; public two months after SV ends. Starts after 3 month engineering verification phase.
- Need to develop/test PH2 and exposure time/planning tools for SITELLE observers.
- CFHT's power is in partial observing groups (i.e., can pick up observations from one night to next; currently a 36 hr window is possible.)
- Test sensitivity goals: 4 hr: 5 sigma flux: 4E-17 erg/s/cm2
- Non-sidereal guiding? e.g. comet physics
- Tests for PSF variations/distortions
- Data cube alignment? SpIOMME uses stars to re-align the datacube? Might be possible to get away without this if fluxure is solved in ORBS.
- Binning modes: 1, 2, 4
- Max datacube size is 1088 slices (this might be a limitation of overheads in high-res UV observations; want to restrict OBs over

Possible targets for SV:

- Comet. *Some timely bright comets are coming.*
- PN in elliptical galaxies
- Ly alpha in a COSMOS field
- Bright HII regions split over two needs to test partial OG observing

**Issues**: Can we do something like SCAMP astrometry for SITELLE?

## SITELLE Optics (Thibault)

Goals: need 11x11 arcmin design. Need to get lines at 370 nm. Need to design for wavefront image quality at pupil. Lots of expensive 20 cm lenses with calcium fluoride coatings for NUV. Lots of choices to make when designing optics! Lots of compromises too.

*Potentially 80% vignetting in the corner.*

**Optical cost: $170K.** 200 mm lens alone costs $35K (manufacturer didn't want to coat it; need to heat and cool such a lens slowly for coating).

Note that the optics themselves have a resolution of 0.85"; seeing is typically 0.65". Thus typical effective seeing is 1" for SITELLE images.

## Detectors (Marc Baril)

CFHT is handling the CCD system integration/software.

100 foot cryostat lines!

CCD cooled to -100˚C. Will need a fast clock rate to read in 3 seconds (250 kHz). Total cycle time is 3.5 seconds (including CCD clearing; shutter settling).

Cross-talk less than 0.1%.

*Noise associated with grounding the inputs. This will be debugged...* Should get readout noise below 5 electrons. Gain 1.8 ADU/e

## Cometary Science (Rousselot)

CFHT got spectra of Halley's comet back in 1985.

SITELLE could be great for understanding the wide-field ionization structure of a comet.

Na tail first discovered with Schmidt objective prism in 1960. Rediscovered with Na filter on Hale-Bopp in 1997. Origin of Na tail is unclear. Ejected from dust grains?

C/2012 S1 ISON will peak at V= -4 mag; perihelion passage in November 2013. Good target for SV? Trick is proximity to sunrise!

Real interest is to see where these species originate from the nucleus/coma.

## Commentary

*Devost:* Large Program call. February 2014 deadline? Hopefully the commissioning will tell us enough about SITELLE. May be only one round of LPs for SITELLE. We also need to ensure that SITELLE is not a niche instrument.

**Laurent:** pressure on getting photometric accuracy. Note that calibration procedures evolve.

**Morrison:** Some concern with building data cubes over several nights. This hasn't been done with SpiOMME.

Science Verification is a good time to try out large program observations. **This is encouraged.** Devost envisions setting up a SITELLE TAC to setup a program for science verification.

This week: develop SV programs. And choose filters!

**Question about mosaicing.** There *will* be a loss of spectral resolution from centre to edge. But this only relevant for very high R. Shouldn't be an issue for R=5000.

**Bureau:** FTS for dummies document? We need to know how to convince the TAC that FTS is the right tool for the job.

**Mandar:** For absorption lines: just use a really tight filter around the line. That will solve the continuum noise problem. Again, we need to design a set of filters. Also note that for a tight filter, you need long steps, which will impact the readout time. Want to read out only as slowly as the mirror moves to optimize read noise.

****

# Monday Afternoon

## HII Regions (Gilles Joncas)

HII regions have ionization structures, reflecting radiation fields, temperatures, electron densities, etc..

Kinematic structure: gas flows, turbulence (Reynolds number ~ 10^6), stellar winds.

Diagnostic line ratios give you temperatures, densities (their solutions are covariant). You should solve these with diagnostic lines of similar ionization potentials to ensure you're mapping the same ionization structure. Don't use Temperature of OIII to get (O/H) abundances! Also need Ha/Hb to get extinction structure.

To do a proper job:

- 370 to 955 nm
- Absolute calibration
- Large enough R to avoid night sky line blending. Note that we need to patch different spectral domains together.

Science questions

- velocity fluctuations (turbulence)
- density fluctuations (irregular boundaries)
- turbulence may be a *source* of energy (where temperature is higher).
- abundances determined from collision lines different from recombination lines (2-3 for HIIR; up to factor five for PNe!) Yikes.

Another problem is that photoionization model codes aren't fully 3D. No code includes gas dynamics either.

M42 may be good for SV because it will display internal reflections, chip defects, etc. because there is so much signal.

## Ionization Temperature Fluctuations (Oliviera)

**Abundance discrepancy problem.** We need to reconcile recombination and collisionally excited lines. Peimbert (1967) proposed that electron temperature fluctuations explain the AD problem.

OIII (L4959 + 5007)/4363 to estimation t^2, the electron temperature fluctuations.

Observational approach: poor-man's IFU with stepped long-slit spectroscopy of NGC 2579. SITELLE will fix this.

Some tricks: t^2 is modelled in 3D, but observed in 2D. Lots of thought must go into line choices.

## M27 Temperature and Density Structures (Lagrois)

Observations are a combination of four data cubes made with SpiOMM. Had to rebuilt red cube with an even narrower filter to get enough S/N. Things to think about with FTS...

SII as a density ind. NII for temperature. OI emission hidden inside dust clouds!

Sources of density and temperature structures

- shocks. Ionization maps show increased excitation at shell. Some sort of shock? Perhaps see polar shocks at either end of M27??? Don't see much temperature enhancement. 1.5x density enhancement (in fact could see cooling in the compression).
- turbulence. It looks like SII and NII are cospatial, so they can be used together to solve both temperature and density. Find turbulence as deviations from large scale kinematics.

Overall, a neat demonstration of what can be done with 2D spectroscopy.

## HII Region Kinematics and Star Formation (Russell)

Expansion of HIIR can trigger SF (see Blegling et al 2009, recently).

Herschel observations at 100, 250 and 500 µm. Can directly see SF on edges of HIIRs. Good examples are pillars of creation. See Dehaveng et al 2012.

H alpha Fabry-Perot observations along plane of MW. Not a simple match between Halpha FWHM and LOS velocity map. Means of course that there are internal kinematics in HIIRs.

What can SITELLE do (in conjunction with Herschel obs.)?

- Link dust properties with HIIR properties
- Understand HIIR impact on ISM
- Understand triggers for SF

Want to survey different morphologies fo HIIR (blister; champagne phase, pillars, etc). Select from Herschel surveys. Survey different regions of the galaxy.

## Asymmetry in Wolf-Rayet nebulae (Nicole St. Louis)

WR are >25 solar mass O stars; He-burning phase. There much to learn about their evolution, and *actually let them collapse into a SNe; GRBs*. GRB progenitors must rotate quickly; these would be young WR. Find these young WR by nebulae, which would dissipate rapidly.

Global asymmetry in wind causes continuum polarization by Thomson scattering.

If nebula was ejected during the WRs rotation, then gas kinematics should reflect that rotation. Ideal project for SITELLE since you can observe the 2D velocity field. W6 is huge: 40'x40'. More WR nebulae are about 10 arcmin though. Models don't exist for these winds. Most modelling has been done for B stars (Connection to MIMES project?). Use Ha and [OIII] for this project, simply on basis for S/N for kinematics. Add in more lines to get ionization structure at the same time.

## Hyperspectral Observations of Cas A (Alarie)

Lots of good Great Observatory coverage (HST, Spitzer, GALEX). SNIIb remnant (?). Here we look at SpIOMM 645-700 nm bandpass. 4 arc min sq. object.

*n.b.: Winner of best slide transitions.*

Sulfur doublet, NII, Halpha.

Reconstruct a 3D view of the nebula from kinematics (assumes spherical expansion?). There's a deconvolution equation that goes unexplained.

Some structures aren't moving: **Quasi Stationary Floculi**. Might have been ejected prior to the nebula. As the main nebular passed by, they are lit up.

Seems to be unusually nitrogen rich.

Multi-epoch observations between 2000 and 2009 with HST. Get transverse velocity. Traced 3500 knots and manually mapped their displacement vectors. The expansion is actually faster on the outside! Trace expansion inwards: estimate site of explosion. It seems that the star (or nebula) has moved relative to the explosion site. *Velocity would be 200 km/s. Could it be a binary pair?*

To get total velocity (combining radial and transverse), need a distance estimate. He uses spherical symmetry; finds D to make traverse velocity and radial velocities balance. *D=3.33 kpc*. Under this assumption, he gets a 'true' 3D map of Cas A.

## Using SITELLE to fine Be and other Massive Stars in CoRoT fields (Maillard)

CoRoT = Convection, Rotation and Planetary Transits. Observe opposites directions in MW between summer and winter.

Be stars rotate quickly (1.5 days). Show Balmer emission (equatorial plane envelop).

To find these... FLAMES spectrograph with 132 fibres over 25 arcmin field. They've found 21 Be stars.

With SITELLE (H alpha) one could multiplex spectra; classify stars much more quickly. Be candidates would have an Ha emission component. SITELLE could go to V~18 mag.

Near-UV? Use the Balmer decrement (360 - 390 nm) to help discriminate a B from Be star.

Note: 4 SITELLE fields would cover a single FLAMES/GIRAFFE field. First, verify SITELLE in a FLAMES field. Need R=3000 for Ha; R=1500 for Balmer decrement feature.

Note: can't just do narrowband MegaCam imaging b/c you need to careful about continuum subtraction. You could easily miss the Halpha emission.

Spectroscopic follow-up to GAIA?

## Dynamics of Ionized Gas Outside Galaxies (Guillard)

Spitzer found H2 bright galaxies powered by intense turbulence. (see Guillard 2009). e.g. Stephan's quintet. See a Giant Shock along with star formation. Shock also seen in [Cii] 158 µm.

SITELLE can answer what the role of turbulence is *in regulating star formation*. SITELLE can trace ionized gas in/outside galaxies in 

- galaxy collision
- galaxy cluster
- ram pressure stripping
- AGN/starburst

environments.

## Discussion

*Bureau* SITELLE could also be used for proper+radial velocity measurements of clusters around galaxies to estimate distances (of the cluster to the galaxy) in that case too...

****

# Monday

## 1D FTS at the CFH with BEAR (Maillard)

Milestones:

- Connes, Connes and Maillard 1969: *Atlas of NIR Spectra of Venus, Mars, Jupiter and Saturn (en Français).* with same resolution as a solar atlas.
- 1970 Aspen Intl Conference on Fourier Spectroscopy
- Two FTS on Kitt Peak in the 1970s.
- Voyager I and II as FTS
- Kuiper Airborne Obs. ad an FTS in 1980

CFH-FTS

- At f/35 Cassegrain focus
- 24" FOV.
- Rmax = 5e5 at 2 µm (exceptionally high resolution!)
- Operated 1982 - 2001 (very long operational life!)
- Applications in planetary atmospheres (e.g., Maillard 1995 obs of Jupiter's auroral zones). Found some neat lines in Ks band-- H3+ ion detected!
- Oxygen/carbon isotope ratios in the Martian atmosphere with R=430,000 spectra in H-band. Tricky because these species are in the Earth's atmosphere; work around by observing Mars at maximum doppler shift.
- Outflows from YSOs

Moving to 2D FTS in 1989: just needed to add a *CCD* camera (800x800 pixels). This was effectively the first imaging FTS. Operated in optical of course. With they 'Redeye' camera (256x256 NICMOS) renamed Bear: *Bidimensional Experience with Array Receiver*. First science result was Venus dark-side imaging of O2 in J-band window. In galactic centre, studies of Helium stars (Paumard et al 2001[??]).

Ultimately yielded NIRCAM, SpIOMM, proposal for H2EX (to explore molecular hydrogen). Akari carried an FTS covering 70-150 µm (?). SPIRE on Herschel. FTS-2 on SCUBA-2 (alas, EOL for JCMT).

A very high resolution 1D NIR FTS could fit well on TMT.

**Check out imaging FTS paper by Maillard, Drissen, Grandmon and Thibault in Experimental Astronomy 2013.**

## SNAGS: Survey of Nebular Abundances in Galaxies with SITELLE (Pierre Martin)

SNAGS is still in early planning phases; a lot of us could participate in it. Interest in how galaxies recycle gas. Looking at ISM we can fill in link between successive generations of stellar populations and how gas in lost/moved by winds.

Questions: What are relationships between abundances and galaxy properties.

Hints:

- Temonti 2004: Know relationship between galaxy mass and abundance. 
- Global O/H gradients. Outer parts of galaxies are metal poor.

Competition: PINGS + CALIFA. Optical Fibre array, 3700-7000 AA. R=1000-1600 for **600 galaxies (pending).** Approximately 1 arcmin diameter array. This survey will be great for studying global properties; gradient work might be limited.

SNAGS

1. Nebular Abundance Distribution in Spirals. From long-slit spectroscopy we know there are negative radial gradients. But very few objects have all their HII regions sampled. Revived lately (Bresolin). *Lets look at a bunch of galaxies and get uniform measured O/H gradients.*
2. Role of Bars. Bars are near-ubiquitous. How does secular evolution influence abundance gradients. (Is there a connection between truncation in stellar disks and abundance gradients). Bars are important for feeding the galaxy centre as well: *pseudobulges*. Secular evolution should work to make gradients flatter over time. We can't just measure bar influence from de Vaucouleurs type. Interesting work measuring star formation along bars (Florido 2012).

  - Is bar strength a far
  - Is bar age a factor
  - what are the gas mixing timescales for a galaxy?

We need a homogeneous sample to establish the connection between bars and abundance gradients.
3. Are abundance gradients actually linear?! E.g. NGC3359 (Zahid and Bresolin 2011). Also evidence from MW Cepheids (Andrievsky 2004). Outer disk star formation: Bresolin 2012: abundance gradients are *extremely* flat in outer regions; there is a break from inner profile. Origin of breaks:

  - Gas accretion?
  - Galaxy winds?
  - Spiral/bar resonances?
  - Minor mergers?

*Need a homogenous sample of well-resolved galaxies to establish statistics for these breaks*.

Preliminary SNAGS sample: 70 spirals that have outer disk star formation seen by GALEX. Most can be studied with 1 SITELLE pointing.

*Direct method*: Direct estimation of electron temperature from abundances. Problem is that these auroral lines are very faint. This could be a challenge for SITELLE. Instead SNAGS may try for indirect methods using bright emission lines. Martin has confidence that these indirect methods are becoming well understood in relevant environments. Possible pitfalls E.g. R23. It is crucial to use many abundance indicators simultaneously.

Three spectral ranges to cover NII/Ha/SII/HeI + Hb + x.

Megantic NIR imaging to get bar strengths.

SNAGS is open to collaborations.

What spectral resolution? CALIFA did R=1600. Want more.






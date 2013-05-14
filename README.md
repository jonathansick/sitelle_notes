# SITELLE Notes

*Notes from the SITELLE Workshop, May 12 — 14, 2013.*

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

# Sunday Afternoon

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

## Gas Fuelling in Andromeda's Nucleus (Melchior)

(nb ANDROIDS will solve the issue of using OS X backgrounds to show M31's structure).

HI (Braun 2009): in 10 kpc ring; missing from centre. CO (Nieten 2006) also in ring; issing from centre. IRAM CO observations have fat 9" pixels. MIPS 24 µm shows dust/gas at centre. Groves 2012 showed that the central dust is heated primarily by 1Gyr old stars.

Devereux 1994 Ha+[NII] emission image (1.3˚x1.3˚). Pretty low S/N image!

Block 2006: two rings possibly created by a head-on polar collision with M32. The inner ring is quite offset, thus not likely a secular resonance.

Double peaked radial velocities in inner ring on near-side. Likewise on minor axis far-side. Seems to be a counter-rotating, inclined disk.

Boulesteix 1987 Fabry Perot velocity field of HII.

What about PNe velocity field? PNe follow bulge SP. Seems to be a abundance peak of PNe on minor axes.

Weak CO detections in centre now with IRAM-PdB. Beam is 2" FWHM.
(A_B extinctions from Melchior+ 2001.)
SAURON made [OIII] emission maps; [NII] maps from Fabry-Perot.

X-ray outflows in centre.

Current state of art for central ionized gas is from Jacoby 1995! Hints that Ha and [NII] do not emit at exactly the same place.

SITELLE could help in resolving the velocity field (R=10000-15000). Should discern multiple velocity components. Need to produce separate Ha and [NII] maps because their ionization structure do seem to be different.

Questions: ring expansion consistent with about 5 km/s.

BH sphere of influence may be a few arcseconds.

## Comparing HII Regions in M31 and NGC 5128 (Barmby)

Metallicity gradient in M31 determined in 1982 with only 17 regions. Not much done since! Azimlu+ 2011 mapped M31 HII regions with GMOS spectroscopy.

In M31 can detect auroral lines to use the direct method for measuring electron temperature and abundances. See Croley. Can distinguish between SNR/HII/PNe.

Nebular Empirical Analysis Tool (NEAT) does a Bayesian analysis for electron temperature and abundance. Stock 2011, Wesson 2012. Result: *[N/O] doesn't correlate with [O/H].* This work and Zurita and Bresolin (2012) and Saunders 2012 have improved the radial gradient. *Might see gradient and break; but this is not entirely clear.* Various authors have also measure abundances with supergiant stellar atmospheres. This abundance profile is perhaps still wanting. Want to know about azimuthal gradients. Zurita and Bresola PNe abundances above HII regions. Odd.

Wavelength range 370-950 nm. Spectral resolution of 2000 would be good.

We need the tools to deal with SITELLE data. Visualization tools? IFSView (Python); PINGSoft (IDL); DS9 (C). Nice CALIFA visualizations: in Husemann 2013; Cid Fernandes et al 2013. Good inspiration. We can do better! How do we combine catalogs and N-dimeinsional data?

## Virgo Cluster (FTW) (Nathalie Ouellette)

A great laboratory for studying galaxies. SHIVir Survey: Spectroscopic and H-band Imaging of Virgo. Long-slit Palomar, KPNO and Apache Point Observatories.

**Both early and late type galaxies.** Spans morphologies, sizes and shapes.

Goals:

- Homogeneous photometric and spectroscopic sample. Want to bridge photometry and spectroscopy. Compilation of parameters: photometric and spectroscopic.
- Scaling Relations
- Defining and refining metrics for Vrot and velocity dispersion. How can scatter be minimized in scaling relations?

Rotation curves: 34 SHIVir gas-rich galaxies. In detail, deviations from regular RCs. PA alignment (will be fixed by SITELLE 2D spectroscopy!); symmetric warps; non-axisymmetric dynamics (bars, arms).

Tully Fisher Relations: V(23.5) vs Mi(23.5) works best.

Velocity Dispersion Profiles. Most studies focus on central velocity dispersion (a scalar quantity). Here, Nathalie manages to measure *sigma profiles*. Rotation corrected sigma profiles are in work. Will yield a Vc-sigma relation for Virgo galaxies!

Faber-Jackson: sigma(1.5Re) vs Mi(23.5) yields the tightest FJ. Next step is to move into the Fundamental Plane. Does the FP want rotation correction or not?

Future work: observations with Gemini to explore dwarf elliptical populations. Goal is to create a Virgo velocity function (akin to a mass function) to test galaxy formation models.

SITELLE's potential: can resolve issues in non-axisymmetric velocity fields. E.g. disentangle bar from disk dynamics. Also, photometric and dynamical position angles can disagree. Want all the data! Interactions can also create non-axisymmetric dynamics that need to be resolved. Just need Ha lines, likely with R=5000. Also create 2D dynamical mass maps.

## Square Kilometer Array (Carignan)

SKA: half to Australia for low-freq, other half to S. Africa. Note that SKA is *really* a pan-African project. Lots of countries collaborating! Arrays all the way out to Kenya.

Status: MeerKAT (64 dish)/SKA PH1 will be completed in 2016. Construction of full SKA completed by 2025 (3000 15 m dishes!). KAT7 prototype is already useful for continuum source detection.

NGC 3109 kinematics and mass distribution; getting 4 arc min spatial resolution with 1 km/s kinematic resolution. HI here extends over a degree, so this is exceptional resolution. Tests of RCs against NFW, MOND. MOND doesn't seem to fit. VLA observations were missing a lot of the HI because the field was too small. KAT7's wide field fits this niche well. Wildly warped HI disk; tilted ring modelling. Effectively doubles extent of RC from VLA observations.

SITELLE: do absorption work from Mg and Ca lines in blue and red.

Next step is MeerKat, with 64 dishes. 29m to 1 km baseline. Until SKA, this will be the most sensitive radio interferometer in the world (useful for nearby galaxies).

SKA site. Data processing will be done underground to shield radio emission.

### MHONGOOSE Survey: D<20 Mpc Galaxy HI Survey.

200h per galaxy! Covers all morphological types, AGN, etc..

- How did galaxies get their gas? Connect gas fuelling from the cosmic web.
- How is star formation regulated, etc.

With better receivers we're detecting thicker HI disks (below 1e19 atoms/cm). Study extra planar gas: fountains and accretion flows.

SITELLE optical follow-up. There *is* some declination overlap. Study how gas gets converted into stars. Higher spatial resolution will improve inner kinematic profiles for DM studies. For kinematics, Halpha Fabry-Perot with SALT. Also combine IR imaging from WISE. SITELLE OII and SII will be useful.

Projects like SKA are crucial for retaining talent in Africa.

## SITELLE + Herschel Reference Survey (Amram)

How did galaxies in the young universe form? How do they evolve? Local samples are useful for answering this because we can study them in detail. Need to figure out what we're seeing with JWST.

We see red and blue sequence galaxies that roughly correlate with early vs late type morphologies. More fundamentally, how does mass and angular momentum build up; where does SF occur; BH feedback, etc.. Need to study formation of galaxy components. Bulge formation encodes early formation history. Disk grows tells us how gas continues to accrete. How is star formation quenched (feedback from AGN, winds)?

There are now ~50 integral field spectrographs in the world. None in the 8-10m class are being used for major/complete surveys (hmm?). Most have FOV of 1 arc min. Most have R=1000-2000. DiskMass has R=10000. MANGA at SDSS/APO is doing 10000 galaxies!

Herschel Reference Survey: studies dust in 'normal' galaxies. Dust shields gas from UV field; cools the gas. (n.b., Dust is important people!)

- Dust mass/temperature/gas-to-dust ratios
- Study role of dust in ISM
- Reconstruct SEDs
- etc..

Herschel RS is *volume limited* at high galactic latitude (15 to 25 Mpc). Includes 323 galaxies (258 late types; 65 early). Includes field *and* Virgo cluster. Lots of data across the entire electromagnetic spectrum to tie in. HeDaM database combines all these.

How can SITELLE help? Need all phases of ISM: HI, H2, neutral and **ionized** (and dust). SITELLE can help with ISM (emission line fluxes and ratios) and stars (stellar populations and kinematics).

## Dynamics of Nearby (Early-Type) Galaxies with SITELLE (Eric Peng)

SITELLE's wide field could be great for providing extended dynamics that current IFUs can't reach.

- Dark matter content
- assembly histories

Nice thing about ETs is that they're great structures to study dark matter profiles since they have little gas. Stellar streams/kinematic substructures should also show up.

Other surveys: SAURON/ATLAS3D, CALIFA and MaNGA.

Outer parts of galaxies (high M/L) are where you're DM dominated. Structures from structure formation (mergers/accretions) are preserved in the outer parts of galaxies. Ideally want to cover out to 100 kpc (18 effective radii!). Discrete tracers (PNe/GCs) are necessary to trace kinematics in these low surface regimes. PNe are great: emission; intrinsically narrow (5 km/s) lines; no foreground confusion. Globular clusters: give chemistry/age and only require standard/broadband imaging to detect. Ideally want to do both.

Gemini/GMOS globular cluster kinematic survey in Virgo cluster. VCC 1231; 1062; 2000; 685. Extant PNe studies hint that there is unusually little DM in these galaxies. Found 17 -- 52 GCs per galaxy. Needed to use three masks/galaxy because of slit crowding (inefficient). Slits give GC + galaxy + sky light. Thus you can even get kinematics of diffuse galaxy light, in addition to GC kinematics. Diffuse light plot out to R=10 kpc; GCs even further out of course. Some show stars+GCs co-rotating; or GCs not rotating; inner co-rot w/ no outer rotation; or even counter rotation in outer parts! **Lots of different kinematic patterns! Wild.** SITELLE could be great here: multiplexing capabilities should pick up kinematic tracers very quickly, without central crowding problems for slits.

PNe: effectively get 10^4 solar luminosities just in the [OIII] line! Traditional observations used two step process:

1. Narrowband imaging with custom made filter for the galaxy of interest. Then off-band image to subtract continuum. Detect PNe.
2. Then use a MOS to get velocity measurements. Fibre configuration really challenging.

Two step process is logistically challenging because you need to deal with two TACs. With SITELLE you do an entire galaxy in one cube!

Width of PNe lines governed by expansion vel. (20-30 km/s). With R=10000 can get 3 km/s velocities (awesome!). Need to determine band pass of SITELLE cube: narrow to avoid sky; wide enough to cover velocity dispersion. Main contaminant are Lyman-alpha galaxies at z=3. R=10000 spectra should easily distinguish these.

PNe detection limits at Virgo distance (considering PNLF): 11 photons/minute at CFHT. Key challenge is sky: narrow band pass means you limit noise from bright sky photons. Competitive setup is narrowband imaging+VLT/FLAMES. Have great image quality means better S/N for PNe (FLAMES has fat fibers). SITELLE could be competitive in this respect.  What about WHT spectrograph? Counter-dispersed spectrograph (slitless). WHT's downfall is poor seeing. And SITELLE can do an order of magnitude better velocity resolution.

Use  ATLAS3D as a parent sample: 89 ETs within 20 Mpc. Nice demonstration that a 40 AA (5005A-5045A) bandpass filter would work well for most of these galaxies. These galaxies are also nicely sized for SITELLE's 11 arcmin FOV.

The dream: simultaneous integrated light + PNe + GC kinematic maps. This helps us understand systematics of each type of tracer.

Simard: Can we look for PNe being kicked out, potentially yielding the age of the last major merger? Very few found, but cool idea!

Should we broaden the filter to add Mg lines, for e.g.. Or would the [OIII] flux kill simultaneous absorption line studies. Probably.

****

# Monday Afternoon

## SITELLE Data Simulator (Laurent and students)

*Don't look at the numbers.* (Will be fixed of course)

Ingredients:

- Template spectrum. To understand noise, you need a template spectrum for your observation.
- Filter. Add your own; see what needs to be built.
- Specify either resolution or time available.

Simulator can turn on/off different types of noise. Will be able to automatically output S/N for various features. Will be good to add a seeing parameter.

Demonstration of how Ly alpha detection suffers in redshifted data because of higher sky flux.

Next steps:

- stellar library
- more sources: comets and galaxies
- need to include a measure of the velocity uncertainty (lots of people want to think in these terms: how long to integrate to get X km/s resolution for Y object)
- extend to 2D
- Move to Python+Web from IDL version.

## Spiral Galaxy Evolution w/ SpIOMM (Laurie Rousseau-Nepton)

SpIOMM is 12 arc min square; blue and red filters used here. Coverage of SA-SAB galaxies.

Calibration: need to do CCD corrections on the interferogram. Make a standard star data cube to do absolute flux calibration. Then sky subtraction. Finally, in this case use HIIphot to extract HII regions (Thilker 2004).

Flux calibration details: standard star, then correct for filter transmission curve. Gives a correction factor as a function of wavelength to put data cube spectra in physical units. Beyond the ZPD, the FT of a star is very constant. Thus don't need a lot of frames of the standard star. This helps you do the calibration throughout the night. (editor's note: wait for the SITELLE guide before undertaking your calibrations!)

From Halpha flux, yield star formation rate.

Look at density of HII regions in various parts (arm/interarm) regions of the galaxy. Look at HII luminosity function. The HII LF seems to be stable across all galaxies sampled. The same dataset even yields rotation curves. Can also get extinction maps.

Gas metallicity maps. Estimate with both NII/Halpha and OIII/Hbeta indicators. Metallicity gradients aren't linear. Caveats with how you do abundances with these methods...

NGC7331: flatter gradient, indication of gas mixing.

BPT analysis: HII vs AGN vs ?. The regions outside HII domain could be shocking. Or PNe? Diffuse ionized gas: this can bias measurements. (n.b. can SITELLE be used to map the diffuse ionized gas of a galaxy? Yes?) Nice thing about having 2D mapping is that SN remnants can be identified and masked from HII analyses.

Question: comparison of these indicators to the *direct method*.

## Early Type Galaxies with SITELLE (Bureau)

Early Types? He's crazy, right? But SITELLE's wide FOV makes it appealing to try absorption line studies of galaxies. ETs *do* have some ionized gas. Dark matter: disintegrated light kinematics, etc..

ATLAS3D: 40"x30" WHT/SAURON (no longer the wide-field benchmark). Has looked at all the ETs in the local volume. Having high resolution data across the electromagnetic spectrum means that you can meaningfully compare data cubes.

SAURON: narrow 400 angstrom spectral range covering [OIII], Hbeta. Use [NI] as proxy for [NII]. SITELLE driver: get kinematics at large radii with ionized gas (beyond FOV of SAURON). Line ratio diagnostics don't work here, outside traditional HII regions.  **Crucial to compare absorption line and emission metallicities**. They are really different things.

With SAURON, detect faint emission lines by modelling the spectrum; yielding emission as residuals. Needs high S/N to trust these detections.

Stellar kinematics: need to constrain dynamics are large radii in DM-dominated regime. SITELLE will be a competitive instrument for discrete kinematic tracers.

What about using SITELLE as a light bucket for integrated light studies. The stars are *always* there, but surface brightness is extremely low (µV ~23). Light bucket approach (at least with SAURON) means extreme spatial binning.

SITELLE challenges:

- Trick is to avoid strong emission lines, which will distribute noise into absorption lines. 
- Can you bin in the data cube space? How does noise propagation work?
- Note that kinematics studies observe convolution of galaxy and stellar kinematics! Modern studies use a combination of stellar templates (think: GANDALF code). Rather than convolving galaxy and stellar templates from real space, should we stick to Fourier space? Does this work? A good start would be to observe the template stars with the FTS.

SITELLE would also be great for studying cooling flows around brightest cluster galaxies. The large FOV is a real win here.

## Spiral Galaxy Stellar Populations and SNAGS (Carmelle Robert)

Stellar pops: ages, Z, stellar mass, SFR, dust, gas ionization. **Stellar archaeology**: retains the chemistry of galaxy from epoch of star formation. Want to work towards a picture of global galaxy evolution.

Kudritzki 2012: Stellar metallicity gradient from resolved Keck spectra!

Need a stellar population synthesis code to model a galaxy's stellar population (SED): IMF; SFH parameterization; stellar isochrones; stellar spectra. Then add in nebular lines. Note that dust *will* be different between different stellar populations. Taking into account Ha/Hb emission will shift the stellar population ages. IFUs will reveal the clumpy ISM. (we really need to start thinking about realistic radiation transfer; related to diffuse interstellar gas).

PINGS survey needed 36 fields over 6 nights to cover a galaxy!

We need to start thinking about doing stellar populations with IFS.

Filters:

- [OII] at 3727
- WR bump at 4686, Hb, [OIII]
- Mg, Fe lines 5177; 5270; 5335
- Ha, [NII]
- Near NaI 8200; CaT 8498; 8542, 8662, TiO

Bureau: Can detect IMF variations from line strengths in NIR. Yes... (Is this the Conroy method?)

Barmby: What pop synth codes do we use? Ultimately we need to compare them

## Stellar Systems in the Nearby Universe (Pat Côté)

There is a bird named SITELLA: we *can* do absorption line work.

Scaling relations of galaxies: Tully fisher; Faber Jackson. Guzman 1993: extend into low mass galaxies. Modern state of the art is ATLAS3D (Cappellari 2012). Extending this to even lower mass: fundamental manifolds, etc. (Zaritsky 2006; log sigma - log M/L). **The hardest thing to measure with dwarf galaxies is velocity dispersion**.

What can SITELLE do (compared to A3D and CALIFA):

- Better site than 
- Field of View
- Spatial resolution
- Flexible spectral resolution

NGVS (ugri survey of Virgo with MegaCam) could be a great parent data set to being planning a SITELLE kinematic followup. Key driver of NGVS is the luminosity and mass function (e.g. the missing satellites problem; need a richer dataset than the local group). 317 previously undetected Virgo galaxies! MacArthur 2013 is working on an automatic detection code working on CANFAR.

MacArthur 2013: SExtractor finds *a lot* of sources. The trick is to find Virgo galaxies against a background. Membership probability based on scaling relations, photometric redshifts, comparison against background fields, residual images after modelling light profiles. **Another great discriminant would be velocities**.

NGVS is finding lots of galaxies for which we need LOS velocities. Adding these would be great to understand the kinematics of Virgo. Focus on H beta either in absorption or emission to find a velocity (the line will always be there). A very narrow bandpass will help reduce noise in the SITELLE observations.

Also lots of ultra compact dwarfs (UCDs) or globular clusters. SITELLE could cover an enormous number of these.

Peng 2013: radius vs velocity dispersion. May show break between galaxy and cluster potential. Cool stuff!

Noyola 2008: intermediate mass BHs in globular clusters. Good case for SV.

## Absorption Structures in M87 with SpIOMM (Sébastian Lavoie)

Lots of discussion at the workshop about how FTS works with absorption lines. Enemy of absorption lines is distributed noise. Continuum sources has most information near ZPD; emission sources appear at many more steps in the interferogram. (Also avoid emission lines in your bandpass.)

How to boost S/N of absorption line: narrower filter! (minimize photo noise from continuum). Doing so gives you higher spectral resolution too! Or longer exposure with same filter; problem is that you will ultimately saturate the CCD.

M87 with SpIOMM. Lots of globular clusters! Impressive Na absorption line strength gradient. More modulation in the V interferogram helps with noise. Pick out core filaments.

****

# Tuesday Morning

## Abell 1882: Kpc-scale spatially resolved star formation in a z=0.14 proto-cluster (Glenn Morrison)

**Is large scale structure driving galaxy evolution?** Groups in isolation have SFR 30% higher than cluster but 30% lower than field (Bai 2010). Even in dense groups, SF fraction in groups higher than in cluster outskirts. Preprocessing of galaxies in group environments is not sufficient to explain lower SF fraction in clusters.

Lots of panchromatic data, including MegaCam (Elixir-LSB), WIRCam, Radio continuum, Spitzer and Hectospec, GALEX and more...

Three groups, each separated by about 1.2--1.6 Mpc. Most 24µm emission outside dense areas.

Caustics! See infall velocities. Nearest-neighbour clustering; looking for filament structures.

Elbaz 2007; 2011: *Main Sequence of Star Formation*. Galaxy mass vs. star formation rate. Classify passive, main sequence and star bursting galaxies. Starbursting galaxies smaller than  10^9.5 solar mass; main seq are bigger, passive even more massive. Main seq. pop is disk, have gas still. Morphologies make sense.

Star forming galaxies are smoother than expected: not clumpy as you'd expect from HII regions. Pre-processing going on???

1882 is very much like the field (briefly said).

SITELLE: even with 2x2 binning can spatially sample individual galaxies in the system extremely well.



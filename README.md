# NASA Exoplanet Archive Notes

## Goal:
"As of April 2025, over 5,867 exoplanets have been confirmed across 4,341 planetary systems discovered. However, there are only about 150 exoplanets (2-3% of all) from which we have obtained atmospheric data. About 217 exoplanets are confirmed to be terrestrial systems like our Earth. https://science.nasa.gov/exoplanets/discoveries-dashboard/

Our project this summer is to download, visualize and analyze current exoplanet dataset, identifying patterns that would indicate systematic trends, and reason these trends using statistical tools. We will relate terrestrial exoplanets to factors such as the host star mass, metallicity, activity levels, and disk characteristics which can significantly influence the occurrence and characteristics of terrestrial exoplanets. Low-mass stars with moderate metallicities and stable environments are particularly favorable for forming rocky planets that might support life. Understanding these relationships is crucial for identifying habitable worlds in future surveys.

In this project, you will learn how to work with exoplanet datasets from NASA, perform data visualization & analysis using python, and discover systematic trends & validating these trends to confirm/refute various hypotheses on terrestrial exoplanet formation theories."

## Terms:

### Planetary System
Host Name: Refers to the star system the planet is in (may have any number of stars or planets)

Default Parameter Set: Considered the most accurate of the parameter sets for this exoplanet

Solution Type: Presumable if this set has been confirmed as an actual exoplanet.

Controversial Flag: If confirmation status of planet is quesetioned in publication

Planetary/Stellar/System Parameter Reference: Reference used

Discovery Year (disc_year): Year exoplanet was discovered

#### Planet terms
(high density suggests a rocky composition)
(Terrastrial exoplanets have recorded 0.03-14 Earth densities)

Orbital Period (pl_orbper): Days to make complete orbit around host star (Essentially the planet's year length)

Orbit Semi-Major Axis (pl_orbsmax): Longest radius of eliptic orbit

Epoch of Periastron (pl_orbtper): Exact time planet is at periastron (closest to its star)

Argument of Periastron (pl_orblper): Angle between orbit's ascending node (switches from south the north hemisphere) and periastron ("longitude")

Projected Obliquity (pl_projobliq): tilt of planet's orbital axis relative to star's rotation axis, in the plane of the sky

True Obliquity (pl_trueobliq): The actual angle between orbital axis and star's rotation axis, requiring additional info

Planet Radius (pl_rade): length from center to surface.

Planet Mass (pl_bmasse): Best planet mass estimate available

Planet Density (pl_dens): Density of planet

Eccentricity (pl_orbeccen): Deviation from a perfect circular orbit

Insolation Flux (pl_insol): equilibrium temperature in units relative to those for the earth from the sun

Equilibrium Temperature (pl_eqt): Assumes the planet is completely black and only heated by its host star

Transit Duration (pl_trandur): total time it takes for exoplanet to fully pass in front of its star from Earth perspective (an "eclipse")

Transit Midpoint (pl_tranmid): point when exoplanet is in middle of transit

Transit Depth (pl_trandep): Fraction of star's light blocked by exoplanet during transit

Impact Parameter (pl_imppar): How close to the center of its star a planet crosses during transit

Occulation Depth (pl_accdep): Amoutn of light blocked when exoplanet passes behind its star (and the exoplanet doens't contribute to system brightness)

Radial Velocity Amplitude (pl_rvamp): Maximum change in star's velocity due to exoplanet's interference

#### Stellar Terms
Among types of stars, M-dwarfs are small enough but tend to be unstable. G-dwarfs like our sun have shorter lifespans and don't often form good planets, but they do work. K-dwarfs are a good in-between. (Want low mass stars, typically, 0.1-1.5 Sun masses and 0.1-1.5 Sun radiuses)

Stellar Effective Temperature (st_teff): temperature of a star, assuming black body emitting same total electromagnetic radiation (Look for 2300-6000 K)

Stellar Radius (st_rad): length from center to surface.

Stellar Mass (st_mass): star's mass

Stellar Density (st_dens): star's density

Stellar Surface Gravity (st_logg): gravitational acceleration at star's surface, using log(earth gravity)

Stellar Age (st_age): Age of host star

Stellar Rotational Period (st_ rotp): times it takes for star to complete 1 revolution

Stellar Rotational Velocity (st_vsin): how fast a star spins multiplied by sine of inclination

Stellar Radial Velocity (st_radv): how fast the host star moves toward or away from Earth

Stellar Metallicitty (st_met): Metal content of star compared to hydrogen (Want moderalte metallicity, around -0.02 to 0.02 dex)

Stellar Luminosity (st_lum): Total energy star emits per unit time (power output)

#### Star System Terms

RA: Right Ascension, basically longitude

Dec: Declination, basically latitude

Parallax (sy_plx): Apparent shift in position of system when viewed from another point in Earth's orbit

Distance from Earth (sy_dist): Distance from earth to Exoplanet system

Note for below: The following entries measure the brightness of the exoplanet's host star using certain light filters.

Effective Wavelength Midpoint (EWM) is the wavelength wehre the filter is most sensitive, and is listed as well. The filters below are sorted from lowest to highest EWM; the lower values are ultraviolet and blue filters that are better for broad atmospheric data, while higher values are red and help detect heat signatures and surface details.

Multiple surveys were used:
* Johnson is a traditional optical photometric system covering the ultraviolet to visible range. Cousins is an extension that focuses on red and infrared.
* The Sloan Digital Sky Survey uses a wide variety of filters optimized for galaxy surveys and stellar classification. 
* The Two Micron All-Sky Survay (2MASS) focuses on the near-infrared band.
* The Wide-field Infrared Survey Explorer (WISE) uses mid-infrared light to study star formation, galaxies, and planetary disks.
* Gaia was a space observatory that used broadband filters to measure stellar positions, parallaxes, and motions.
* The Kepler Space Telescope used a broadband, red and visual-centered filter to detect exoplanets.
* The Transiting Exoplanet Survey Satellite (TESS) is a space telecope that uses a broadband filter centered on the very near-infrared to detect exoplanet transits.

u (Sloan) Magnitude (sy_umag): Brightness of host star measured using the Sloan survey's u band (~354 nm) 

B (Johnson) Magnitude (sy_bmag): Brightness of host star measured using the Johnson system's Blue band (~442 nm) 

g (Sloan) Magnitude (sy_gmag): Brightness of host star measured using the Sloan survey's g band (~475 nm)

V (Johnson) Magnitude (sy_vmag): Brightness of host star measured using Johnson system's Visual band (~540 nm)

Kepler Magnitude (sy_kepmag): Brightness of host star measured using Kepler's bandpass (~600 μm) 

r (Sloan) Magnitude (sy_rmag): Brightness of host star measured using the Sloan survey's r band (~622 nm)

Gaia Magnitude (sy_gaiamag): Brightness of host star measured using Gaia's band (~673 nm)

i (Sloan) Magnitude (sy_imag): Brightness of host star measured using the Sloan survey's i band (~763 nm)

I (Cousins) Magnitude (sy_vmag): Brightness of host star measured using Cousins system's Infrared band (~786.5 nm)

TESS Magnitude (sy_tmag): Brightness of host star measured using TESS's bandpass (~800 nm) 

z (Sloan) Magnitude (sy_zmag): Brightness of host star measured using the Sloan survey's z band (~905 nm)

J (2MASS) Magnitude (sy_jmag): Brightness of host star measured using 2MASS's J band (~1.25 μm) 

H (2MASS) Magnitude (sy_hmag): Brightness of host star measured using 2MASS's H band (~1.65 μm) 

Ks (2MASS) Magnitude (sy_kmag): Brightness of host star measured using 2MASS's Ks band (~2.15 μm)

W1 (WISE) Magnitude (sy_w1mag): Brightness of host star measured using WISE's ~3.4 μm band 

W2 (WISE) Magnitude (sy_w2mag): Brightness of host star measured using WISE's ~4.6 μm band

W3 (WISE) Magnitude (sy_w3mag): Brightness of host star measured using WISE's ~12 μm band

W4 (WISE) Magnitude (sy_w4mag): Brightness of host star measured using WISE's ~22 μm band
### Microlensing
When a foreground object (lens) passes in front of a distant star, its gravity warps space-time and causes the star to appear brighter, as the light is focused towards earth. This can reveal objects that don't emit much light.
It works better on cold, distant and/or smaller planets, such as those not bound to a star. However, it can't estimate the radius or allow atmospheric analysis.

RA, DEC

Planet-star Projected SEmi-major axis: Projected physical separation of planet and host star in plane of sky at time of event

Lens Mass: Host star mass

Lens vs source distance: The Lens is a large object that bends light from a distant object due to its gravitational field. The source is the background object emitting the light. 

Time of Lens-source Minimum Separation: in the plane of the sky

Normalized Lens-source Minimum Separation: Normalized to angluar Einstein radius


Einstein crossing time: Time for lens-source separation to change by one Einstein radius

Normalized Source Angular Radius: Ratio of angular source star radius to Einstein radius

Instantaneous Planet-star Projected and Normalized Separation: Projected separation of planet and host star in plane of the sky at tiem of event, normalized to Einstein radius

Source Trajectory-lens Axis Angle: Angle of source system trajectory relative to lens system axis

Source I-Band: Brightness of unmagnified source star

Blend I-Band: Brightness of all objects excluding source star, superposed at time of event

Angular Einstein radius: the angular radius of the Einstein ring, a circular image of the background source created when the lens is perfectly aligned between the observer and the source

Lens-source Relative Proper Motion: mas/year

Default Model: If the microlens model is the default; bestfit model

### Transit:
When an exoplanet passes between its host star and our planet, it temporarily blocks some of the star's light. Through study of this dip in brightness, we can determine:
* the planet's size from the depth of the brightness dip
* the orbital period from how the time between transits
* The atmospheric composition from atmospheric spectroscopy.

More likely to find a habitable, Earth-like planet.

Inclination: Angle of plane of orbit relative to plane parpendicular to line of sight from Earth to object

Time of Conjuction (Transit Midpoint): Average of time planet starts and finishes crossing stellar limb

Impact Parameter: sky-projected distance between center of stellar disc and center of planet disc at conjunction, normalized by stellar radius

Transit Depth: Size of relative flux decrement caused by orbiting body transiting in front of the star

Transit Duration: Time it takes for planet to cross the stellar limb

Ratio of Semi-Major Axis to Stellar Radius: Distance between planet and star at mid-transit / stellar radius. If no eccentricity, the distance is the semi-major axis of planetary orbit

Ratio of Planet to Stellar Ratius: planet/stellar radius

Data show Transit Timing Variations: The gravity of another planet in the system can cause the expected timing of a planet's transit across its star to shift slightly. It caan be used to infer the presence of additional planets and their masses.

### Atmospheric Spectroscopy

When an exoplanet receives light, either from its star (transit) or from direct imaging, the gases in the atmosphere absorb certain wavelengths.

Atmospheric spectra can be used to indentify gases in atmosphere this way. Terrastrial exoplanet atmospheres will likely contain the following gases:
* Water vapor (1.4, 1.9, and 2.7 µm (infrared), plus some mid-infrared (~6 µm))
* Carbon dioxide (4.3 and 15 µm (mid and thermal infrared))
* Nitrogen (1200 nm (infrared) and 1134 Å (ultraviolet), plus some 3955–5007 Å)
* possibly Oxygen (760, 688, and 628 nm (A, B, and γ-bands))
* possibly Ozone (ultraviolet (~250 nm Hartley band) and infrared (~9.6 µm)) 
* possibly Methane (1.65, 2.3, and 3.3 µm (near-mid infrared))

Min/Max Wavelength: (microns) ???

Min/Max OBS Date: If from a single epoc, the date/time of observation for above, if from multiple transits, first (smallest)/last (largest) date

### Precursor Science Stars:
Ideal Conditions for Dust Disk:
* Young age (1-10 mil years)
* Sufficient gas and dust
* Low UV radiation
* Gravitational Stability
* Collisional Activity



B-V (Johnson) Color: Color of the stars as measured by the difference between B and V bands (lower values are O-type while higher is M-type. Sun's is ~0.65)

R (Cousins) Magnitude: Apparent Rc magnitude (600-700 nm, center ~658 nm, red optical range, absorbed by O3, O2, H2O, and CO2 at a weaker rate)

Stellar Luminosity: The amount of energy emitted by a star per unit time, measured as a logarithm of the value in units of solar luminosities.

Stellar Angular Diameter: Basically how big it looks in the sky. Measured in units of milliarcseconds

Stellar Radius and Mass are self-explanatory

Stellar Ca II Chromospheric Activity Index: Activity index is a measure of the emission-line cores of the Ca II H and K lines (centered at 3968.47 Å and 3933.66 Å)

Earth Equivalent Insolation Difference: Amount of sunlight a planet receives from the star relative to earth

Earth Equivalent Planet-Star Ratio: Planet-star brightness ratio for hypothetical Earth twin at quadrature (for flat albedo between 0.5–1µm)

Earth Equivalent R (Cousins) Magnitude: Apparent Rc magnitude Cousins photometric system for hypothetical Earth twin at quadrature (600-700 nm, center 658 nm, red optical filter)

Orbital Period at EEID: Orbital period where irradiance equals that of Earth from the Sun, in days

Earth-Equivalent Radial Velocity Amplitude: Radial velocity amplitude of star perturbed by hypothetical Earth twin at EEID, in cm/s

Earth-Equivalent Astrometric Amplitude: Astrometric amplitude of star perturbed by hypothetical Earth twin at EEID, in uas

WDS Designation: WDS (Washington Double Star) Catalog designation (For the binary+ star system)

WDS Component: WDS (Washington Double Star) Catalog Component ID (letter) (for the individual star)

WDS Separation: WDS (Washington Double Star) Catalog separation (arcsecs) (between stars in the system)

WDS Delta Mag: WDS (Washington Double Star) Catalog Delta Magnitude (mag) (difference in brightness)

Disks Flag: Flag indicating if star has an infrared excess indicative of a dust disk, as measured by IRAS, Spitzer, Herschel, WISE, or LBTI (Y=yes, N=no).

Target Group: HWO (Habitable Worlds Observatory) Selection Tier group for target star (A, B, C)

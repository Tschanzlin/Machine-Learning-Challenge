# Machine-Learning-Challenge
- For this challenge, I'm going to try to use five models to predict whether an unclassified planet ("Candidate") is likley to be classified as "Confirmed" or "False Positive".
- Potential models include:
-- Linear Regression
-- Logistic Regression
-- KNN
-- Support Vector Machine
-- Neural Netwok

## Data Review and Cleaning
- After reviewing the data, potential planets were classified as Candidate, False Positive, or Confirmed.  For this analysis, I am splitting the dataset into a "Candidate" data set and an "Identified" dataset.  Identified will include the Confirmed and False Positive planets.  I'll model and fit on the "Identified" dataset to create a model which will determine whether a planet was Confirmed or False Positive.  I'll then run on the "Candidate" dataset to classify those planets.
- After reviewing the column definitions, I decided to remove the error measurements from each datafield and just go with the actual measurements themselves.  There are 40 total data columns, excluding the planet classification.   By eliminating the error data, the total columns are reduced by half to 20 column, which would seem to be more manageable for the initial data modeling and training.


## CSV File Column Labels and Definitions (note:  error columns are not referenced below)

- KOI - Kepler Object of Interest.  A KOI is a target identified by the Kepler Project that displays at least one transit-like sequence within Kepler time-series photometry that appears to be of astrophysical origin and initially consistent with a planetary transit hypothesis. A KOI name has an integer and a decimal part of the format KNNNNN.DD. The integer part designates the target star; the two-digit decimal part identifies a unique transiting object associated with that star.

## Project Disposition Columns:

- koi_disposition:  The pipeline flag that designates the most probable physical explanation of the KOI. Typical values are FALSE POSITIVE, NOT DISPOSITIONED, and CANDIDATE. 

- koi_fpflag_nt:  A KOI whose light curve is not consistent with that of a transiting planet. This includes, but is not limited to, instrumental artifacts, non-eclipsing variable stars, and spurious (very low SNR) detections.

- koi_fpflag_ss:  A KOI that is observed to have a significant secondary event, transit shape, or out-of-eclipse variability, which indicates that the transit-like event is most likely caused by an eclipsing binary. However, self-luminous, hot Jupiters with a visible secondary eclipse will also have this flag set, but with a disposition of PC.

- koi_fpflag_co:  The source of the signal is from a nearby star, as inferred by measuring the centroid location of the image both in and out of transit, or by the strength of the transit signal in the target's outer (halo) pixels as compared to the transit signal from the pixels in the optimal (or core) aperture.

- koi_fpflag_ec:  The KOI shares the same period and epoch as another object and is judged to be the result of flux contamination in the aperture or electronic crosstalk.

## Transit Properties:

- koi_period:  The interval between consecutive planetary transits.

- koi_period_err1:

- koi_period_err2:

- koi_time0bk: The time corresponding to the center of the first detected transit in Barycentric Julian Day (BJD) minus a constant offset of 2,454,833.0 days. The offset corresponds to 12:00 on Jan 1, 2009 UTC.

- koi_time0bk_err1:

- koi_time0bk_err2:

- koi_impact:  The sky-projected distance between the center of the stellar disc and the center of the planet disc at conjunction, normalized by the stellar radius.

- koi_impact_err1:

- koi_impact_err2:

- koi_duration:  The duration of the observed transits. Duration is measured from first contact between the planet and star until last contact. Contact times are typically computed from a best-fit model produced by a Mandel-Agol (2002) model fit to a multi-quarter Kepler light curve, assuming a linear orbital ephemeris.

- koi_duration_err1:

- koi_duration_err2:

- koi_depth:  The fraction of stellar flux lost at the minimum of the planetary transit. Transit depths are typically computed from a best-fit model produced by a Mandel-Agol (2002) model fit to a multi-quarter Kepler light curve, assuming a linear orbital ephemeris.

- koi_depth_err1:

- koi_depth_err2:

- koi_prad:  The radius of the planet. Planetary radius is the product of the planet star radius ratio and the stellar radius.

- koi_prad_err1:

- koi_prad_err2:

- koi_teq:  Approximation for the temperature of the planet. The calculation of equilibrium temperature assumes a) thermodynamic equilibrium between the incident stellar flux and the radiated heat from the planet, b) a Bond albedo (the fraction of total power incident upon the planet scattered back into space) of 0.3, c) the planet and star are blackbodies, and d) the heat is evenly distributed between the day and night sides of the planet.

- koi_insol:  Insolation flux is another way to give the equilibrium temperature. It depends on the stellar parameters (specifically the stellar radius and temperature), and on the semi-major axis of the planet. It's given in units relative to those measured for the Earth from the Sun.

- koi_insol_err1:

- koi_insol_err2:

## Threshold Crossing Event Information - 

- koi_model_snr:  Transit depth normalized by the mean uncertainty in the flux during the transits.

- koi_tce_plnt_num:  TCE Planet Number federated to the KOI.

## Stellar Parameters

- koi_steff:  The photospheric temperature of the star.

- koi_steff_err1:

- koi_steff_err2:

- koi_slogg:  The base-10 logarithm of the acceleration due to gravity at the surface of the star.

- koi_slogg_err1:

- koi_slogg_err2:

- koi_srad:  The photospheric radius of the star

- koi_srad_err1:

- koi_srad_err2:

## KIC Parameters -- Kepler Input Catalog (KIC) is a catalog containing photometric and physical data for sources in the Kepler mission field of view; it is used by the mission to select optimal targets.

- ra:  KIC Right Ascension

- dec:  KIC Declination

- koi_kepmag:  Kepler-band (mag)








Data Source:  NASA Expolanet Archive
https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html


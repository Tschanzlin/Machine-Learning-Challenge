# Machine-Learning-Challenge



## Review data and determine relevant fields
## Nomenclature:
- KOI - Kepler Object of Interest.  A KOI is a target identified by the Kepler Project that displays at least one transit-like sequence within Kepler time-series photometry that appears to be of astrophysical origin and initially consistent with a planetary transit hypothesis. A KOI name has an integer and a decimal part of the format KNNNNN.DD. The integer part designates the target star; the two-digit decimal part identifies a unique transiting object associated with that star.

- koi_disposition:  The pipeline flag that designates the most probable physical explanation of the KOI. Typical values are FALSE POSITIVE, NOT DISPOSITIONED, and CANDIDATE. 

- koi_fpflag_nt:  A KOI whose light curve is not consistent with that of a transiting planet. This includes, but is not limited to, instrumental artifacts, non-eclipsing variable stars, and spurious (very low SNR) detections.
# koi_fpflag_ss:

- koi_fpflag_co:  The source of the signal is from a nearby star, as inferred by measuring the centroid location of the image both in and out of transit, or by the strength of the transit signal in the target's outer (halo) pixels as compared to the transit signal from the pixels in the optimal (or core) aperture.

# koi_fpflag_ec:  The KOI shares the same period and epoch as another object and is judged to be the result of flux contamination in the aperture or electronic crosstalk.

# koi_period:  The interval between consecutive planetary transits.

# koi_period_err1:

# koi_period_err2:

# koi_time0bk: The time corresponding to the center of the first detected transit in Barycentric Julian Day (BJD) minus a constant offset of 2,454,833.0 days. The offset corresponds to 12:00 on Jan 1, 2009 UTC.

# koi_time0bk_err1:

# koi_time0bk_err2:

# koi_impact:  The sky-projected distance between the center of the stellar disc and the center of the planet disc at conjunction, normalized by the stellar radius.

# koi_impact_err1:

# koi_impact_err2:

# koi_duration:

koi_duration_err1:

koi_duration_err2:

koi_depth:

koi_depth_err1:

koi_depth_err2:

koi_prad:

koi_prad_err1:

koi_prad_err2:

koi_teq:

koi_insol:

koi_insol_err1:

koi_insol_err2:

koi_model_snr:

koi_tce_plnt_num:

koi_steff:

koi_steff_err1:

koi_steff_err2:

koi_slogg:

koi_slogg_err1:

koi_slogg_err2:

koi_srad:

koi_srad_err1:

koi_srad_err2:

ra:

dec:

koi_kepmag:








Data Source:  NASA Expolanet Archive
https://exoplanetarchive.ipac.caltech.edu/docs/API_kepcandidate_columns.html


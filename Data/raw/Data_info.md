# CANDELS EGS Data Overview

This document summarizes the data available in the CANDELS EGS stellar mass, photometric redshift, and physical properties catalogs.

## Stellar Mass

| Column Name      | Measurement Description | Further Considerations |
|-----------------|-------------------------|------------------------|
| ID              | Sequential ID number in the F160W-based SExtractor catalog | Unique identifier for each detected object |
| RAdeg          | Right Ascension (J2000) in the F160W mosaic | Position of the object in the sky |
| DECdeg         | Declination (J2000) in the F160W mosaic | Position of the object in the sky |
| Hmag           | Magnitude in the F160W band | Measures brightness in the near-infrared |
| PhotFlag       | Flag in the photometric catalog | Identifies issues or special cases in photometry |
| Class_star     | SExtractor CLASS STAR parameter | Determines whether the object is a star or a galaxy |
| AGNflag        | Match in the Nandra et al. (2015) catalog (1=yes, 0=no) | Indicates presence of an active galactic nucleus |
| zphot          | Photometric redshift measurement | Estimated redshift based on multi-band photometry |
| zspec          | Spectroscopic redshift from the DEEP3 catalog | More accurate redshift measurement using spectral lines |
| q_zspec        | Quality flag for the spectroscopic redshift (1=Good, 2=Fair, 3=Poor) | Indicates reliability of spectroscopic redshift |
| zbest          | Best redshift measurement, prioritizing spectroscopic over photometric | Combines best available redshift estimate |
| M_neb_med      | Stellar mass measurement considering nebular emission | Accounts for ionized gas contribution to mass estimates |
| s_neb_med      | Uncertainty in M_neb_med | Measurement error due to model assumptions |
| M_med          | Stellar mass measurement without nebular emission | Mass estimate excluding ionized gas effects |
| s_med          | Uncertainty in M_med | Measurement error due to model assumptions |

## Photometric Redshift

| Column Name       | Measurement Description | Further Considerations |
|------------------|-------------------------|------------------------|
| ID               | Object ID from CANDELS photometry catalog | Unique identifier for each detected object |
| RA              | Right Ascension (J2000) | Position of the object in the sky |
| DEC             | Declination (J2000) | Position of the object in the sky |
| z_best          | Best estimate of redshift (prioritizing spec-z, grism-z, then phot-z) | Indicates the object's distance and lookback time |
| z_best_type     | Type of best redshift (s=spec, g=grism, p=phot) | Source of the redshift determination |
| z_spec          | Spectroscopic redshift if available | More accurate redshift measurement using spectral lines |
| z_spec_ref      | Reference catalog for spectroscopic redshift | Indicates the dataset used for spec-z |
| z_grism         | 3D-HST grism redshift if available | Intermediate accuracy redshift from grism spectroscopy |
| mFDa4_z_peak    | Redshift where photo-z probability distribution peaks | Most probable photometric redshift |
| mFDa4_z_weight  | Weighted centroid of the probability distribution | Represents the expected value of redshift |
| HB4_z_peak      | Redshift peak from hierarchical Bayesian method | Statistical peak redshift using Bayesian approach |
| HB4_z_weight    | Weighted centroid from hierarchical Bayesian method | More robust redshift estimate using multiple priors |
| z683_low/high   | 68.3% credible interval for the redshift | Uncertainty range covering 68.3% probability |
| z954_low/high   | 95.4% credible interval for the redshift | Uncertainty range covering 95.4% probability |

## Physical Properties

| Column Name      | Measurement Description | Further Considerations |
|-----------------|-------------------------|------------------------|
| Age            | Logarithm of stellar age in years | Measures the time since star formation |
| tau            | Star formation timescale in Gyr | Characterizes the duration of star formation |
| Av             | Dust extinction in magnitudes | Indicates the amount of light absorbed by dust |
| SFR            | Star formation rate in solar masses per year | Measures how actively stars are forming |
| Gas Metallicity | Metallicity of gas, normalized to solar values | Indicates chemical enrichment of the galaxy |
| Extinction Law | Calzetti (1) or Small Magellanic Cloud (2) | Describes how dust absorbs/scatters light |
| Reduced chi^2  | Goodness-of-fit statistic | Evaluates the reliability of model fitting |
| Lnu(1400A)     | Rest-frame luminosity at 1400 Angstrom (erg/s/Hz) | Indicates UV emission, related to young stars |
| Lnu(2700A)     | Rest-frame luminosity at 2700 Angstrom (erg/s/Hz) | Measures UV-optical emission from stars |
| U, B, V, R, I, J, K | Rest-frame magnitudes in the AB system | Represents intrinsic brightness in different bands |




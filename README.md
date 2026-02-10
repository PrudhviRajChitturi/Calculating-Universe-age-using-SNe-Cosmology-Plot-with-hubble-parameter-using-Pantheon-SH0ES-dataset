# Calculating Universe age using SNe Cosmology Plot with hubble parameter using Pantheon+SH0ES dataset

This project analyzes observational data from the Pantheon+SH0ES dataset to measure fundamental cosmological parameters, specifically the Hubble constant ($H_0$) and the matter density of the universe ($\Omega_m$). By fitting Type Ia supernovae data to a cosmological model, the project provides an estimate for the age of the universe and explores the relationship between distance and redshift.

Developed as part of the **India Space Academy Summer School Project** by **Prudhvi Raj Ch.**

## 🚀 Overview

Type Ia Supernovae (SNe Ia) act as "standardizable candles," making them essential for measuring cosmic distances across the universe.

**Key Features of this Analysis:**

- **Hubble Diagram Construction:** Mapping distance modulus ($\mu$) against redshift ($z$).
- **Model Fitting:** Utilizing scipy.optimize.curve_fit to derive the best-fit values for $H_0$ and $\Omega_m$.
- **Cosmological Calculations:** Implementing the $\Lambda$CDM model luminosity distance equations.
- **Residual Analysis:** Assessing model accuracy and observing deviations from the linear Hubble Law.
- **Redshift Comparison:** Comparing $H_0$ results across low-redshift (low-z) and high-redshift (high-z) samples to observe consistency.

## 📂 Dataset

The project utilizes the **Pantheon+SH0ES** sample, which is a state-of-the-art collection of calibrated SNe Ia.

- **Data Source:** The analysis primarily uses zHD (Hubble diagram redshift), MU_SH0ES (calibrated distance modulus), and MU_SH0ES_ERR_DIAG (statistical uncertainties).
- The raw data is typically sourced from the [Pantheon+ Data Release](https://github.com/PantheonPlusSH0ES/DataRelease).

## 📦 Setup and Requirements

The analysis is performed in Python. To run the notebook, ensure you have the following libraries installed:

```bash
pip install numpy pandas matplotlib scipy astropy
```

**Core Libraries:**

- **NumPy & Pandas:** Data manipulation and numerical operations.
- **Matplotlib:** Generating the Hubble diagram and residual plots.
- **SciPy:** curve_fit for non-linear regression and quad for numerical integration of the distance-redshift relation.
- **Astropy:** Handling physical constants (like the speed of light) and astronomical unit conversions.

## 🛠️ Implementation Details

- Luminosity Distance: Defining the integral for $d_L(z)$ in a flat $\Lambda$CDM universe.
- **Distance Modulus:** Converting luminosity distance to $\mu = 5 \log_{10}(d_L / 10pc)$.
- **Optimization:** Performing a chi-squared minimization to find the $H_0$ that best matches the Pantheon+ observations.
- **Age of the Universe:** Converting the derived $H_0$ into a time value (Gyr) using the Hubble Time relation.

## 📊 Results

The project generates:

- **The Hubble Diagram:** A plot showing the expansion of the universe over time.
- **Parameter Estimates:** Calculated values for $H_0$ (km/s/Mpc) and $\Omega_m$.
- **Sub-sample Analysis:** Comparisons showing how the Hubble constant behaves when calculated from different cosmic distances.

## 🧑‍💻 Author

Chitturi Prudhvi Raj
- **GitHub:**	https://github.com/PrudhviRajChitturi
- **LinkedIn:**	https://www.linkedin.com/in/prudhvi-raj-chitturi
- **📧Email:**	rprudhvi144@gmail.com

## **⚖License**
- This Project is MIT Licensed.

---
layout: page
title: "Study of Behaviors of Time-Varied SEDs emitted by BLRs around SMBBHs"
usemathjax: true
---
## 1.1 Overview

This project is intended to investigate the behaviors of time-dependent [Spectral Energy Distributions(SEDs)](https://en.wikipedia.org/wiki/Spectral_energy_distribution) of Broad Line Regions(BLRs) surrounding the Supermassive Binary Black Holes(SMBBHs). These behaviors may serve as unique features of SMBBHs, which may help us identify the SMBBHs for observation. 

## 1.2 Research Results

### 1.2.1 Raw data for SEDs

The data are all from [Eduardo et al. 2022](https://iopscience.iop.org/article/10.3847/1538-4357/ac56de). Here, I want to thank Eduardo and Manuela for providing the data.

These data shown here is about the total emission of the binary black hole system, including the circumbinary disk.

#### Spinning Binary Black Hole Simulation
![Spinning BBH](https://github.com/zj4050/zj4050.github.io/assets/99605082/78cf381c-ad2b-4423-b7dd-44dbd94f6e4b)
#### Spinless Binary Black Hole Simulation
![Spinless BBH](https://github.com/zj4050/zj4050.github.io/assets/99605082/fa760db5-a59f-4a96-bd66-25cf13615185)

### 1.2.2 BLR radius

We calculated the BLR radius by using the formula in the Section 7 of [Misty C. Bentz et al. (2013)](https://iopscience.iop.org/article/10.1088/0004-637X/767/2/149)

The formula is shown below:

$$\log\left({\frac{R_{BLR}}{1 \text{ lt-day}}}\right) = K + \alpha \log\left({\frac{\lambda L_{\lambda}}{10^{44} \text{ erg/s}}}\right)$$

, where $$K = 1.527$$ and $$\alpha = 0.533$$.
### 1.2.2 Binary-Black-Hole Models

We have built a list of models for the binary black holes for [CLOUDY](https://trac.nublado.org) to run simulation.

The below is from CLOUDY documentation "hazy1":
>CLOUDY is a photoionization code, designed to simulation physical conditions within clouds ranging from the intergalactic medium to high-density LTE and STE limits. It predicts the thermal, ionization, and chemical structure of a cloud which lies with these limits, and predicts its observed spectrum.

Here we used CLOUDY to simulation the spectrum emitted from BLRs around the SMBBHs.

The dataset of models we have here is listed below:

- Minimum luminosity with 1R<sub>BLR</sub>
- Minimum luminosity with 2R<sub>BLR</sub>
- Minimum luminosity with 4R<sub>BLR</sub>
- Time-averaged luminosity with 1R<sub>BLR</sub>
- Time-averaged luminosity with 2R<sub>BLR</sub>
- Time-averaged luminosity with 4R<sub>BLR</sub>
- Maximum luminosity with 1R<sub>BLR</sub>
- Maximum luminosity with 2R<sub>BLR</sub>
- Maximum luminosity with 4R<sub>BLR</sub>


The models for the spinning and spinless cases are the same. 

### 1.2.3 Ionization Parameters

The ionization parameteter is a measure of the ionizing structure of atoms, usually for hydrogen.

It has the expression as follows:

$$U = \frac{Q}{4\pi R_{BLR}^2 c n_H}$$

, where Q is the ionizing photons per second, c is the speed of light, R<sub>BLR</sub> is the radius of the BLR, and n<sub>H</sub> is the number density of the gas (assuming it is pure hydrogen).

#### Ionization parameters for each model


| Spinning Model                               | Ionization Parameter in log scale |
|----------------------------------------------|:---------------------------------:|
| Min_Luminosity_1R<sub>BLR</sub>              |          0.1857                   |
| Min_Luminosity_2R<sub>BLR</sub>              |          -0.4163                  |
| Min_Luminosity_4R<sub>BLR</sub>              |          -1.0184                  |
| Time-averaged_Luminosity_1R<sub>BLR</sub>    |          0.2909                   |
| Time-averaged_Luminosity_2R<sub>BLR</sub>    |          -0.3112                  |
| Time-averaged_Luminosity_4R<sub>BLR</sub>    |          -0.9132                  |
| Max_Luminosity_1R<sub>BLR</sub>              |          0.4473                   |
| Max_Luminosity_2R<sub>BLR</sub>              |          -0.1548                  |
| Max_Luminosity_4R<sub>BLR</sub>              |          -0.7569                  |


| Spinless Model                               | Ionization Parameter in log scale |
|----------------------------------------------|:---------------------------------:|
| Min_Luminosity_1R<sub>BLR</sub>              |          0.1437                   |
| Min_Luminosity_2R<sub>BLR</sub>              |          -0.4584                  |
| Min_Luminosity_4R<sub>BLR</sub>              |          -1.0604                  |
| Time-averaged_Luminosity_1R<sub>BLR</sub>    |          0.2251                   |
| Time-averaged_Luminosity_2R<sub>BLR</sub>    |          -0.3769                  |
| Time-averaged_Luminosity_4R<sub>BLR</sub>    |          -0.9790                  |
| Max_Luminosity_1R<sub>BLR</sub>              |          0.3969                   |
| Max_Luminosity_2R<sub>BLR</sub>              |          -0.2052                  |
| Max_Luminosity_4R<sub>BLR</sub>              |          -0.8072                  |
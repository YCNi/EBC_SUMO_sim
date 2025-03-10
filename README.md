# E-Bike City in SUMO
Ellen J. Fulton, Ying-Chuan Ni <br />
Traffic Engineering Group, Institute for Transport Planning and Systems, ETH Zurich

## Introduction
This repository contains the SUMO simulation package of the E-Bike CIty project using the city center of Zurich as the case study site. The network is deisgned by Ballo et al. (2024)*. In the four scenarios (morning/evening, fixed-time/actuated signal control) available here, 75% of the trips are shifted from cars to bicycles. Python codes which can produce average OD travel times and network fundamental diagrams (NFDs) are also provided.

*Ballo, L., Raubal, M., & Axhausen, K. W. (2024). Designing an E-Bike City: An automated process for network-wide multimodal road space reallocation. Journal of Cycling and Micromobility Research, 2, 100048.

## Instructions

### Required package
- sumo
- Python 3.1
- numpy
- pandas
- seaborn
- matplotlib

### Running simulation
There are four scenarios:
- 25_MIV_75_BIKE (modal share: 25% cars and 75% bicycles, morning 6-11, fixed-time signal control)
- 25_MIV_75_BIKE (modal share: 25% cars and 75% bicycles, morning 6-11, actuated signal control)
- e_25_MIV_75_BIKE (modal share: 25% cars and 75% bicycles, evening 15-20, fixed-time signal control)
- e_25_MIV_75_BIKE_actuated (modal share: 25% cars and 75% bicycles, evening 15-20, actuated signal control)

The simulation can be executed by simply running the .sumocfg files in the scenario folder. There are five .sumocfg files, representing five random seeds, in each folder. 

### Post-processing and visualization
The post-processing and visualization include the NFDs and average OD travel times. The analysis for NFDs is based on the lane-based method introduced in Leclercq et al. (2014). The aggregation interval is 5 minutes.<br />
The codes are available in .ipynb format.<br />
There are also alternative (simple) ways to output NFDs and travel times by using the SUMO E3 detectors, which will be provided soon.

*Leclercq, L., Chiabaut, N., & Trinquier, B. (2014). Macroscopic fundamental diagrams: A cross-comparison of estimation methods. Transportation Research Part B: Methodological, 62, 1-12.

## To cite
Fulton, E. J., Ni, Y. C., & Kouvelas, A. (2025). Impact of radical bike lane allocation on bi-modal urban network traffic performance: A simulation case study. SVT Working Papers. ETH Zurich.

## Note
The codes are now only available for the scenario 25_MIV_75_BIKE. For other scenarios, the same codes can be applied after modifying the file names in the codes.<br />
All the resources may still be constantly updated. You are strongly adviced to contact the author for instructions beforehand. For instance, the OD demand will be updated with a calibrated version soon.

## Contact information
For questions, please feel free to contact the author via email (ying-chuan.ni@ivt.baug.ethz.ch). Scheduling a video call is also possible upon requests.

## Acknowledgement
This work was supported by E-Bike City project in the Department of Civil, Environmental and Geomatics Engineering (D-BAUG) at ETH Zurich and funded by Swiss Federal Office of Energy (SFOE).

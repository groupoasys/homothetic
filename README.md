# Supplementary material of the work *Forecasting the Price-Response of a Pool of Buildings via Homothetic Inverse Optimization*

## Overview

In this repository, we provide supplementary information about the work entitled *Forecasting the Price-Response of a Pool of Buildings via Homothetic Inverse Optimization*:

- Mathematical formulation of an efficient data-driven two-step heuristic estimation procedure
- Database synthetically generated of a pool of smart buildings equipped with thermostatically-controlled loads

The paper can be accessed via arxiv in [[1]](https://arxiv.org/abs/2004.09819). This article has been developed by R. Fernandez-Blanco, J. M. Morales, and S. Pineda, which are members of the [OASYS group](https://sites.google.com/view/groupoasys/home), and it has been possible thanks to the funding of the project [Flexanalytics](https://groupoasysflexanalytics.readthedocs.io/en/latest/). We suggest you to visit the related links to know more our research. 


## Mathematical formulation

The proposed two-step heuristic estimation method is built upon the one proposed in [[2]](https://ieeexplore.ieee.org/document/7859377). However, the procedure has been substantially modified to account for the building thermal dynamics. This estimation process is made up of two linear problems: (i) the feasibility problem and (ii) the optimality problem. The respective formulations as well as the steps of the heuristic estimation approach are presented in the supplementary material found in this repository.

## Database

This repository also includes the data to synthetically generate the load for a pool of 100 buildings, as well as the input data for the proposed homothetic inverse optimization problem. To do that, we use problem (9) of the paper [[1]]. The input data for problem (9) is publicly available in the excel file *input_data_pool.xlsx*, where each of the excel sheets are explained below:  

- *theta_amb*: hourly ambient temperature is given for June, July and August of 2017 (in total 2208 periods) in Malaga, Spain. 
- *price*: Hourly electricity prices are taken from ENTSO-E for June, July and August in 2017.
- *omega_het01*: the technical parameters for the 100 buildings by using an heterogeneity factor of 10%. 
- *omega_het075*: the technical parameters for the 100 buildings by using an heterogeneity factor of 75%. 

After running problem (9), we obtain the results reported in the excel files *data_pool_heterogeneity_01.xlsx* and *data_pool_heterogeneity_075.xlsx*. In those files, we provide the following information: 

- *power*: the power of the cooling device per buildings in kW for 2208 hourly periods and 100 buildings.
- *theta*: the indoor air temperature for 2208 hourly periods and 100 buildings.
- *slack_theta*: the temperature outside the comfort bounds for 2208 hourly periods and 100 buildings. 

In this repository, we also provide the input data for the proposed approach *rnp*, which is also publicly available in the excel files *input_invfor_heterogeneity_01.xlsx* and *input_invfor_heterogeneity_075.xlsx* for the cases with 10% and 75% of heterogeneity among buildings, respectively.  Each excel sheet is explained below:  

- *regressors*: we have chosen as regressors the ambient temperature at hours h+2, h+1, h, h-1, and h-2 for 1848 hourly periods.
- *ObsPower*: the aggregate power of the pool of buildings in kW for 1848 hourly periods.
- *ObsTheta*: the ambient temperature for 1848 hourly periods.
- *price*: the electricity prices in €/kWh for 1848 hourly periods. 
- *initial_conditions*: the initial indoor air temperature of the ensemble for 77 days. 

## References

[1] Fernández-Blanco, R., Morales, J. M., & Pineda, S. (2020). Forecasting the Price-Response of a Pool of Buildings via Homothetic Inverse Optimization. arXiv preprint: https://arxiv.org/abs/2004.09819

[2] Saez-Gallego, J., & Morales, J. M. (2017). Short-term forecasting of price-responsive loads using inverse optimization. IEEE Transactions on Smart Grid, 9(5), 4805-4814. https://ieeexplore.ieee.org/document/7859377


 ## License
 
    Copyright 2019 Optimization and Analytics for Sustainable energY Systems (OASYS)

    Licensed under the GNU General Public License, Version 3 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.gnu.org/licenses/gpl-3.0.en.html

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
 

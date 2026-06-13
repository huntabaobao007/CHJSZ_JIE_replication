Readme file for the replication package of “Endogenous Mobility in Pandemics: Theory and Evidence from the United States” by Chen, Huang, Ju, Sun, and Zhang.

This document describes the data and programs for the paper “Endogenous Mobility in Pandemics: Theory and Evidence from the United States” by Chen, Huang, Ju, Sun, and Zhang. It is organized into three components:

	Component A (Empirics), contains the reduced-form analysis, which generates Figure 1 in Section 1 and the stylized facts in Section 2; and parameter estimation in Section 5. 

	Component B (Simulation) provides the code to conduct the simulation in Sections 4.

	Component C (Quantification) includes the code and data to perform the quantitative analysis in Section 5. 


Notes: Please change the directories to your local ones before running the code.

A. Empirics

For Figure 1 from Section 1 and stylized facts from Section 2, see the do file under path "~ \empirics\do ", with outputs saved under "~ \empirics\results". Please install the mapping tool “ssc install geo2xy” if it is not installed on your Stata.

Run "RegressionTables.do":

(1) Generate Figures 1, 2, and 3;
(2) Generate Tables 1, 2, and B4.

Run "ParameterEstimation.do" to estimate trade costs and mobility elasticity:

(1) Generate Tables B1, B6 and trade cost parameters.

B. Simulation

For simulation results from Section 4, see the m files under path "~\simulation\Code_Simulation".

Run "main.m":

(1) generates Figure 5 (simulation_dynamics_GE.eps) from the 4-region economy
(2) generates Figure B.4 (short_effect.eps) from the model with short-run mobility
C. Quantification

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

For calibration and baseline counterfactual results, see the m files under path "~\quantification\Benchmark".  

First, run "importdata_high.m":

(1) Generate Figure B.1 (a)(b) (productivity.eps; amenity.eps)
(2) Generate Figure B.3 (V_d_fitness.eps)
(3) Calibrate the mobility distance elasticity alpha_1 (stored in variable “para(2)”) and contiguity barrier alpha_2 (stored in variable “para(3)”)
(4) Calibrate the local containment policy elasticity nu (stored in variable “sol_chi(1)”)
(5) Calibrate the mobility containment policy elasticity eta (stored in variable “E_PolicyMob”)

Then, run "main_dynamics.m":

(1) Generate Figure B.2 (Population_fitness.eps)
(2) Generate Figure 6 (a)(b) (Infection_fitness-I.eps; Infection_state.eps)
(3) Generate Figure 7 (NewCaseRatio.eps)
(4) Generate Table 3

Notes: The welfare and health outcomes saved in the csv file Benchmark.csv
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

For robustness w.r.t. the discount rate beta, see the m files under path "~\quantification\Robust_beta". 

First, run "importdata_high.m" with beta evaluated at heading section
Then, run "main_dynamics.m" with beta evaluated at heading section:

(1) Generate panel (a) of Table B.7

Notes: The welfare and health outcomes saved in the csv file Counterfactual_RR_beta.csv
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

For robustness w.r.t. the inverse mobility elasticity kappa, see the m files under path "~\quantification\ Robust_kappa".

First, run "importdata_high.m" with kappa evaluated at heading section
Then, run "main_dynamics.m" with kappa evaluated at heading section:

(1) Generate panel (c) of Table B.7

Notes: The welfare and health outcomes saved in the csv file Counterfactual_RR_kappa.csv

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
For robustness w.r.t. the healthcare congestion effect, lambda, see the m files under path "~\quantification\Robust_lambda".

First, run "importdata_high.m"
Then, run "main_dynamics.m" with lambda evaluated at heading section:

(1) Generate panel (b) of Table B.7

Notes: The welfare and health outcomes saved in the csv file Counterfactual_RR_lambda.csv

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

For robustness w.r.t. with the trade elasticity theta=0.76, see the m files under path "~\quantification\Robust_theta0.76".

First, run "importdata_high.m" setting flag_theta=1
Then, run "main_dynamics.m":

(1) Generate panel (d) of Table B.7

Notes: The welfare and health outcomes saved in the csv file Counterfactual_RR_theta.csv


For robustness w.r.t. with the trade elasticity theta=2.84, see the m files under path "~\quantification\Robust_theta2.84".

First, run "importdata_high.m" setting flag_theta=2
Then, run "main_dynamics.m":

(1) Generate panel (e) of Table B.7
Notes: The welfare and health outcomes saved in the csv file Counterfactual_RR_theta.csv

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
For robustness w.r.t. the social cost of death, Vd, see the m files under path "~\quantification\Robust_Vd".

First, run "importdata_high.m"
Then, run "main_dynamics.m" with Vd evaluated at heading section:

(1) Generate panel (f) of Table B.7
Notes: The welfare and health outcomes saved in the csv file Counterfactual_RR_Vd.csv

I. Overview of directory contents

1. The directory contains two subdirectories:
   a. miscelleneous_analysis_codes: This contains all the codes that analyze simulation results.
   b. simulations: This contains the primary fortran codes to run simulations for various scenarios.

2. The simulations directory contains four subdirectories
   a.  system: This contains the code to run MC simulations with all the components - RNAPs, free and bound Nus, and the chromosome-polymer. 
   b.  phase_diag: This contains the codes to run MC simulations with only the free Nus proteins in absence of chromosome and RNAPs.
   c.  model_modification: This contains codes to run MC simulations with all components with one modification -Temporal fluctuations to the attractive interaction.
   d.  diff_constant_and_res_times: This contains codes to run MC simulations with all components with data printed more frequently so that the diffusion constants
       of Nus in the two phases may be calculated and the residence time in the dense phase may be calculated.

3.  The miscelleneous_analysis_codes contains all the analysis codes for most of the analysis presented in the paper.


II. Instructions to run analysis codes

    -The user may first run the simulations using the codes given in the simulations directory. The simulation files generates files which list the positions of all components corresponding to each        MCS. The positions are printed in files named as 'store_MCS-step'.For instance, the positions of all the components in iteration index-10000 will be listed in the file: store_10000.

    -Each of the 'store_MCS-step' file has the format: Label, X-coordinate, Y-coordinate, Z-coordinate. The label `O' denotes the coordinates of a monomer of the chromosome-polymer. 
    The label `Na' denotes the coordinate of a free Nus protein. The label `N' denotes the coordinate of a bound Nus protein. The label `C' denotes the coordinate of a bound Nus protein.

    -The analysis codes take these files as input to generate results.

    
III. Overview of Analysis Codes 

     - Inside the directory titled `miscelleneous_analysis_codes' we have the code titled 'nearest_neighbour_ensemble.f90' code. This code was used to generate the phase diagram in Fig.2 and the plot        presented in Fig.3b.
      
      - Inside the directory titled `miscelleneous_analysis_codes' we have another code titled 'cluster_analysis_detailed_ensemble.f90'. This code was used to generate the analyisis presented in              Fig.4a and 4b.

      - To replicate the analysis presented In Fig.6a, the user should run `operon_distribution_ensemble.f90'. To replicate the analysis presented in Fig.6b and 6c, run the code titled    `contact_map.f90'.


IV.  Additional Comments

      - To replicate the analysis presented In Fig.5a and 5b, the user must go to simulations/diff_constant_and res_times. First the main simulation code `main_simulation_code/llps_mc.f90' must be run. Thereafter, the code: `residence_time_analysis/residence_time_approach.f90' must be run to conduct the analysis presented in Fig.6a. To replicate the analysis presented in Fig.6b, run the codes `Diffusion_constant_analysis/diff_const_dilute2.f90' and  'Diffusion_constant_analysis/diff_constant_dense2.f90'. 

      - To replicate the analysis presented In Fig.7, the user must first run simulations by running the code simulations/model_modification/main_simulation/llps_mc.f90.
      - To conduct the analysis presented in Fig.7, the user must run the analysis codes in  simulations/model_modification/analysis_code.

      


    
         

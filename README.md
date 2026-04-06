I. Overview of directory contents

1. The directory contains two subdirectories:
   a. miscelleneous_analysis_codes: This contains all the codes that analyze simulation results.
   b. simulations: This contains the primary fortran codes to run simulations for various scenarios.

2. The simulations directory contains four subdirectories
   a.  system: This contains the codes to run MC simulations with all the components - RNAPs, free and bound Nus, and the chromosome-polymer. 
   b.  phase_diag: This contains the codes to run MC simulations with only the free Nus proteins in absence of chromosome and RNAPs.
   c.  model_modification: This contains codes to run MC simulations with all components with one modification -Temporal fluctuations to the attractive interaction.
   d.  diff_constant_and_res_times: This contains codes to run MC simulations with all components with data printed more frequently so that the diffusion constants
       of Nus in the two phases may be calculated and the residence time in the dense phase may be calculated.

3. The miscelleneous_analysis_codes contains all the analysis codes for all the analysis presented in the paper   

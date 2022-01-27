# Analysis code for Zhang et al. Environment symmetry drives a multidirectional code in rat retrosplenial cortex

the code packages contain 2 main functions: contest_v2 and egoTEST_v2

contest_v2  function for analysing directional cells in different environments (e.g.multicompartment maze, 2-box and 4-box)
- A function for analysing the context box (multicompartment maze) data. This uses an 'sdata' structure, produced by custom-built MATLAB code to analyze raw data (see https://www.nature.com/articles/s41467-020-14611-7).It can run on a single tetrode and cluster: contest(out_name,tetrodes,clusters).This function allows the user to specify the maze boundaries and trial order (e.g. trial a, b ... g) with this information we can divide data between the different compartments and compare tuning curves in this way. But the maze outline is also used later to analyse egocentric boundary tuning.

egoTEST_v2  function for analysing egocentric boundary tuning in different environments (e.g.multicompartment maze, 2-box and 4-box)
- This function should be run following contest_v2 (specifies maze frame/boundaries). This function mainly replicates the analysis reported in: Alexander et al. (2019) Egocentric boundary vector tuning of the retrosplenial cortex http://dx.doi.org/10.1101/702712 to test for egocentric boundary cell coding. Most of the analysis is placed in the sdata structure where it was analysed and plotted for publication using later functions.

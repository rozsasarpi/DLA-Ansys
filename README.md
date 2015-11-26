# Dynamic load analysis

Moving and fixed (steady state) dynamic load analysis with sinusoid exciting force (time history analysis)
per British Standard and Sétra recommendations

__Codes:__ Ansys APDL

__Usage__ 
* define element group under name 'moving_load_path' - contains the elements where the load will be applied
* adjust values inside the settings part
* moving_load_results


__Optional__ 
* (applies only for reduced analysis) define the node/element group under name 'moving_load_results' where results are needed (if not selected the nodes corresponding to 'moving_load_path' will be selected)
	

__Notes__  
* currently can handle only cases where the moving path runs in X direction (local coordinate system required otherwise) and loaded in Z direction
* in case of full transient analaysis the Rayleigh damping coefficients are calculated with the assumptions that the first two important (largest mass participation in excitation direction if mass_sort_freq=1) modes have the specified structural damping
* currently working only with line type load path (torsional modes..)
* the moving_load_path is used for mode shape extraction for BS -> later mode_line COMP
* -> later moving_load_area COMP 

__Other Ansys related repos:__
* [run Ansys in parallel batch mode using Matlab](https://github.com/rozsasarpi/Parallel-Ansys)
* [dynamic load analysis for bridges](https://github.com/rozsasarpi/DLA-Ansys)
* [construction stage analysis](https://github.com/rozsasarpi/CSA-Ansys)
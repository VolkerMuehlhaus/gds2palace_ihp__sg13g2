The *.py files are Python model code to create a simulation model from *.gds layout and *.xml technology stackup. Each *.py file creates one simulation model, or to be more excat: the files required to run the AWS Palace simulation. These output files will be created in a directory "palace_model" inside your current directory where you run the model.

The gds2palace folder contains the code modules required by this workflow. This directory must always be included in your current directory where you start the actual model code.

The *.xml files include the technology description with materials, layer mappings and physical location in the stackup. They look similar to the files used by IHP openEMS workflow, but might be slightly different in the details to enable special "tricks" for Palace.

The *.gds files are the layouts for these examples. They include port shapes on special layers (typically 201 and above) that are referenced by the simulation model code. Note that port shapes for this Palace workflow must be 2D sheets, so vertical via ports are created as zero width boxes in the xy plane. This makes it difficult to see them in the GDSII layout viewer.
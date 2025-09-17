# MetaNet Metaphor and Frame extraction

This project extracts metaphors and source/target frames from [MetaNet](https://metanet.arts.ubc.ca/).

## Prerequisites

You will need to install the [`owlrl`](https://owl-rl.readthedocs.io/en/latest/owlrl.html) Python module using `pip`. You will also need to download the RDF file, which is a representation of the MetaNet database. You can download it at [https://metanet.arts.ubc.ca/metaphor-databases/](https://metanet.arts.ubc.ca/metaphor-databases/). You also need `pandas`, but you probably have it installed already.

You don't have to use a virtual environment, but if you'd like to, there is a `requirements.txt` file provided so that you can install the required modules.

## Extracting data

Open the `meta-net_metaphors.ipynb` file in a Jupyter notebook. Then, find the `original_filename` variable and change it to the name of the RDF file you downloaded from MetaNet.

From there, you can simply run the notebook. It will first clean the input file for processing, and then produce the output files. These include:

`meta-net_metaphor_list.csv`: this is a table of metaphors and their corresponding source and target frames. Note that some metaphors don't have a source/target frame, which would be shown as `TBD`, `TBC`, or `?`. Additionally, some metaphors are considered to be a "supercategory" for which exist "subcategory" metaphors, or metaphors that are involved in entailment relationships. The source/target frames for the "supercategory" metaphors are completely blank. Currently, this file does not show these relationships between metaphors, but that might change in the future.

`meta-net_source_frames_list.csv`: this is a list of all the source frames used in the MetaNet database.

`meta-net_target_frames_list.csv`: this is a list of all the target frames used in the MetaNet database.

`meta-net_all_frames_list.csv`: this is a list of _all_ the frames used in the MetaNet database, both source and target.

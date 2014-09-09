# Mystic

An inferred biomass biogeochemical model of Mystic Lake. 

- by: Scott W Olesen (swo@mit.edu)
- development page: http://github.com/swo/mystic
- main page: http://almlab.mit.edu/mystic.html

## Dependencies

- Matlab (developed with version 8)
- Python (developed with version 2.7)

## Installation
    $ git clone http://github.com/almlab/mystic.git

## File structure
- `analysis/`: Tool for plotting timecourses and the profiles for rates and concs.
- `bin/`: Main matlab scripts.
- `simulation/`: Scripts for running the model with easily-adjustable parameters and displaying the output.
- `lake.cfg`: Configuration for the simulation.
- `README.md`: This file.

## Usage

### Interactive
To run the model,
- Update `lake.cfg` with the desired parameters.
- Under `simulation`, use `write_default_values_script.py` to create `run_interactive_defaults.m`, which supplies the values in `lake.cfg` to `interactive.m`.
- In Matlab, run `run_interactive.m`. This requires the `bin/` folder to be on Matlab's path. If running in the terminal, you can use the `set_matlab_path.py` script to do this.
- The output of the simulation is stored in `concs_history` and `rates_history` variables. You can write them to files using `bin/write_data_to_files.m`.

### Analysis
To make timecourses and end-time plots for all the rates and chemical concentrations, copy the desired `history.mat` data file to `analysis/` and run `analysis/profiles/pipeline.sh`.

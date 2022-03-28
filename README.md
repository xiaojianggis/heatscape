🚨🚨🚨 ***THIS README IS A PLACEHOLDER TO GET STARTED. PLEASE REPLACE WITH README DOCUMENTING YOUR SPECIFIC CASE STUDIES*** 🚨🚨🚨

# uDALES experiments

This repository is used as a template for setting up experiments in uDALES. By default, the uDALES experiments repository structure is as follows:

```sh
.
├── data        # Contains or links to any external data used by the experiments.
├── docs        # Relevant documentation or papers used for the experiment.
├── experiments # Configuration files grouped by experiment number.
│   └── 001     # Any configurations files needed by uDALES to run experiment 001.
│   └── 002     # Any configurations files needed by uDALES to run experiment 002.
│   └── ...
├── tools       # Additional or specialized tools other then the ones already included with uDALES.
└── u-dales     # uDALES model repository.

```

Any files (excluding uDALES output files) in `experiments` and `tools` directories are automatically tracked by Git by default. Files in `data` and `docs` as these should be downloaded using a download script. If you require to change these settings please customize your `.gitignore`.




## Usage

To run a simulation in uDALES using this experiment template, compile uDALES as per installation instructions and run the case study from your experiment folder.

```sh
# E.g. to compile u-DALES using defaults
mkdir u-dales/build && cd u-dales/build
cmake ..
make -j4
cd ../..

# E.g. to run a sample experiment
cd experiments/001
mpiexec -np 2 ../../u-dales/build/u-dales namoptions.001
```

## Copyright and license

Copyright 2019 D. Meyer. Licensed under MIT.
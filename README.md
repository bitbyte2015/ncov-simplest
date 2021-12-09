In order to run the analysis yourself, you need to `select all` on GISAID, `download` and then select `Input for the Augur pipeline`.

Put the downloaded `.tar` file into the `data` folder.

Install Conda from https://www.anaconda.com/products/individual

Create a new environment with `conda create -name ncov_simplest` and `conda activate ncov_simplest`

Install mamba `conda install mamba`

Install nextclade and augur `mamba install nextclade` and `mamba install python=3.9 augur`

Downgrade bcbio `mamba install bcbio-gff=0.6.7`

Then run Snakemake with `snakemake build -c0`.

The resulting `auspice.json` will be in the folder `auspice`.

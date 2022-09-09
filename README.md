# LLPSWise
computational prediction of biological liquid-liquid phase separation systems

https://www.biorxiv.org/content/10.1101/2022.07.25.501404v1

## Installation

`LLPSWise` requires several packages that have dependencies conflicts due to
differences in source and repository versions for those dependencies. Until, all
this is solved, installation requires some manual intervention.

1. install Anaconda
1. `conda create --name llpswise -c conda-forge python=3.10
1. `conda activate llpswise`
1. `conda env update --file requirements_free.yml`
1. `cd ..`
1. `git clone https://github.com/biopython/biopython`
1. `git clone https://github.com/ialbert/bio`
1. `cd biopython`
1. `python setup.py build`
1. `python setup.py install`
1. `cd ../bio`
1. `conda install -c conda-forge more-itertools requests tqdm`
1. `pip install mygene`
1. `python setup.py develop --no-deps`

## Collect data

1. Download PPI data（"BIOGRID-ORGANISM-Homo_sapiens-4.4.211.tab3.txt"） from biogrid

https://downloads.thebiogrid.org/BioGRID/Release-Archive/BIOGRID-4.4.211/

and change the path in `Code/main.py`.

3. start the query

`python Code/main.py --id [uniprotID]`

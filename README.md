# Installing Miniconda
Install Miniconda within an existing Linux environment (Ubuntu).

Retrieve the latest Miniconda
```console
$ wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

Generate the script to be executable.
```console
$ chmod +x Miniconda3-latest-Linux-x86_64.sh
```

Run the executable miniconda script.
```console
$ ./Miniconda3-latest-Linux-x86_64.sh
```

# Installing the right environment for Python automation in Miniconda
Install the nessesary channels if Bioconda has not been used before. 
```console
$ conda config --add channels defaults
$ conda config --add channels bioconda
$ conda config --add channels conda-forge
```
Intall git in Miniconda to clone this environment locally to your computer.

```console
conda install -c conda-forge git
```




Download the cytoscape.yml within this repository (

conda env create -f environment.yml

# Python automation tutorial


# Loading in the rsnumber-gene network in cytoscape for linking the wikipathway
Install cytargetlinker in the Cytoscape app (Apps > App Manager > search Cytargetlinker > install). Load in the generated csv file (readme file 1) with edges in cytoscape.


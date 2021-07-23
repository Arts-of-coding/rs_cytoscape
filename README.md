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
$ conda install -c conda-forge git
```

Clone the rs_cytoscape repository locally to your computer (at a directory of your choice: "dir").
```console
$ git clone https://github.com/Arts-of-coding/rs_cytoscape.git
```

Install all nessesary software packages by creating the cytoscape environment.
```console
$ conda env create -f dir/envs_yml/cytoscape.yml
```

Activate the cytoscape environment
```console
$ conda activate cytoscape
```

Installing jupyter lab extensions for using jupyter notebook.
```console
$ conda install -c anaconda python
```
```console
$ conda install -c conda-forge jupyterlab
```
Run jupyter notebook
```console
$ jupyter notebook
```

# Python automation tutorial
Run the project.ipynb in jupyter notebook.

# Linking the generated network to pathways in the Cytoscape app.
Download (https://cytoscape.org/download.html) and install Cytoscape (run the .exe file).

Install cytargetlinker in the Cytoscape app (Apps > App Manager > search Cytargetlinker > install). Load in the generated csv file (readme file 1) with edges in cytoscape.

Import the netowrk (Cytoscape > import Network from Filesystem). See image below for selecting the right settings.
![Networktable](https://user-images.githubusercontent.com/78762941/126752666-49366503-d30f-4fea-9714-48535d04cd6b.PNG)

Download the wikipathways dataset from https://cytargetlinker.github.io/pages/linksets/wikipathways and unzip the dataset on your system.

Extend the network (Cytoscape > apps > cytargetlinker > extend network). See image below for choosing the right settings.
![Choices](https://user-images.githubusercontent.com/78762941/126750932-95f7c9f6-6d50-4b14-b5e8-f67a4e0f8924.PNG)

Now the Ensembl genes are linked to the pathways and the final network is generated!

# Notes of interest
If the jupyter widgets do not show wihtin jupyter notebook then execute the following command within your activated cytoscape environment before restarting jupyter notebook:

```console
$ jupyter nbextension enable --py widgetsnbextension
```

### BASALT - Binning Across a Series of AssembLies Toolkit

BASALT is a versatile toolkit that recovers, compares and optimizes MAGs across a series of assemblies assembled from short-read, long-read or hybrid strategies. Firstly, BASALT uses high-throughput assembly methods to automatically assemble/co-assemble multiple files in parallel to reduce the manual input; Next, BASALT incorporates self-designed algorithms which automates the separation of redundant bins to elongate and refine best bins and improve contiguity; Further, BASALT facilitates state-of-art refinement tools using third-generation sequencing data to calibrate assembled bins and complement genome gaps that unable to be recalled from bins; Lastly, BASALT is an open frame toolkit that allows multiple integration of bioinformatic tools, which can optimize a wide range of datasets from various of assembly and binning software.

##### SYSTEM REQUIREMENTS
The resource requirements for this pipeline will be based on the amount of data being processed. However, due to large memory requirements of many softwares used (e.g. SPAdes), 8+ cores and 125GB+ RAM are recommended. BASALT officially supports only Linux x64 systems.

##### INSTALLATION
As there are many required dependencies needed to install, we highly recommend that you install and manage BASALT with conda. Once you have Miniconda or Anaconda installed, create a conda environment and install the BASALT within the specific environment.

1 Download this basalt_env.yml.

2 (Optional) You can also use mirroring to increase the download speed of BASALT dependent software. For example:


```
site=https://mirrors.tuna.tsinghua.edu.cn/anaconda
conda config --add channels ${site}/pkgs/free/ 
conda config --add channels ${site}/pkgs/main/
conda config --add channels ${site}/cloud/conda-forge/
conda config --add channels ${site}/cloud/bioconda/ 
```
 



3 Make a new conda environment to install and manage all dependancies:
```
conda env create -n BASALT --file basalt_env.yml
```
The step 3 will take a while.

4 Download this BASALT.zip. Then upload this file to your Linux directory.
```
unzip BASALT.zip
chmod -R 750 BASALT
```
Move BASALT files to your conda BASALT environment. In general, your conda BASALT environment is located in the subdirectory envs of the conda installation (e.g. /home/anaconda2/envs/).
```
mv BASALT/* /home/anaconda2/envs/BASALT/bin
```

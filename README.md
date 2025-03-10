# ShortCourseBioinformatics_BB4F
Official repository of the Bioinformatics Short Course - Decoding (Meta)genomes for Natural Products Discovery, an initiative of the BlueBio4Future ERA Chair (March 17th to March 19th, 2025, Porto). 


> [!IMPORTANT]
> It is recommended that participants arrive with all the required programs installed properly. Carefully reading this GitHub page is also recommended.

# 01 Before arriving to the short course
# Software Prerequisites

For Windows users:
Download Ubuntu subsystem for Windows - directly from the Microsoft store or from the official website.
+ [Windows](https://ubuntu.com/desktop/wsl)

#  Python and Conda environment

Check if you already have python installed. You  can do so by typing `python` in your terminal.

Otherwise, install python. Type in your terminal:
```
sudo apt update
```
```
sudo apt install python3 python3-pip
```

#  Setting up conda
In your terminal type:

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```
```
bash Miniconda3-latest-Linux-x86_64.sh
```
+ press ENTER, scroll down, type in ‘yes’
+ press ENTER
+ type in yes

Add conda channels
```
conda config --add channels defaults
```
```
conda config --add channels conda-forge
```
```
conda config --add channels bioconda
```

Or follow the instructions here:
+ [Windows/macOS miniconda installation](https://www.anaconda.com/docs/getting-started/miniconda/install#macos-linux-installation)

# 02 Getting started at this ahort course

If you have successfully completed all the steps above, now you are ready to get started installing the required programs for the hans-on sessions.

 + Check here the installation instructions for [BiG-SCAPE](https://github.com/medema-group/BiG-SCAPE/wiki/01.-Installing-and-Running-BiG-SCAPE).

+ Check here the installation instructions for [CORASON](https://bigscape-corason.secondarymetabolites.org/installation/).


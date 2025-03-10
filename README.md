# ShortCourseBioinformatics_BB4F
Official repository of the Bioinformatics Short Course - Decoding (Meta)genomes for Natural Products Discovery, an initiative of the BlueBio4Future ERA Chair (March 17th to March 19th, 2025, Porto). 


> [!IMPORTANT]
> It is recommended that participants arrive with all the required programs installed properly. Carefully reading this GitHub page is also recommended.

# Before arriving to the short course
# 01 Programs installation

For Windows users:
Download Ubuntu subsystem for windows - directly from the Microsoft store or from the official website.
+ [Windows]([https://www.python.org/downloads/windows/](https://ubuntu.com/desktop/wsl).

#Python & Conda environment

Check if you already have python installed. You  can do so by typing `python` in your terminal.

Otherwise, install python from here:

Familiarize yourself with unix (here and/or here) and conda.

If you do not already have an ssh client as part of the operating system (e.g., if you have a Windows machine), download a third party software such as one of the following:

MobaXterm
PuTTY
Cygwin
For file transfer on Windows, we recommend downloading winscp
Getting started at the workshop
Open your ssh client and connect to Cousteau (the ETH teaching server)
Click for instructions:
Setting up conda
Click for instructions:

In your terminal type:
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

bash Miniconda3-latest-Linux-x86_64.sh

press ENTER, scroll down, type in ‘yes’

press ENTER

type in yes

close and reopen session (exit then ssh cousteau)

rm Miniconda3-latest-Linux-x86_64.sh

Install should take ~5min

Log out and log in again
Add conda channels
conda config --add channels defaults
conda config --add channels conda-forge
conda config --add channels bioconda


https://github.com/medema-group/BiG-SCAPE/wiki/01.-Installing-and-Running-BiG-SCAPE

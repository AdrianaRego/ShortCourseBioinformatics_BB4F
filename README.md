# ShortCourseBioinformatics_BB4F
Official repository of the Bioinformatics Short Course - Decoding (Meta)genomes for Natural Products Discovery, an initiative of the BlueBio4Future ERA Chair (March 17th to March 19th, 2025, Porto). 

You can find information about the researchers who will lead the course, targeting cutting-edge tools and techniques used in bioinformatics pipelines for natural product discovery, in the course [website](https://bb4f.ciimar.up.pt/short-course-in-bioinformatics/).

Find the course agenda [here](https://github.com/AdrianaRego/ShortCourseBioinformatics_BB4F/blob/main/agenda_shortcourse%20bioinformatics_update_15.03.25.pdf).

# Schedule
 Day 1 - 17th 
Time         | Topic         | Instructor    |
   --------- | ------------- | ------------- |
   10h15     |  [Introduction to Bioinformatics in Natural Products Discovery](https://github.com/AdrianaRego/ShortCourseBioinformatics_BB4F/blob/main/Introduction_bioinformatics_NPs.pdf)  | Adriana Rego  |    
  11h        | NLP/AI for Functional Annotation of Enzymes  | Leandro Pereira |
12h/14h	     |antiSMASH and BiG-SCAPE workflows [Hands-on session](https://github.com/CatarinaCarolina/Genome-Mining-2025?tab=readme-ov-file) | Catarina Loureiro
16h          |[GNPS and MicrobeMASST](https://docs.google.com/presentation/d/1E4EZYhA7jc0fRYiGQpEI2GeZAwvSY8J7vxOF9a15u80/edit#slide=id.g29070bedc82_0_126) [Link Documents](https://docs.google.com/document/d/1mX5aPMZDAzsgU2ARXYCndQYs1PtAeb3KkrCJZ4xgQZQ/edit?tab=t.0)] | Mauricio Caraballo

> [!IMPORTANT]
> It is recommended that participants arrive with all the required programs installed properly. Carefully reading this GitHub page is also recommended.

# 01 Before arriving to the short course
# Software Prerequisites

For Windows users:
Download Ubuntu subsystem for Windows - directly from the Microsoft store or from the official website.
+ [Windows](https://ubuntu.com/desktop/wsl)

#  Python and Conda environment

Check if you already have python installed. You  can do so by typing `python3` in your terminal.

Otherwise, install python. Type in your terminal:
```
sudo apt update
```
```
sudo apt install python3
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


Or follow the instructions here:
+ [Windows/macOS miniconda installation](https://www.anaconda.com/docs/getting-started/miniconda/install#macos-linux-installation)

# 02 Getting started at this short course

If you have successfully completed all the steps above, now you are ready to get started installing the required programs for the hans-on sessions.

 + Check here the installation instructions for [BiG-SCAPE](https://github.com/medema-group/BiG-SCAPE/wiki/01.-Installing-and-Running-BiG-SCAPE).

+ Check below the installation instructions for CORASON:


Check if you already have curl installed. You  can do so by typing `curl` in your terminal.

Otherwise, install curl. Type in your terminal:
```
sudo apt-get update
```
```
sudo apt-get install curl
```
CORASON is run using Docker, a container platform provider available for multiple operating systems. 
Let's start with linux minimal docker installation:
```
curl -fsSL https://get.docker.com/ | sh
```
Then type (without brackets):
```
sudo usermod -aG docker [your username]
```
Then log out from your session (restart your machine) and get back in into your user session before the next step. Test the docker installation:

```
docker run hello-world
```
After successfully installing docker, we can install CORASON:
```
mkdir ~/bin    # not required if you already have that
```
```
curl -q https://raw.githubusercontent.com/nselem/corason/master/run_corason > ~/bin/run_corason
```
```
chmod a+x ~/bin/run_corason
```
```
~/bin/run_corason
```

More information in [CORASON](https://bigscape-corason.secondarymetabolites.org/installation/) website.

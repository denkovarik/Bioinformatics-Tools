# Annotate-KEGG-Pathway

## Introduction
This project was designed to help researchers use the biochemical pathways on KEGG (KEGG pathways) to analyze the genome of an organism. Specifically, it indicates which proteins from a KEGG pathway are present in an organism's genome. This project reads the excel file of an organism's genome annotation and records the EC numbers for the proteins present in them. Then it parses the html file of a KEGG pathway to determine the EC numbers of the proteins present in the pathway. The program compares the proteins from the KEGG pathway to the proteins found in the organism's genome annotation. Proteins from a genome annotation that are also found to be present in a KEGG Pathway are indicated by colored boxes around the protein's EC Number in the KEGG Pathway. When completed, the annotated KEGG pathway will open up in your browser as a working webpage. 

## Setup
This project was developed for the Window's Operating System on a 64 bit machine.

### Dependences
* Git
* Python 3
* pillow
* pandas
* openpyxl
* PySimpleGUI
* xlrd

### Install Python 3.9
The project relies on Python 3.9 in order to runs. This link, [Python 3.9 Download](https://www.python.org/downloads/), will help you download and install both.

### Install Git on Windows
The first thing you need to do is to make sure that Git is installed on your device. This would allow you to clone and download this repository on your device. If necessary, the tutorial [Install Git](https://github.com/git-guides/install-git) will walk you through how to do this.

### Cloning This Repo with HTTPS
To download this repository on your device, you must clone this repo using either HTTPS or SSH. The easiest way to clone this repository on your local device is through HTTPS. If your SDK allows you to clone a repo through HTTPS, then do so. Otherwise, you can do it directly on the command prompt. To do so, open up the command prompt and move to the desired directory. Then simply run the following command and enter you credentials if prompted to do so.
```
git clone https://github.com/denkovarik/Annotate-KEGG-Pathway.git
```
After the repo has been cloned on your device, move into the Annotate-KEGG-Pathway directory from the command line.
```
cd Annotate-KEGG-Pathway
```

### Cloning This Repo with SSH
You can also clone this repo using SSH. Follow the instructions below to clone the repo using SSH. Please note that if you have already cloned the repo using HTTPS, then you can skip to the 'Install Dependencies' step. If you wish to clone this repo using SSH, then please note that you will need an account on Github or Gitlab.

#### Generate an SSH Key Pair
In order to clone this repository, you need to add your public SSH key to this repo. If you don't have one, then you would need to generate one. [How to Generate SSH key in Windows 10? Easy Methods!!](https://techpaal.com/how-to-generate-ssh-key-in-windows-10-easy-methods/) should help you generate an SSH key pair.

#### Add Your Public SSH Key to GitHub
Once you have an SSH Key Pair generated, you need to add your public SSH key to GitHub. Follow [How to view your SSH keys in Linux, macOS, and Windows](https://www.techrepublic.com/article/how-to-view-your-ssh-keys-in-linux-macos-and-windows/) to access you public key. Then follow [Adding a new SSH key to your GitHub account](https://docs.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account) to add your public SSH key to GitHub.

#### Clone the Repository
If your SDK allows for it, then clone this repository through your SDK. Otherwise, open up the command prompt, move into the directory of your choice, then run the following command.
```
git clone git@github.com:denkovarik/Annotate-KEGG-Pathway.git
```
After the repo has been cloned on your device, move into the Annotate-KEGG-Pathway directory from the command line.
```
cd Annotate-KEGG-Pathway
```

### Install Dependencies
Next, install the dependencies needed for the project. This can be done by simply running 'setup.bat' by doulble clicking on it in the file explorer. Alternatively, you can run this script by executing the following command on the command line from within the project directory.
```
setup.bat
```

## Usage
First downloaded the complete webpage of the KEGG Pathway you want to annotate and save it an a known location. On the KEGG homepage, select 'KEGG Pathway'. Please note that the saved pathway should consist of an .htm file and a folder containing more files and images. To save the complete webpage to your local device, open the KEGG Pathway you want to annotate in your browser. Select 'File', then 'Select Save Page...'. Select the directory that you wish to save the page to, and make sure that the option 'Save as type:' is selected in the 'Save as type:' box. Then select save, and the complete webpage should be saved in the selected folder on you local device.

To start the program run 'start.py'. This can be done by double clicking on 'start.py' in the file explorer. Alternativley from the command line in the project directory, run the following command.
```
py start.py
```

Upon startup, this program will ask for 4 filepaths. Enter either the filepath for the RAST genome annotataion excel spreadsheet, the filepath for the PATRIC genome annotataion excel spreadsheet, or both. Please note that only one of these excel spreadsheets are needed, but the program will also except both. Select the .htm file from the downloaded "
usage += "pathway that you want to annotate. Finally, select the output directory that you want the program to place the annotated KEGG Pathway in. This will be a webpage that should open up in your browser.

Finally, select 'Go'. The pathway will be annotated indicating which proteins in the pathway are also present in your organism. A green box means that the gene for a protein was found in both the RAST and PATRIC genome annotations. An orange box indicates that the gene for the protein was only found in the RAST genome annotation. Blue boxes means that the gene for the protein was only found in the PATRIC genome annotation.

## Author
* Dennis Kovarik

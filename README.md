# GroundSegment
This repository holds all the general information regarding the ground segment subsystem. 

- [GroundSegment](#groundsegment)
  - [General project information](#general-project-information)
  - [Repository structure](#repository-structure)
  - [Main requirements key points for GS subsystem](#main-requirements-key-points-for-gs-subsystem)
  - [System overview](#system-overview)
  - [Annex](#annex)
    - [Build LaTeX Document](#build-latex-document)

## General project information
This is part of the Firehorn project, created by the EPFL Rocket Team. The goal of the project is to develop the first student bi-liquid rocket capable of reaching 9km.

This repository is one of six repositories on this Git account dedicated to all the code within the ground segment subsystem. 

On the same account you'll find the other repositories
- [**Control**](https://github.com/LaGSdeKarlHeinz/LPCamera) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ground Segment Control (GUI, ...) 
- [**Motherboard**](https://github.com/LaGSdeKarlHeinz/Motherboard) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Motherboard interfacing Radioboard and GSC
- [**RadioBoard**](https://github.com/LaGSdeKarlHeinz/Radioboard) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Radio Communications boards
- [**Tracker**](https://github.com/LaGSdeKarlHeinz/Tracker) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Rocket Tracker, both Antenna and Camera
- [**LPCamera**](https://github.com/LaGSdeKarlHeinz/LPCamera) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Launch Pad Camera module


## Repository structure

This repository is organized as follows:

- Readme.md: this file
- **Documentation**: All documentations of GS
  - GroundSegment.pdf: Latest verified GS documentation
  - **latex**: files used to build the document
    - GroundSegment.pdf: Latest *not verified* GS documentation
    - main.tex: main LaTeX file
    - packages_list.tex: all packages used within the LaTeX project
    - Makefile: used to build LaTeX project ([more information here](#build-latex-document))
    - preview.bat: open the document in firefox (windows) for us because we are lazy
    - **General**
      - .tex files concerning general stuff
    - **GS**
      - .tex files concerning GS stuff
    - **Images**
      - All documentation images sorted by theme
    - **Interface**
      - .tex files concerning interfaces

## Main requirements key points for GS subsystem
- **GS Declaratition of Purpose** : The GST will support the communication with the LV (Launch Vehicle) and GSE (Ground Station Equipment) from the ground before, during and after the flight.
- **EuRoC** : The GS shall comply to the rules enonced in the Appendix B of the Appendix Design_Test_Evaluation_Guide document povided by the EuRoC (European Rocket Competition).
- **Human Ressources** : GS operations shall require at most 2 team members for setup and operation.

For full details, refer to project documentation (not yet written) or contact the team.


## System overview
**TO DO**

## Annex

### Build LaTeX Document
Make sure you have LaTeX install on your computer.
Our version is *MiKTeX-pdfTeX 4.16 (MiKTeX 23.10.12)*

Go to `GroundSegment/Documentation/latex` in a terminal and execute the following command

If you have the make utility package install in your computer, you can just do 

    make

This will build the *main.tex* file to *GroundSegment.pdf* in the same directory. 
There is also 
- `make clean` to remove all compilation file
- `make rmpdf` to remove the pdf

If you don't have make package at disposition, just do 

    pdflatex main.tex --job-name=GroundSegment

**Latex may ask to install packages**, accept it or you won't be able to build the document.

Now your document should be ready and you have a GroundSegment.pdf file.
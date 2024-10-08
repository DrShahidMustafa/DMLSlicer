# DMLSlicer
It is a slicer for the Direct Metal Laser Sintering (DMLS),  the powder bed fusion process for metal-AM

## What's this DMLSlicer?
DMLSlicer  is  a laser exposure vector genertor  for PBF based 3D printers: it reads 3D models (STL, OBJ, AMF, 3MF) and it converts them into instructions for the laser scan paths. It is under development and currently, exposes only the basic function of generating laser beam scan stategies for the core component and the support structure.

DMLSlicer is based on libslic3r, which are the core libraries of Slic3r.  The original Slic3r is  high configurable but does not support 3D printing of metal parts with powder bed fusion technology such as Direct Metal Laser Sintering (DMLS) also known as SLM. 

DMLSlicer may serve as  a platform for implementing several new (experimental) ideas in DMLS process, such as multiple energy beams, new design of support structures, variable-height layers, built-plate  settings, machine integration, post-processing scripts, and more. 

## What language is it written in?
The core parts of DMLSlicer  are written in C++11, with multithreading. Currently, there is no  graphical interface.

## How to built?
**Cmake**  is used as the build system. The external dependancies are manged with  **vcpkg**. This makes the process of compiling fully automated and painfree.

### Directory structure


* `src/dmlslicer`: the C++ source of the `DMLSlicer` executable and the CMake definition file for compiling it
* `src/GUI`: The C++ GUI. Yet to be implemented

* `src/Utilities/`: various useful libraries
* `src/Core/`: C++ sources for libslic3r and many more

### Acknowledgements

The use of  libslic3r  is acknowledged in this project.


### How can I invoke Slic3r using the command line?

The command line  instruction is     DMLSlic3r --export-svg  example.stl --load  example.ini 


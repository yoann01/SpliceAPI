Fabric Splice API
======================
A C/C++ API for creating cross-DCC portable runtimes.

Fabric Splice API allows you to make use of the Fabric Core inside of DCCs, and persist custom runtime to be able to use them across multiple DCC applications.

Repository Status
=================

This repository will be maintained and kept up to date by Fabric Software to match the latest Fabric Core.

Supported platforms
===================

To date all three major platforms (windows, linux, osx) are supported, if you build the thirdparty dependencies for the corresponding platform.

Building
========

A scons (http://www.scons.org/) build script is provided. Fabric Splice API depends on
* A static build of boost (http://www.boost.org/), version 1.55 or higher.
* A dynamic build of Fabric Core (matching the latest version).
* The FTL (Fabric Template Library) repository (it can be pulled here: https://github.com/fabric-engine/FTL).

To inform scons where to find the Fabric Core includes as well as the thirdparty libraries, you need to set the following environment variables:

* FABRIC_BUILD_OS: Should be the type of OS you are building for (Windows, Darwin, Linux)
* FABRIC_BUILD_ARCH: The architecture you are building for (x86, x86_64)
* FABRIC_BUILD_TYPE: The optimization type (Release, Debug)
* FABRIC_SPLICE_VERSION: Refers to the version you want to build. Typically the name of the branch (for example 1.13.0)
* FABRIC_DIR: Should point to Fabric Engine's installation folder.
* BOOST_DIR: Should point to the boost root folder (containing boost/ (includes) and lib/ for the static libraries).

The temporary files will be built into the *.build* folder, while the structured output files will be placed in the *.stage* folder.

To perform a build you can just run

    scons all -j8

To clean the build you can run

    scons clean    

License
==========

The license used for this API can be found in the root folder of this repository.

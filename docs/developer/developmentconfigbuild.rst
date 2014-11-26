
===================================
Development Configuration and Build
===================================

Authors: Hugh Sorby, David & Andre Nickerson.

This document describes how you configure and build the libCellML library.

.. contents::

Overview
========

After following the :doc:`setup process <developmentsetup>` you need to configure and build the library.  The libCellML library uses a recent version CMake for generating environment specific build scripts.  To configure and build libCellML you will need a recent version of CMake and a compiler toolchain (gcc, clang, cl, intel).  You can configure the build either through the command line or a CMake GUI interface.  Detailed steps are given below for each platform that libCellML is tested on.

From the command line we can configure the following variables to change the build::

  BUILD_TYPE - Choose the type of build: Debug, Release, etc. (Debug is the default build)
  INSTALL_PREFIX - Set the install prefix
  COVERAGE - Enable coverage profiling (available only with gcc compilers)
  MEMCHECK - Enable memory checking (available only with gcc compilers)
  
These same variables can be set in a GUI but the names will have LIBCELLML\_ prefixed to them.

Linux Command Line
==================

The following commands will configure and build a release version of the libCellML library on Linux from the command line::

  mkdir libcellml-build
  cd libcellml-build
  cmake -DBUILD_TYPE=Release ../libcellml
  make 

OS X Command Line
=================

The following commands will configure and build a release version of the libCellML library on OS X from the command line::

  mkdir libcellml-build
  cd libcellml-build
  cmake -DBUILD_TYPE=Release ../libcellml
  make
  
Windows Command Prompt
======================

The following commands will configure and build a 32 bit release version of the libCellML library on OS X from the command line::

  "C:\\<install specific location of >\\vcvarsall.bat" x86
  mkdir libcellml-build
  cd libcellml-build
  cmake -G"NMake Makefiles" -DBUILD_TYPE=Release ../libcellml
  nmake
  





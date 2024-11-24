# Root Directory Readme

##Table Of Contents
 1. [Repository Contents](#repository-contents)
 1. [Assumptions](#assumptions)
 1. [Getting Started](#getting-started)
 1. [About the development environment, tools and source code](#about-the-development-environment--tools-and-source-code)
 1. [Design Goals](#design-goals)
 1. [Directory Layout](#directory-layout)
 1. [Testing](#testing)
 1. [References](#references)
 1. [Note from the author](#note-from-the-author)

### Repository Contents

This repository contains a collection of general purpose interface classes and libraries written in C++
which target embedded systems.  The contents are:

1. [Finite State Machine](#./FiniteStateMachine/readme.md)

### Assumptions

The author assumes that the reader is an experienced software developer or student who has C++ training and 
understands the tools and processes discussed or can read the reference links to learn.  Git needs to 
be installed before proceeding to the Getting Started section.

### Getting Started

1. Clone the repository to your location of choice using ```git clone https://github.com/rminer57/Cpp-Embedded-Interfaces.git```


### About the development environment, tools and source code

All code is written in C++ using standard [C++23](https://en.wikipedia.org/wiki/C%2B%2B23). While many companies use proprietary end-to-end 
embedded development solutions including an OS such as Wind River, here we use open source tools.  
The operating system used was Ubuntu Linux.  Using Cygwin, Mingw64 or git bash for windows is possible but installing additional tools can
be harder than it is on Ubuntu.  [CMake](https://cmake.org/getting-started/) was used to create the build environment.
The [GNU](https://gcc.gnu.org/) compiler and linker are used to build artifacts. For testing, we use [googletest](https://github.com/google/googletest).
For documentation, we use markdown, [doxygen](https://www.doxygen.nl/manual/index.html) and [plantuml](https://plantuml.com/), all industry standard.   

### Design Goals

The following were the intended design goals:

1. Portability, not restricted to a particular architecture or endiness.
2. Extensability, adding new functionality should be easy. 
3. Testability, the code strives to be testable with 100% execution path coverage.
4. Loose Coupling, keep dependencies between components at a minimum.
5. Optimized for Embedded, solutions consider embedded system constraints.
6. Fast Board Bringup, get a new development board up and running fast.
7. Good documentation, easy understanding of the code and how to change it to suit needs.
8. Adherance to MISRA standards in writing code, for obvious reasons.
9. Favor use of applicable UML design patterns.

### Directory Layout

Every project the author has worked on, had a different directory structure from other projects.  The structure used will
depend on who the technical lead is and what structure they favor.  The author is not dogmatic about the matter and
recognizes that there are many good ways to do it and that there are trade-offs in every choice.  Having said that, as a 
project grows and hundreds of source files are added, it can become difficult to find things.  VSCode intellisense will help
that but a well organized directory structure that follows the software architecture will make things easier for developers.
The author has found that keeping it as simple as possible is best, therefore the following is used:

```
<name>/
│
└── build/
│   ├── build
│   ├── a.out
│   ├── a.map
│
└── docs/
│   ├── doxygen/
│   ├── markdowns/
│
├── src/
│   ├── foo.h
│   ├── foo.cpp
│
└── test/
│   ├── footest.h
│   ├── footest.cpp
│
├── readme.md
```

*  build - contains the build script and all build output artifacts are placed here. See its readme.
*  docs - contains documentation including doxygen output. See its readme.
*  src - contains source and header files. See its readme.
*  test - contains unit test framework and files. See its readme.

### Testing

to be done

### References

See

### Note from the author

The author is an embedded software developer with over 20 years professional experience with C++ development for
embedded systems at companies such as Motorola, Ford Motor Company, Caterpillar and Maxar Technologies.
These files are intended to reflect the best practices learned during a long career.  If you are
curious to know more, take a look at [linkedin](https://www.linkedin.com/in/randall-miner-bsce)

It has always been frustrating to clone some tool or utility on gitlab, only to discover that the
author provides no documentation on how to build, install and use it. Apparently it was considered intuitively
obvious which might not be the case.  To avoid that for this repository, great pains were taken
to explain everything one needs to know.  If you have comments or suggestions, they are most welcome and all will
be carefully considered.





# OrbSLAM3_Setup
## Installing OrbSLAM3 and its dependencies : 
This document is supposed to be used with in conjunction with the official documentation of OrbSLAM3, while working on 
this document I didn't know much about cpp, pangolin, eigen3, g20, and other dependencies. In the past, I had issues installing
these dependencies, this document is an attempt to systematically approach the installation process.

## What is MultiMap? in ORB-SLAM3 is the first real-time SLAM library able to perform Visual, Visual-Inertial and Multi-Map SLAM with monocular, stereo and RGB-D cameras, using pin-hole and fisheye lens models. 

A multi-map in ORB-SLAM3 is a feature of the library that allows it to perform simultaneous localization and mapping (SLAM) using multiple maps.
This means that the system can keep track of multiple different environments and switch between them as needed, rather than only being able to 
handle one map at a time. This can be useful in applications such as robots or autonomous vehicles that need to navigate multiple different environments.

## Explain : C++11 or C++0x Compiler : We use the new thread and chrono functionalities of C++11.

C++11 is the name given to the version of the C++ programming language that was released in 2011. It introduced several new features and improvements to the language, including threading and timing functionalities.

A C++11 compiler is a compiler that is capable of understanding and implementing the new features and changes introduced in C++11. These functionalities include new data types such as std::chrono::duration, std::chrono::time_point, and several new functions like std::this_thread::sleep_for, std::this_thread::sleep_until that are used for precise time management.

A C++0x compiler is a compiler that is capable of understanding and implementing the new features and changes introduced in C++11, also known as C++0x. The "0x" in the name refers to the hexadecimal representation of the version number (11 in decimal is 0xB in hexadecimal).

In the statement given, the use of the new thread and chrono functionalities of C++11 means that the software is utilizing the threading and timing features that were introduced in the C++11 standard.

## STEPS TO INSTALL PRE-REQUISITES:
### 1. Check C++ version with command
```sh
g++ --version
# This will print the GNU C++ compiler (g++) that is installed on the system
```
or alternatively one can use 
```sh
cpp --version
# This will display the version of the C preprocessor (cpp) that is currently installed on your system.
```

The C preprocessor (cpp) and the C++ compiler (g++) are two separate tools that are used in the process of compiling C++ code.

The C preprocessor is a program that processes source code before it is passed to the compiler. It is used to handle things like macro expansion, conditional compilation, and include directives. It takes the source code as input, performs preprocessing on it, and then passes the preprocessed code to the compiler.

The C++ compiler, on the other hand, is responsible for converting the preprocessed C++ code into machine code that can be executed by the computer. The compiler checks the syntax of the code, generates assembly code, and then converts the assembly code into machine code.

### 2. Install Pangolin
Pangolin is a lightweight C++ library for creating interactive multi-dimensional visualisations. It is often used in computer vision and robotics applications. Try running 
```sh
pangolin-config --version
# If Pangolin is already installed, this prints the version number.
```
If not previously installed, you can get [Pangolin](https://github.com/stevenlovegrove/Pangolin) here.

## Installing Pangolin(vcpkg) ##

You can download and install pangolin using the [vcpkg](https://github.com/Microsoft/vcpkg) dependency manager:

    git clone https://github.com/Microsoft/vcpkg.git
    cd vcpkg
    ./bootstrap-vcpkg.sh
    ./vcpkg integrate install
    ./vcpkg install pangolin

The pangolin port in vcpkg is kept up to date by Microsoft team members and community contributors. If the version is out of date, please [create an issue or pull request](https://github.com/Microsoft/vcpkg) on the vcpkg repository.



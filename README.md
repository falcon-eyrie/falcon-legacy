# Falcon

> [!Important]
> **Note:** This repository is the legacy version of **Falcon**.  
> Active development continues at **falcon-core**:  
> https://github.com/falcon-eyrie/falcon-core


## Overview

Falcon is a high-performance, modular software platform for real-time closed-loop neuroscience experiments. It provides a multithreaded graph-based processing pipeline that allows neural data to be streamed, processed, and acted on with very low latency. Falcon is flexible, extensible, and designed to support custom processing nodes and experimental workflows while maintaining reliable millisecond-scale performance. See the original [paper](https://iopscience.iop.org/article/10.1088/1741-2552/aa7526) for more details.


## Dependencies


### zeromq
```
    sudo apt-get install libzmq3-dev
```

###  C++ boost libraries
```
    sudo apt-get install libboost-all-dev
```

###  CMAKE
```
    sudo apt-get install cmake
```

###  G++ compiler (v5 or higher)
```
    sudo apt-get install g++
```

###  GSL libraries
```
    sudo apt-get install libgsl0ldbl
    sudo apt-get install libgsl0-dev
```

###  Z-lib (needed by cnpy)
```
    sudo apt-get install zlib1g
    sudo apt-get install zlib1g-dev
```

###  External libraries included in source tree

g3log
cppzmq (header only library)
cmdline (header only library)
disruptor
cnpy
yaml-cpp

###  External libraries not included in source tree

USB-4750 DIO card drivers (see dedicated doc for more information)

## Build instructions

To compile issue the following commands while in the falcon root directory: 

```
    mkdir build
    cd build
    cmake -DCMAKE_CXX_COMPILER=`g++` ..
    make
```


## Installation instructions

```
    cd build/src
    cp falcon ~/bin
    sudo setcap 'cap_sys_nice=pe' ~/bin/falcon
```

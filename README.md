# A new version of Falcon is in development !
# Most processors and datatypes have been ported on the new version - Check out the documentation [here!](https://falcon-core.readthedocs.io)



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
